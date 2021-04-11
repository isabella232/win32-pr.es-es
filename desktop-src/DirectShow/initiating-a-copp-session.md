---
description: Iniciar una sesión de COPP
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: Iniciar una sesión de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d64ef848874aee95d3f928a5b8bb637323a92a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152524"
---
# <a name="initiating-a-copp-session"></a><span data-ttu-id="09ee8-103">Iniciar una sesión de COPP</span><span class="sxs-lookup"><span data-stu-id="09ee8-103">Initiating a COPP Session</span></span>

<span data-ttu-id="09ee8-104">Para iniciar una sesión de protocolo de protección de salida (COPP) certificada, debe preparar una *firma*, que es una matriz que contiene la concatenación de los números siguientes:</span><span class="sxs-lookup"><span data-stu-id="09ee8-104">To initiate a Certified Output Protection Protocol (COPP) session, you must prepare a *signature*, which is an array that contains the concatenation of the following numbers:</span></span>

-   <span data-ttu-id="09ee8-105">Número aleatorio de 128 bits devuelto por el controlador.</span><span class="sxs-lookup"><span data-stu-id="09ee8-105">The 128-bit random number returned by the driver.</span></span> <span data-ttu-id="09ee8-106">(Este valor se muestra como *guidRandom* en [la obtención de la cadena de certificados del controlador](obtaining-the-drivers-certificate-chain.md)).</span><span class="sxs-lookup"><span data-stu-id="09ee8-106">(This value is shown as *guidRandom* in [Obtaining the Driver's Certificate Chain](obtaining-the-drivers-certificate-chain.md).)</span></span>
-   <span data-ttu-id="09ee8-107">Una clave AES simétrica de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="09ee8-107">A 128-bit symmetric AES key.</span></span>
-   <span data-ttu-id="09ee8-108">Un número de secuencia inicial de 32 bits para solicitudes de estado.</span><span class="sxs-lookup"><span data-stu-id="09ee8-108">A 32-bit starting sequence number for status requests.</span></span>
-   <span data-ttu-id="09ee8-109">Un número de secuencia inicial de 32 bits para los comandos COPP.</span><span class="sxs-lookup"><span data-stu-id="09ee8-109">A 32-bit starting sequence number for COPP commands.</span></span>

<span data-ttu-id="09ee8-110">Genere una clave AES simétrica como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="09ee8-110">Generate a symmetric AES key as follows:</span></span>


```C++
DWORD dwFlag = 0x80;         // Bit length: 128-bit AES.
dwFlag <<= 16;               // Move this value to the upper 16 bits.
dwFlag |= CRYPT_EXPORTABLE;  // We want to export the key.
CryptGenKey(
    hCSP,           // Handle to the CSP.
    CALG_AES_128,   // Use 128-bit AES block encryption algorithm.
    dwFlag,
    &m_hAESKey      // Receives a handle to the AES key.
);
```



<span data-ttu-id="09ee8-111">La función **CryptGenKey** crea la clave simétrica, pero la clave todavía se mantiene en el CSP.</span><span class="sxs-lookup"><span data-stu-id="09ee8-111">The **CryptGenKey** function creates the symmetric key, but the key is still held in the CSP.</span></span> <span data-ttu-id="09ee8-112">Para exportar la clave a una matriz de bytes, utilice la función **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="09ee8-112">To export the key into a byte array, use the **CryptExportKey** function.</span></span> <span data-ttu-id="09ee8-113">Este es el motivo por el que se usa la marca de CIFRAdo \_ EXportable cuando se llama a **CryptGenKey**.</span><span class="sxs-lookup"><span data-stu-id="09ee8-113">This is the reason for using the CRYPT\_EXPORTABLE flag when calling **CryptGenKey**.</span></span> <span data-ttu-id="09ee8-114">El código siguiente exporta la clave y la copia en el</span><span class="sxs-lookup"><span data-stu-id="09ee8-114">The following code exports the key and copies it into the</span></span>


```
pData
```



<span data-ttu-id="09ee8-115">.</span><span class="sxs-lookup"><span data-stu-id="09ee8-115">array.</span></span>


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



<span data-ttu-id="09ee8-116">Los datos devueltos en</span><span class="sxs-lookup"><span data-stu-id="09ee8-116">The data returned in</span></span>


```
pData
```



<span data-ttu-id="09ee8-117">tiene el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="09ee8-117">has the following layout:</span></span>


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



<span data-ttu-id="09ee8-118">Sin embargo, no se define ninguna estructura que coincida con este diseño en los encabezados de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="09ee8-118">However, no structure that matches this layout is defined in the CryptoAPI headers.</span></span> <span data-ttu-id="09ee8-119">Puede definir una o varias operaciones aritméticas de punteros.</span><span class="sxs-lookup"><span data-stu-id="09ee8-119">You can either define one or do some pointer arithmetic.</span></span> <span data-ttu-id="09ee8-120">Por ejemplo, para comprobar el tamaño de la clave:</span><span class="sxs-lookup"><span data-stu-id="09ee8-120">For example, to verify the size of the key:</span></span>


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



<span data-ttu-id="09ee8-121">Para obtener el puntero a la propia clave:</span><span class="sxs-lookup"><span data-stu-id="09ee8-121">To get the pointer to the key itself:</span></span>


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



<span data-ttu-id="09ee8-122">A continuación, genere un número aleatorio de 32 bits para usarlo como secuencia inicial para solicitudes de estado de COPP.</span><span class="sxs-lookup"><span data-stu-id="09ee8-122">Next, generate a 32-bit random number to use as the starting sequence for COPP status requests.</span></span> <span data-ttu-id="09ee8-123">La manera recomendada de crear un número aleatorio es llamar a la función **CryptGenRandom** .</span><span class="sxs-lookup"><span data-stu-id="09ee8-123">The recommended way to create a random number is to call the **CryptGenRandom** function.</span></span> <span data-ttu-id="09ee8-124">No utilice la función **Rand** en la biblioteca en tiempo de ejecución de C, ya que no es realmente aleatoria.</span><span class="sxs-lookup"><span data-stu-id="09ee8-124">Do not use the **rand** function in the C run-time library, because it is not truly random.</span></span> <span data-ttu-id="09ee8-125">Genere un segundo número aleatorio de 32 bits para usarlo como secuencia inicial para los comandos COPP.</span><span class="sxs-lookup"><span data-stu-id="09ee8-125">Generate a second 32-bit random number to use as the starting sequence for COPP commands.</span></span>


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



<span data-ttu-id="09ee8-126">Ahora puede preparar la firma de COPP.</span><span class="sxs-lookup"><span data-stu-id="09ee8-126">Now you can prepare the COPP signature.</span></span> <span data-ttu-id="09ee8-127">Se trata de una matriz de 256 bytes, definida como la estructura [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) .</span><span class="sxs-lookup"><span data-stu-id="09ee8-127">This is a 256-byte array, defined as the [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) structure.</span></span> <span data-ttu-id="09ee8-128">Inicialice el contenido de la matriz en cero.</span><span class="sxs-lookup"><span data-stu-id="09ee8-128">Initialize the contents of the array to zero.</span></span> <span data-ttu-id="09ee8-129">A continuación, copie los cuatro números en la matriz: el número aleatorio del controlador, la clave AES, el número de secuencia de estado y el número de secuencia de comandos, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="09ee8-129">Then copy the four numbers into the array—the driver's random number, the AES key, the status sequence number, and the command sequence number, in that order.</span></span> <span data-ttu-id="09ee8-130">Por último, intercambie el orden de bytes de toda la matriz.</span><span class="sxs-lookup"><span data-stu-id="09ee8-130">Finally, swap the byte order of the entire array.</span></span>

<span data-ttu-id="09ee8-131">Según la documentación de **CryptEncrypt**:</span><span class="sxs-lookup"><span data-stu-id="09ee8-131">According to the documentation for **CryptEncrypt**:</span></span>

<dl> <span data-ttu-id="09ee8-132">"La longitud de los datos de texto sin formato que se pueden cifrar con una llamada a **CryptEncrypt** con una clave RSA es la longitud del módulo de claves menos once bytes.</span><span class="sxs-lookup"><span data-stu-id="09ee8-132">"The length of plaintext data that can be encrypted with a call to **CryptEncrypt** with an RSA key is the length of the key modulus minus eleven bytes.</span></span> <span data-ttu-id="09ee8-133">Los once bytes son el mínimo elegido para el \# relleno PKCS 1. "</span><span class="sxs-lookup"><span data-stu-id="09ee8-133">The eleven bytes is the chosen minimum for PKCS \#1 padding."</span></span>  
</dl>

<span data-ttu-id="09ee8-134">En este caso, el módulo es de 256 bytes, por lo que la longitud máxima del mensaje es de 245 bytes (256 – 11).</span><span class="sxs-lookup"><span data-stu-id="09ee8-134">In this case, the modulus is 256 bytes, so the maximum message length is 245 bytes (256 – 11).</span></span> <span data-ttu-id="09ee8-135">La estructura **AMCOPPSignature** es 256 bytes, pero los datos significativos de la firma son solo de 40 bytes.</span><span class="sxs-lookup"><span data-stu-id="09ee8-135">The **AMCOPPSignature** structure is 256 bytes, but the meaningful data in the signature is only 40 bytes.</span></span> <span data-ttu-id="09ee8-136">En el código siguiente se cifra la firma y se proporciona el resultado en</span><span class="sxs-lookup"><span data-stu-id="09ee8-136">The following code encrypts the signature and provides the result in</span></span>


```
CoppSig
```



<span data-ttu-id="09ee8-137">.</span><span class="sxs-lookup"><span data-stu-id="09ee8-137">.</span></span>


```C++
AMCOPPSignature CoppSig;
ZeroMemory(&CoppSig, sizeof(CoppSig));
// Copy the signature data into CoppSig. (Not shown.)

// Encrypt the signature:
const DWORD RSA_PADDING = 11;    // 11-byte padding.
DWORD cbDataOut = sizeof(AMCOPPSignature);
DWORD cbDataIn = cbDataOut - RSA_PADDING;
CryptEncrypt(
    hRSAKey, 
    NULL,     // No hash object.
    TRUE,     // Final block to encrypt.
    0,        // Reserved.
    &CoppSig, // COPP signature.
    &cbDataOut, 
    cbDataIn
);
```



<span data-ttu-id="09ee8-138">Ahora pase la matriz cifrada a [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span><span class="sxs-lookup"><span data-stu-id="09ee8-138">Now pass the encrypted array to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span></span>


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



<span data-ttu-id="09ee8-139">Si este método se ejecuta correctamente, está listo para enviar comandos COPP y solicitudes de estado al controlador.</span><span class="sxs-lookup"><span data-stu-id="09ee8-139">If this method succeeds, you are ready to send COPP commands and status requests to the driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09ee8-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09ee8-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09ee8-141">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="09ee8-141">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



