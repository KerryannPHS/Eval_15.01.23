# Steve_ test

def test_decomposer():
    assert decomposer(123) == (1, 2, 3)
    assert decomposer(456) == (4, 5, 6)
    assert decomposer(789) == (7, 8, 9)
    assert decomposer(100) == (1, 0, 0)

test_decomposer()

def test_somme():
    assert somme(1, 2, 3) == True
    assert somme(4, 5, 6) == True
    assert somme(7, 8, 9) == True
    assert somme(1, 0, 0) == False 

test_somme()

def test_divisible():
    assert divisible(27) == True  # 27 est divisible par 9
    assert divisible(45) == False  # 45 n'est pas divisible par 9
    assert divisible(81) == True  # 81 est divisible par 9
    assert divisible(100) == False  # 100 n'est pas divisible par 9

test_divisible()

def test_devine():
    result = devine()
    assert 100 <= result <= 999
    (c, d, u) = decomposer(result)
    assert somme(c, d, u) and divisible(result)

test_devine()

## Résultat des Tests Unitaires

- **decomposer:** Fonctionne correctement.
- **somme:** Passes tous les tests.
- **divisible:** Quelques échecs sur des cas particuliers.
- **devine:** Fonctionne correctement.

# Turing test

Test Unitaire

# decomposer
assert decomposer(345) == (3, 4, 5)

Nombre en dehors de la plage attendue
assert decomposer(1000) == None

Nombre en dehors de la plage attendue
assert decomposer(99) == None

# somme
assert somme(1, 2, 3) == True

Nombre en dehors de la plage attendue
assert somme(10, 2, 3) == None

Condition de somme non satisfaite
assert somme(1, 2, 4) == False

Nombre divisible par 9
assert divisible(81) == True

Nombre non divisible par 9
assert divisible(7) == False

Nombre négatif divisible par 9
assert divisible(-45) == True

# devine

Le résultat doit être un nombre entre 100 et 999
result = devine()
assert 100 <= result <= 999

Les chiffres du nombre doivent satisfaire les conditions de somme et de divisibilité
(c, d, u) = decomposer(result)
assert somme(c, d, u) == True
assert divisible(result) == True

Test
import unittest

class TestFunctions(unittest.TestCase):
    
    def test_decomposer(self):
        self.assertEqual(decomposer(345), (3, 4, 5))
        self.assertIsNone(decomposer(1000))
        self.assertIsNone(decomposer(99))

    def test_somme(self):
        self.assertTrue(somme(1, 2, 3))
        self.assertIsNone(somme(10, 2, 3))
        self.assertFalse(somme(1, 2, 4))

    def test_divisible(self):
        self.assertTrue(divisible(81))
        self.assertFalse(divisible(7))
        self.assertTrue(divisible(-45))


if __name__ == '__main__':
    unittest.main()


kerryann PAPHOS, 15.01.2024 ver. 1.0

