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
# <a name="encrypting-data"></a><span data-ttu-id="1f1e8-103">Cifrar datos</span><span class="sxs-lookup"><span data-stu-id="1f1e8-103">Encrypting Data</span></span>

<span data-ttu-id="1f1e8-104">En el procedimiento siguiente se describen los pasos que se deben seguir para cifrar un mensaje con las funciones de criptografía base.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-104">The following procedure describes steps to take to encrypt a message with the Base Cryptography Functions.</span></span> <span data-ttu-id="1f1e8-105">Para cifrar mensajes mediante \# estándares PKCS 7, consulte [funciones de mensaje de bajo nivel](cryptography-functions.md) y [funciones de mensaje simplificadas](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1f1e8-105">To encrypt messages using PKCS \#7 standards, see [Low-level Message Functions](cryptography-functions.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="1f1e8-106">**Para cifrar un mensaje**</span><span class="sxs-lookup"><span data-stu-id="1f1e8-106">**To encrypt a message**</span></span>

1.  <span data-ttu-id="1f1e8-107">Genere una clave de sesión mediante la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="1f1e8-107">Generate a session key by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>

    <span data-ttu-id="1f1e8-108">Al realizar esta llamada, se genera una clave aleatoria y se devuelve un identificador para que se pueda usar la clave para cifrar y descifrar los datos.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-108">Making this call generates a random key and returns a handle so the key can be used to encrypt and decrypt data.</span></span> <span data-ttu-id="1f1e8-109">El algoritmo de cifrado que se va a usar también se especifica en este momento.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-109">The encryption algorithm to use is also specified at this point.</span></span> <span data-ttu-id="1f1e8-110">Dado que CryptoAPI no permite a las aplicaciones usar algoritmos de clave pública para cifrar datos masivos, especifique un algoritmo simétrico como RC2 o RC4 con la llamada [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="1f1e8-110">Because CryptoAPI does not permit applications to use public key algorithms to encrypt bulk data, specify a symmetric algorithm such as RC2 or RC4 with the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) call.</span></span>

2.  <span data-ttu-id="1f1e8-111">También puede usar la función [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) para transformar una contraseña en una clave adecuada para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-111">Alternatively, use the [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) function to transform a password into a key suitable for encryption.</span></span>

    <span data-ttu-id="1f1e8-112">Si una aplicación necesita cifrar el mensaje para que cualquier persona con una contraseña especificada pueda descifrar los datos, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) para transformar la contraseña en una clave adecuada para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-112">If an application needs to encrypt the message so that anyone with a specified password can decrypt the data, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) to transform the password into a key suitable for encryption.</span></span>

    > [!Note]  
    > <span data-ttu-id="1f1e8-113">En este caso, se llama a esta función en lugar de a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) y no se necesitan las llamadas posteriores a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) .</span><span class="sxs-lookup"><span data-stu-id="1f1e8-113">In this case, this function is called instead of the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function and the subsequent [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls are not needed.</span></span>

     

3.  <span data-ttu-id="1f1e8-114">Si es necesario, establezca propiedades criptográficas adicionales de la clave mediante la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)</span><span class="sxs-lookup"><span data-stu-id="1f1e8-114">If necessary, set extra cryptographic properties of the key by using the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function</span></span>

    <span data-ttu-id="1f1e8-115">Una vez generada la clave, se pueden establecer propiedades criptográficas adicionales de la clave con la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="1f1e8-115">After the key has been generated, extra cryptographic properties of the key can be set with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)function.</span></span> <span data-ttu-id="1f1e8-116">Esta función permite cifrar diferentes secciones del archivo con diferentes sales Key y proporciona una manera de cambiar el modo de cifrado o el vector de inicialización de la clave.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-116">This function allows different sections of the file to be encrypted with different key salts and provides a way to change the cipher mode or initialization vector of the key.</span></span> <span data-ttu-id="1f1e8-117">Estos parámetros se pueden usar para hacer que el cifrado cumpla con un estándar de cifrado de datos determinado.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-117">These parameters can be used to make the encryption conform with a particular data encryption standard.</span></span>

