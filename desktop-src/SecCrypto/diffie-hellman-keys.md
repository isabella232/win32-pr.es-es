---
description: Explica cómo generar, intercambiar, importar y exportar claves de Diffie-Hellman.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Claves de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361628"
---
# <a name="diffie-hellman-keys"></a><span data-ttu-id="8c2d4-103">Claves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="8c2d4-103">Diffie-Hellman Keys</span></span>

-   [<span data-ttu-id="8c2d4-104">Generar claves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="8c2d4-104">Generating Diffie-Hellman Keys</span></span>](#generating-diffie-hellman-keys)
-   [<span data-ttu-id="8c2d4-105">Intercambio de claves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="8c2d4-105">Exchanging Diffie-Hellman Keys</span></span>](#exchanging-diffie-hellman-keys)
-   [<span data-ttu-id="8c2d4-106">Exportar una clave privada Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="8c2d4-106">Exporting a Diffie-Hellman Private Key</span></span>](#exporting-a-diffie-hellman-private-key)
-   [<span data-ttu-id="8c2d4-107">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c2d4-107">Example Code</span></span>](#example-code)

## <a name="generating-diffie-hellman-keys"></a><span data-ttu-id="8c2d4-108">Generar claves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="8c2d4-108">Generating Diffie-Hellman Keys</span></span>

<span data-ttu-id="8c2d4-109">Para generar una clave de Diffie-Hellman, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8c2d4-109">To generate a Diffie-Hellman key, perform the following steps:</span></span>

1.  <span data-ttu-id="8c2d4-110">Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-110">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="8c2d4-111">Genere la nueva clave.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-111">Generate the new key.</span></span> <span data-ttu-id="8c2d4-112">Hay dos maneras de lograrlo: Si tiene CryptoAPI, debe generar todos los valores nuevos para G, P y X, o bien usar los valores existentes para G y P, y generar un nuevo valor para X.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-112">There are two ways to accomplish this—by having CryptoAPI generate all new values for G, P, and X or by using existing values for G and P, and generating a new value for X.</span></span>

    <span data-ttu-id="8c2d4-113">**Para generar la clave generando todos los valores nuevos**</span><span class="sxs-lookup"><span data-stu-id="8c2d4-113">**To generate the key by generating all new values**</span></span>

    1.  <span data-ttu-id="8c2d4-114">Llame a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , pasando **CALG \_ DH \_ SF** (almacenar y reenviar) o **CALG \_ DH \_ EPHEM** (efímero) en el parámetro *algid* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-114">Call the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function, passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter.</span></span> <span data-ttu-id="8c2d4-115">La clave se generará con nuevos valores aleatorios para G y P, un valor calculado recientemente para X y su identificador se devolverá en el parámetro *phKey* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-115">The key will be generated using new, random values for G and P, a newly calculated value for X, and its handle will be returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="8c2d4-116">La nueva clave ya está lista para su uso.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-116">The new key is now ready for use.</span></span> <span data-ttu-id="8c2d4-117">Los valores de G y P deben enviarse al destinatario junto con la clave (o enviados por algún otro método) al realizar un [*intercambio de claves*](../secgloss/e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8c2d4-117">The values of G and P must be sent to the recipient along with the key (or sent by some other method) when doing a [*key exchange*](../secgloss/e-gly.md).</span></span>

    <span data-ttu-id="8c2d4-118">**Para generar la clave con valores predefinidos para G y P**</span><span class="sxs-lookup"><span data-stu-id="8c2d4-118">**To generate the key by using predefined values for G and P**</span></span>

    1.  <span data-ttu-id="8c2d4-119">Llame [**a CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pasando **CALG \_ DH \_ SF** (almacenar y reenviar) o **CALG \_ DH \_ EPHEM** (efímero) en el parámetro *algid* y **CRYPT \_ PREGEN** para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-119">Call [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter and **CRYPT\_PREGEN** for the *dwFlags* parameter.</span></span> <span data-ttu-id="8c2d4-120">Se generará un identificador de clave y se devolverá en el parámetro *phKey* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-120">A key handle will be generated and returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="8c2d4-121">Inicialice una estructura de [**\_ \_ BLOB de datos de cifrado**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con el miembro **PbData** establecido en el valor P.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-121">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the P value.</span></span> <span data-ttu-id="8c2d4-122">El [*BLOB*](../secgloss/b-gly.md) no contiene información de encabezado y el miembro **pbData** está en formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-122">The [*BLOB*](../secgloss/b-gly.md) contains no header information and the **pbData** member is in [*little-endian*](../secgloss/l-gly.md) format.</span></span>
    3.  <span data-ttu-id="8c2d4-123">El valor de P se establece mediante una llamada a la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , pasando el identificador de clave recuperado en el paso a en el parámetro *hKey* , la marca de **KP \_ P** en el parámetro *dwParam* y un puntero a la estructura que contiene el valor de P en el parámetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-123">The value of P is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_P** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of P in the *pbData* parameter.</span></span>
    4.  <span data-ttu-id="8c2d4-124">Inicialice una estructura de [**\_ \_ BLOB de datos de cifrado**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) con el miembro **PbData** establecido en el valor G.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-124">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the G value.</span></span> <span data-ttu-id="8c2d4-125">El BLOB no contiene información de encabezado y el miembro **pbData** está en formato Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-125">The BLOB contains no header information and the **pbData** member is in little-endian format.</span></span>
    5.  <span data-ttu-id="8c2d4-126">El valor de G se establece mediante una llamada a la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , pasando el identificador de clave recuperado en el paso a en el parámetro *hKey* , la marca de **KP \_ G** en el parámetro *dwParam* y un puntero a la estructura que contiene el valor de G en el parámetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-126">The value of G is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_G** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of G in the *pbData* parameter.</span></span>
    6.  <span data-ttu-id="8c2d4-127">El valor de X se genera mediante una llamada a la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , pasando el identificador de clave recuperado en el paso a en el parámetro *hKey* , la marca de **KP \_ X** en el parámetro *dwParam* y **null** en el parámetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-127">The value of X is generated by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_X** flag in the *dwParam* parameter, and **NULL** in the *pbData* parameter.</span></span>
    7.  <span data-ttu-id="8c2d4-128">Si todas las llamadas de función se realizaron correctamente, la clave pública Diffie-Hellman está lista para su uso.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-128">If all the function calls succeeded, the Diffie-Hellman public key is ready for use.</span></span>

3.  <span data-ttu-id="8c2d4-129">Cuando ya no se necesite la clave, debe destruirla pasando el identificador de la clave a la función [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-129">When the key is no longer needed, destroy it by passing the key handle to the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

<span data-ttu-id="8c2d4-130">Si se especificó **CALG \_ DH \_ SF** en los procedimientos anteriores, los valores de clave se conservan en el almacenamiento con cada llamada a [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="8c2d4-130">If **CALG\_DH\_SF** was specified in the previous procedures, the key values are persisted to storage with each call to [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span></span> <span data-ttu-id="8c2d4-131">Los valores G y P se pueden recuperar mediante la función [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-131">The G and P values can then be retrieved by using the [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) function.</span></span> <span data-ttu-id="8c2d4-132">Algunos CSP pueden tener valores G y P codificados de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-132">Some CSPs may have hard-coded G and P values.</span></span> <span data-ttu-id="8c2d4-133">En este caso, se devolverá un error de **NTE \_ FIXEDPARAMETER** si se llama a **CryptSetKeyParam** con **KP \_ G** o **KP \_ P** especificados en el parámetro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-133">In this case a **NTE\_FIXEDPARAMETER** error will be returned if **CryptSetKeyParam** is called with **KP\_G** or **KP\_P** specified in the *dwParam* parameter.</span></span> <span data-ttu-id="8c2d4-134">Si se llama a **CryptDestroyKey** , se destruye el identificador de la clave, pero los valores de clave se conservan en el CSP.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-134">If **CryptDestroyKey** is called, the handle to the key is destroyed, but the key values are retained in the CSP.</span></span> <span data-ttu-id="8c2d4-135">Sin embargo, si se especificó **CALG \_ DH \_ EPHEM** , se destruye el identificador de la clave y se borran todos los valores del CSP.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-135">However, if **CALG\_DH\_EPHEM** was specified, the handle to the key is destroyed, and all values are cleared from the CSP.</span></span>

## <a name="exchanging-diffie-hellman-keys"></a><span data-ttu-id="8c2d4-136">Intercambio de claves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="8c2d4-136">Exchanging Diffie-Hellman Keys</span></span>

<span data-ttu-id="8c2d4-137">El propósito del algoritmo Diffie-Hellman es hacer posible que dos o más entidades creen y compartan una clave de sesión secreta idéntica compartiendo información a través de una red que no es segura.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-137">The purpose of the Diffie-Hellman algorithm is to make it possible for two or more parties to create and share an identical, secret session key by sharing information over a network that is not secure.</span></span> <span data-ttu-id="8c2d4-138">La información que se comparte a través de la red está en forma de un par de valores constantes y una Diffie-Hellman clave pública.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-138">The information that gets shared over the network is in the form of a couple of constant values and a Diffie-Hellman public key.</span></span> <span data-ttu-id="8c2d4-139">El proceso que usan dos entidades de intercambio de claves es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="8c2d4-139">The process used by two key-exchange parties is as follows:</span></span>

-   <span data-ttu-id="8c2d4-140">Ambas partes aceptan el Diffie-Hellman parámetros, que son un número primo (P) y un número de generador (G).</span><span class="sxs-lookup"><span data-stu-id="8c2d4-140">Both parties agree to the Diffie-Hellman parameters which are a prime number (P) and a generator number (G).</span></span>
-   <span data-ttu-id="8c2d4-141">La entidad 1 envía su clave pública Diffie-Hellman a la entidad 2.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-141">Party 1 sends its Diffie-Hellman public key to party 2.</span></span>
-   <span data-ttu-id="8c2d4-142">La entidad 2 calcula la clave de sesión secreta usando la información contenida en la clave privada y la clave pública de la entidad 1.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-142">Party 2 computes the secret session key by using the information contained in its private key and party 1's public key.</span></span>
-   <span data-ttu-id="8c2d4-143">La entidad 2 envía su clave pública Diffie-Hellman a la entidad 1.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-143">Party 2 sends its Diffie-Hellman public key to party 1.</span></span>
-   <span data-ttu-id="8c2d4-144">La entidad 1 calcula la clave de sesión secreta mediante la información contenida en su clave privada y la clave pública de la entidad 2.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-144">Party 1 computes the secret session key by using the information contained in its private key and party 2's public key.</span></span>
-   <span data-ttu-id="8c2d4-145">Ambas partes tienen ahora la misma clave de sesión, que se puede usar para cifrar y descifrar los datos.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-145">Both parties now have the same session key, which can be used for encrypting and decrypting data.</span></span> <span data-ttu-id="8c2d4-146">Los pasos necesarios para ello se muestran en el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-146">The steps necessary for this are shown in the following procedure.</span></span>

<span data-ttu-id="8c2d4-147">**Para preparar una clave pública de Diffie-Hellman para la transmisión**</span><span class="sxs-lookup"><span data-stu-id="8c2d4-147">**To prepare a Diffie-Hellman public key for transmission**</span></span>

1.  <span data-ttu-id="8c2d4-148">Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-148">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="8c2d4-149">Cree una clave de Diffie-Hellman llamando a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para crear una nueva clave o llamando a la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar una clave existente.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-149">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="8c2d4-150">Obtiene el tamaño necesario para contener el BLOB de clave Diffie-Hellman llamando a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), pasando **null** para el parámetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-150">Get the size needed to hold the Diffie-Hellman key BLOB by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passing **NULL** for the *pbData* parameter.</span></span> <span data-ttu-id="8c2d4-151">El tamaño necesario se devolverá en *pdwDataLen*.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-151">The required size will be returned in *pdwDataLen*.</span></span>
4.  <span data-ttu-id="8c2d4-152">Asigne memoria para el BLOB de clave.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-152">Allocate memory for the key BLOB.</span></span>
5.  <span data-ttu-id="8c2d4-153">Cree un [*BLOB de clave pública*](../secgloss/p-gly.md) Diffie-Hellman llamando a la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , pasando **PUBLICKEYBLOB** en el parámetro *dwBlobType* y el identificador a la clave de Diffie-Hellman en el parámetro *hKey* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-153">Create a Diffie-Hellman [*public key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PUBLICKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span> <span data-ttu-id="8c2d4-154">Esta llamada de función provoca el cálculo del valor de clave pública (G ^ X) mod P.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-154">This function call causes the calculation of the public key value, (G^X) mod P.</span></span>
6.  <span data-ttu-id="8c2d4-155">Si todas las llamadas de función anteriores se realizaron correctamente, el BLOB de clave pública de Diffie-Hellman ya está listo para su codificación y transmisión.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-155">If all the preceding function calls were successful, the Diffie-Hellman public key BLOB is now ready to be encoded and transmitted.</span></span>

<span data-ttu-id="8c2d4-156">**Para importar una clave pública Diffie-Hellman y calcular la clave de sesión secreta**</span><span class="sxs-lookup"><span data-stu-id="8c2d4-156">**To import a Diffie-Hellman public key and calculate the secret session key**</span></span>

1.  <span data-ttu-id="8c2d4-157">Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-157">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="8c2d4-158">Cree una clave de Diffie-Hellman llamando a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para crear una nueva clave o llamando a la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar una clave existente.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-158">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="8c2d4-159">Para importar la clave pública de Diffie-Hellman en el CSP, llame a la función [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , pasando un puntero al BLOB de clave pública en el parámetro *pbData* , la longitud del BLOB en el parámetro *dwDataLen* y el identificador de la clave de Diffie-Hellman en el parámetro *hPubKey* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-159">To import the Diffie-Hellman public key into the CSP, call the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function, passing a pointer to the public key BLOB in the *pbData* parameter, the length of the BLOB in the *dwDataLen* parameter, and the handle to the Diffie-Hellman key in the *hPubKey* parameter.</span></span> <span data-ttu-id="8c2d4-160">Esto hace que se realice el cálculo (Y ^ X) mod P, con lo que se crea la clave secreta compartida y se completa el [*intercambio de claves*](../secgloss/e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8c2d4-160">This causes the calculation, (Y^X) mod P, to be performed, thus creating the shared, secret key and completing the [*key exchange*](../secgloss/e-gly.md).</span></span> <span data-ttu-id="8c2d4-161">Esta llamada de función devuelve un identificador para la nueva clave de sesión secreta en el parámetro *hKey* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-161">This function call returns a handle to the new, secret, session key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="8c2d4-162">En este punto, la Diffie-Hellman importada es de tipo **CALG \_ AGREEDKEY \_ any**.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-162">At this point, the imported Diffie-Hellman is of type **CALG\_AGREEDKEY\_ANY**.</span></span> <span data-ttu-id="8c2d4-163">Antes de que se pueda usar la clave, debe convertirse en un tipo de clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-163">Before the key can be used, it must be converted into a session key type.</span></span> <span data-ttu-id="8c2d4-164">Esto se logra mediante una llamada a la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con *DwParam* establecida en **KP \_ ALGID** y con *pbData* establecido en un puntero a un valor de [**\_ identificador de alg**](alg-id.md) que representa una clave de sesión, como **CALG \_ RC4**.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-164">This is accomplished by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function with *dwParam* set to **KP\_ALGID** and with *pbData* set to a pointer to a [**ALG\_ID**](alg-id.md) value that represents a session key, such as **CALG\_RC4**.</span></span> <span data-ttu-id="8c2d4-165">La clave se debe convertir antes de usar la clave compartida en la función [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) o [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-165">The key must be converted before using the shared key in the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) or [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span> <span data-ttu-id="8c2d4-166">Se producirá un error en las llamadas realizadas a cualquiera de estas funciones antes de convertir el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-166">Calls made to either of these functions prior to converting the key type will fail.</span></span>
5.  <span data-ttu-id="8c2d4-167">La clave de sesión secreta ahora está lista para usarse para el cifrado o el descifrado.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-167">The secret session key is now ready to be used for encryption or decryption.</span></span>
6.  <span data-ttu-id="8c2d4-168">Cuando la clave ya no sea necesaria, destruya el identificador de clave mediante una llamada a la función [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-168">When the key is no longer needed, destroy the key handle by calling the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

## <a name="exporting-a-diffie-hellman-private-key"></a><span data-ttu-id="8c2d4-169">Exportar una clave privada Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="8c2d4-169">Exporting a Diffie-Hellman Private Key</span></span>

<span data-ttu-id="8c2d4-170">Para exportar una clave privada Diffie-Hellman, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8c2d4-170">To export a Diffie-Hellman private key, perform the following steps:</span></span>

1.  <span data-ttu-id="8c2d4-171">Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-171">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="8c2d4-172">Cree una clave de Diffie-Hellman llamando a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para crear una nueva clave o llamando a la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar una clave existente.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-172">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="8c2d4-173">Cree un [*BLOB de clave privada*](../secgloss/p-gly.md) Diffie-Hellman llamando a la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , pasando **PRIVATEKEYBLOB** en el parámetro *dwBlobType* y el identificador a la clave de Diffie-Hellman en el parámetro *hKey* .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-173">Create a Diffie-Hellman [*private key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PRIVATEKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="8c2d4-174">Cuando el identificador de clave ya no sea necesario, llame a la función [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) para destruir el identificador de clave.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-174">When the key handle is no longer needed, call the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function to destroy the key handle.</span></span>

## <a name="example-code"></a><span data-ttu-id="8c2d4-175">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c2d4-175">Example Code</span></span>

<span data-ttu-id="8c2d4-176">En el ejemplo siguiente se muestra cómo crear, exportar, importar y usar una clave de Diffie-Hellman para realizar un intercambio de claves.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-176">The following example shows how to create, export, import, and use a Diffie-Hellman key to perform a key exchange.</span></span>


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
