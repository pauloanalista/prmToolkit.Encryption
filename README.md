# prmToolkit

# Encryption
Classe responsável por criptografar e descriptografar dados ou mensagens

### Installation - Encryption

Para instalar, abra o prompt de comando Package Manager Console do seu Visual Studio e digite o comando abaixo:

```sh
Install-Package prmToolkit.Encryption
```
### Exemplo de como usar

```sh
using System;
using Microsoft.VisualStudio.TestTools.UnitTesting;
using prmToolkit.Encryption;

namespace prmToolkit.Test
{
    [TestClass]
    public class MD5CryptTest
    {
        [TestMethod]
        public void MD5Crypt_Encrypt_Decrypt()
        {
            string senha = "Paulo Rogério";

            string senhaCriptografada = MD5Crypt.Encrypt(senha);

            string senhaDesCriptografada = MD5Crypt.Decrypt(senhaCriptografada);


            string senhaMD5 = MD5Crypt.EncryptMD5(senha);

            Assert.AreEqual(senhaCriptografada, "sE0hI8fXaecNxoHI2IokuQ==");
            Assert.AreEqual(senhaDesCriptografada, senha);
            Assert.AreEqual(senhaMD5, "69103C8FA326DB8B39CB87A6492390C6");
        }
    }
}
```
# VEJA TAMBÉM
## Grupo de Estudo no Telegram
- [Participe gratuitamente do grupo de estudo](https://t.me/blogilovecode)

## Cursos baratos!
- [Meus cursos](https://olha.la/udemy)

## Novidades, cupons de descontos e cursos gratuitos
https://olha.la/ilovecode-receber-cupons-novidades