4.  <span data-ttu-id="1f1e8-118">Cifre los datos del archivo con la función [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="1f1e8-118">Encrypt the data in the file with the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function.</span></span>

    <span data-ttu-id="1f1e8-119">La función [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) toma la clave de sesión que se generó en el paso anterior y cifra un búfer de datos.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-119">The [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function takes the session key that was generated in the previous step and encrypts a buffer of data.</span></span>

    > [!Note]  
    > <span data-ttu-id="1f1e8-120">A medida que se cifran los datos, los datos se pueden expandir ligeramente mediante el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-120">As the data is encrypted, the data may be slightly expanded by the encryption algorithm.</span></span> <span data-ttu-id="1f1e8-121">La aplicación es responsable de recordar la longitud de los datos cifrados, por lo que se puede especificar la longitud adecuada para la función [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="1f1e8-121">The application is responsible for remembering the length of the encrypted data so the proper length can later be specified for the [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span>

     

5.  <span data-ttu-id="1f1e8-122">Opcionalmente, utilice la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) para permitir que el usuario actual Descifre los datos en el futuro.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-122">Optionally, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function to allow the current user to decrypt the data in the future.</span></span>

    <span data-ttu-id="1f1e8-123">Para permitir que el usuario actual Descifre los datos en el futuro, la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) se usa para guardar la clave de descifrado en un formato cifrado (un BLOB de clave) que solo se puede descifrar con la clave privada del usuario.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-123">To allow the current user to decrypt the data in the future, the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function is used to save the decryption key in an encrypted form (a key BLOB) that can only be decrypted with the user's private key.</span></span> <span data-ttu-id="1f1e8-124">Esta función requiere la clave pública de intercambio de claves del usuario para este propósito, que se puede obtener mediante la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) .</span><span class="sxs-lookup"><span data-stu-id="1f1e8-124">This function requires the user's key exchange public key for this purpose, which can be obtained by using the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function.</span></span> <span data-ttu-id="1f1e8-125">La función **CryptExportKey** devolverá un BLOB de clave que debe almacenar la aplicación para su uso en el descifrado del archivo.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-125">The **CryptExportKey** function will return a key BLOB that must be stored by the application for use in decrypting the file</span></span>

> [!Note]  
> <span data-ttu-id="1f1e8-126">Si la aplicación tiene certificados (o claves públicas) para otros usuarios, puede permitir que otros usuarios descifren el archivo mediante la realización de llamadas de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) para cada usuario que deba recibir acceso.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-126">If the application has certificates (or public keys) for other users, it can permit other users to decrypt the file by performing [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls for each user who should receive access.</span></span> <span data-ttu-id="1f1e8-127">La aplicación debe almacenar los blobs de clave devueltos, como en el paso 5.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-127">The returned key BLOBs must be stored by the application, as in step 5.</span></span>

 

## <a name="creating-an-encrypted-message"></a><span data-ttu-id="1f1e8-128">Creación de un mensaje cifrado</span><span class="sxs-lookup"><span data-stu-id="1f1e8-128">Creating an Encrypted Message</span></span>

<span data-ttu-id="1f1e8-129">Las funciones de mensaje simplificadas facilitan el cifrado y descifrado de los datos.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-129">The simplified message functions make it easier to encrypt and decrypt data.</span></span> <span data-ttu-id="1f1e8-130">En la ilustración siguiente se muestran las tareas individuales que se deben realizar para cifrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-130">The following illustration depicts the individual tasks that must be accomplished to encrypt a message.</span></span> <span data-ttu-id="1f1e8-131">Los pasos se describen en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-131">The steps are described in the following list.</span></span>

![cifrado de un mensaje](images/encmsg.png)

<span data-ttu-id="1f1e8-133">**Para cifrar un mensaje**</span><span class="sxs-lookup"><span data-stu-id="1f1e8-133">**To encrypt a message**</span></span>

1.  <span data-ttu-id="1f1e8-134">Obtiene un puntero al mensaje de texto simple.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-134">Get a pointer to the plaintext message.</span></span>
2.  <span data-ttu-id="1f1e8-135">Genere una clave simétrica (sesión).</span><span class="sxs-lookup"><span data-stu-id="1f1e8-135">Generate a symmetric (session) key.</span></span>
3.  <span data-ttu-id="1f1e8-136">Mediante la clave simétrica y el algoritmo de cifrado especificado, Cifre los datos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-136">Using the symmetric key and specified encryption algorithm, encrypt the message data.</span></span>
4.  <span data-ttu-id="1f1e8-137">Abra un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-137">Open a certificate store.</span></span>
5.  <span data-ttu-id="1f1e8-138">Obtener el certificado del destinatario.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-138">Get the recipient's certificate.</span></span>
6.  <span data-ttu-id="1f1e8-139">Obtiene la clave pública del certificado del destinatario.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-139">Get the public key from the recipient's certificate.</span></span>
7.  <span data-ttu-id="1f1e8-140">Mediante la clave pública del destinatario, cifre la clave simétrica.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-140">Using the recipient's public key, encrypt the symmetric key.</span></span>
8.  <span data-ttu-id="1f1e8-141">Obtiene el identificador del destinatario del certificado del destinatario.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-141">Get the recipient's identifier from the recipient's certificate.</span></span>
9.  <span data-ttu-id="1f1e8-142">Incluya lo siguiente en el mensaje con doble cifrado: el algoritmo de cifrado de datos, los datos cifrados, la clave simétrica cifrada y el identificador del destinatario.</span><span class="sxs-lookup"><span data-stu-id="1f1e8-142">Include the following in the digitally enveloped message: the data encryption algorithm, the encrypted data, the encrypted symmetric key, and the recipient identifier.</span></span>

 

 



