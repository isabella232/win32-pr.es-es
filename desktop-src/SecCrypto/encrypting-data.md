---
description: Describe los pasos que se deben seguir para cifrar un mensaje con las funciones de criptografía básicas.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Cifrar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44db44db08268241e399107d8af4088dac3c0c2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565941"
---
# <a name="encrypting-data"></a>Cifrar datos

En el procedimiento siguiente se describen los pasos que se deben seguir para cifrar un mensaje con las funciones de criptografía base. Para cifrar mensajes mediante \# estándares PKCS 7, consulte [funciones de mensaje de bajo nivel](cryptography-functions.md) y [funciones de mensaje simplificadas](cryptography-functions.md).

**Para cifrar un mensaje**

1.  Genere una clave de sesión mediante la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .

    Al realizar esta llamada, se genera una clave aleatoria y se devuelve un identificador para que se pueda usar la clave para cifrar y descifrar los datos. El algoritmo de cifrado que se va a usar también se especifica en este momento. Dado que CryptoAPI no permite a las aplicaciones usar algoritmos de clave pública para cifrar datos masivos, especifique un algoritmo simétrico como RC2 o RC4 con la llamada [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .

2.  También puede usar la función [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) para transformar una contraseña en una clave adecuada para el cifrado.

    Si una aplicación necesita cifrar el mensaje para que cualquier persona con una contraseña especificada pueda descifrar los datos, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) para transformar la contraseña en una clave adecuada para el cifrado.

    > [!Note]  
    > En este caso, se llama a esta función en lugar de a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) y no se necesitan las llamadas posteriores a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) .

     

3.  Si es necesario, establezca propiedades criptográficas adicionales de la clave mediante la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)

    Una vez generada la clave, se pueden establecer propiedades criptográficas adicionales de la clave con la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam). Esta función permite cifrar diferentes secciones del archivo con diferentes sales Key y proporciona una manera de cambiar el modo de cifrado o el vector de inicialización de la clave. Estos parámetros se pueden usar para hacer que el cifrado cumpla con un estándar de cifrado de datos determinado.

4.  Cifre los datos del archivo con la función [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) .

    La función [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) toma la clave de sesión que se generó en el paso anterior y cifra un búfer de datos.

    > [!Note]  
    > A medida que se cifran los datos, los datos se pueden expandir ligeramente mediante el algoritmo de cifrado. La aplicación es responsable de recordar la longitud de los datos cifrados, por lo que se puede especificar la longitud adecuada para la función [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .

     

5.  Opcionalmente, utilice la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) para permitir que el usuario actual Descifre los datos en el futuro.

    Para permitir que el usuario actual Descifre los datos en el futuro, la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) se usa para guardar la clave de descifrado en un formato cifrado (un BLOB de clave) que solo se puede descifrar con la clave privada del usuario. Esta función requiere la clave pública de intercambio de claves del usuario para este propósito, que se puede obtener mediante la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) . La función **CryptExportKey** devolverá un BLOB de clave que debe almacenar la aplicación para su uso en el descifrado del archivo.

> [!Note]  
> Si la aplicación tiene certificados (o claves públicas) para otros usuarios, puede permitir que otros usuarios descifren el archivo mediante la realización de llamadas de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) para cada usuario que deba recibir acceso. La aplicación debe almacenar los blobs de clave devueltos, como en el paso 5.

 

## <a name="creating-an-encrypted-message"></a>Creación de un mensaje cifrado

Las funciones de mensaje simplificadas facilitan el cifrado y descifrado de los datos. En la ilustración siguiente se muestran las tareas individuales que se deben realizar para cifrar un mensaje. Los pasos se describen en la lista siguiente.

![cifrado de un mensaje](images/encmsg.png)

**Para cifrar un mensaje**

1.  Obtiene un puntero al mensaje de texto simple.
2.  Genere una clave simétrica (sesión).
3.  Mediante la clave simétrica y el algoritmo de cifrado especificado, Cifre los datos del mensaje.
4.  Abra un almacén de certificados.
5.  Obtener el certificado del destinatario.
6.  Obtiene la clave pública del certificado del destinatario.
7.  Mediante la clave pública del destinatario, cifre la clave simétrica.
8.  Obtiene el identificador del destinatario del certificado del destinatario.
9.  Incluya lo siguiente en el mensaje con doble cifrado: el algoritmo de cifrado de datos, los datos cifrados, la clave simétrica cifrada y el identificador del destinatario.

 

 



