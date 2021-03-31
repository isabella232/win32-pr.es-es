---
description: En este tema se describe cómo comprobar que el sistema admite un método de síntesis.
ms.assetid: dd1b53cd-66b9-46b3-89ad-ee84b4690e1e
title: Comprobar que el sistema admite un método de síntesis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acf3e0c2c7f4927fc6047c88039e443e2db3e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912633"
---
# <a name="verify-the-system-supports-a-digest-method"></a><span data-ttu-id="a8929-103">Comprobar que el sistema admite un método de síntesis</span><span class="sxs-lookup"><span data-stu-id="a8929-103">Verify the System Supports a Digest Method</span></span>

<span data-ttu-id="a8929-104">En este tema se describe cómo comprobar que el sistema admite un método de síntesis.</span><span class="sxs-lookup"><span data-stu-id="a8929-104">This topic describes how to verify that the system supports a digest method.</span></span>

<span data-ttu-id="a8929-105">Las firmas digitales XPS usan la API de cifrado, que proporciona métodos para comprobar que el sistema admite un método de síntesis específico.</span><span class="sxs-lookup"><span data-stu-id="a8929-105">XPS Digital Signatures use the Crypto API, which provides methods for verifying that the system supports a specific digest method.</span></span> <span data-ttu-id="a8929-106">Para usar la función **CryptXmlEnumAlgorithmInfo** de la API de Crypto con el fin de enumerar los métodos de síntesis admitidos por el sistema, el llamador debe proporcionar un método de devolución de llamada y una estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="a8929-106">To use the Crypto API's **CryptXmlEnumAlgorithmInfo** function to enumerate the digest methods that are supported by the system, the caller must provide a callback method and a data structure.</span></span> <span data-ttu-id="a8929-107">La función **CryptXmlEnumAlgorithmInfo** devuelve los datos de la enumeración al llamador mediante el método de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a8929-107">The **CryptXmlEnumAlgorithmInfo** function passes the enumeration data back to the caller by way of the callback method.</span></span>

<span data-ttu-id="a8929-108">La estructura de datos usada en este ejemplo se muestra en el ejemplo de código siguiente y contiene los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="a8929-108">The data structure used in this example is shown in the following code example and contains the following fields:</span></span>

| <span data-ttu-id="a8929-109">Campo</span><span class="sxs-lookup"><span data-stu-id="a8929-109">Field</span></span>                            | <span data-ttu-id="a8929-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8929-110">Description</span></span>                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8929-111">**userDigestAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="a8929-111">**userDigestAlgorithm**</span></span>          | <span data-ttu-id="a8929-112">Un campo **LPWStr** que apunta a la cadena que contiene el URI del algoritmo de resumen que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="a8929-112">An **LPWSTR** field that points to the string that contains the URI of the digest algorithm to be checked.</span></span> |
| <span data-ttu-id="a8929-113">**userDigestAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="a8929-113">**userDigestAlgorithmSupported**</span></span> | <span data-ttu-id="a8929-114">Un valor **booleano** que indica si el algoritmo de síntesis es compatible con el certificado.</span><span class="sxs-lookup"><span data-stu-id="a8929-114">A **Boolean** value that indicates whether the digest algorithm is supported by the certificate.</span></span>           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



<span data-ttu-id="a8929-115">El método de la API de cifrado que enumera los métodos de síntesis utiliza un método de devolución de llamada para devolver datos al llamador.</span><span class="sxs-lookup"><span data-stu-id="a8929-115">The Crypto API method that enumerates the digest methods uses a callback method to return data to the caller.</span></span> <span data-ttu-id="a8929-116">**CryptXmlEnumAlgorithmInfo** enumera los métodos de síntesis que admite el sistema y llama al método de devolución de llamada para cada método de síntesis que enumera, hasta que el método de devolución de llamada devuelve **false** o hasta que se enumeran todos los métodos de síntesis admitidos por el sistema.</span><span class="sxs-lookup"><span data-stu-id="a8929-116">**CryptXmlEnumAlgorithmInfo** enumerates the digest methods that are supported by the system, and it calls the callback method for each digest method that it enumerates, until the callback method returns **FALSE** or until all digest methods supported by the system are enumerated.</span></span> <span data-ttu-id="a8929-117">En este ejemplo, el método de devolución de llamada compara el método de síntesis que **CryptXmlEnumAlgorithmInfo** pasa con el método de síntesis proporcionado por el método de llamada.</span><span class="sxs-lookup"><span data-stu-id="a8929-117">The callback method in this example compares the digest method that is passed in by **CryptXmlEnumAlgorithmInfo** with the digest method provided by the calling method.</span></span>


```C++
BOOL WINAPI 
EnumDigestMethodCallback (
    __in   const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt  void                     *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, consider
    // setting this value dynamically.
    static const  size_t MAX_ALG_ID_LEN = 128;
    DigestMethodData   *certificateAlgorithmData = 
        (DigestMethodData*)userArg;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (DigestMethodData*)userArg;
    } else {
        // Unable to continue this enumeration without 
        //  data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see 
    //  if the URI of the current supported algorithm matches 
    //  the URI passed in userArg.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userDigestAlgorithm, 
        MAX_ALG_ID_LEN );

    if ( 0 == cmpResult )
    {
        // This is a match...
        //  set supported value to true
        certificateAlgorithmData->userDigestAlgorithmSupported = TRUE;
        //  ...and return FALSE to stop any further enumeration
        return FALSE;
    } 
    else
    {
        // no match was found
        // return TRUE to continue enumeration
        return TRUE;
    }
}
```



<span data-ttu-id="a8929-118">En el ejemplo de código siguiente se incluye la funcionalidad de validación en un único método, que devuelve un valor **booleano** que indica si el sistema admite el método de síntesis.</span><span class="sxs-lookup"><span data-stu-id="a8929-118">The following code sample wraps the validation functionality into a single method, which returns a **Boolean** value that indicates whether the system supports the digest method.</span></span>


```C++
BOOL 
SupportsDigestAlgorithm (
    __in LPCWSTR digestMethodToCheck
)
{
    HRESULT  hr = S_OK;

    // Initialize the structure that will hold information about the 
    //  digest method to check
    DigestMethodData  certificateAlgorithmData;

    certificateAlgorithmData.userDigestAlgorithmSupported = FALSE;
    certificateAlgorithmData.userDigestAlgorithm = digestMethodToCheck;

    // Enumerate the algorithms that are supported on the system, 
    //  the callback method compares each supported algorithm to the one
    //  passed in digestMethodToCheck and returns true in the
    //  certificateAlgorithmData.userDigestAlgorithmSupported field if
    //  the provided digest algorithm is supported by system.
    //
    // Note that CRYPT_XML_GROUP_ID_HASH is set to enumerate 
    //  digest methods
    hr = CryptXmlEnumAlgorithmInfo(
        CRYPT_XML_GROUP_ID_HASH,       // NOTE: CRYPT_XML_GROUP_ID_HASH
        CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
        (void*)&certificateAlgorithmData,
        EnumDigestMethodCallback);

    return certificateAlgorithmData.userDigestAlgorithmSupported;
}
```



## <a name="related-topics"></a><span data-ttu-id="a8929-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8929-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a8929-120">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="a8929-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="a8929-121">Cargar un certificado desde un archivo</span><span class="sxs-lookup"><span data-stu-id="a8929-121">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="a8929-122">Comprobar que un certificado admite un método de firma</span><span class="sxs-lookup"><span data-stu-id="a8929-122">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="a8929-123">Insertar cadenas de certificado en un documento</span><span class="sxs-lookup"><span data-stu-id="a8929-123">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="a8929-124">**Se usa en este ejemplo**</span><span class="sxs-lookup"><span data-stu-id="a8929-124">**Used in This Example**</span></span>
</dt> <dt>

<span data-ttu-id="a8929-125">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="a8929-125">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="a8929-126">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="a8929-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="a8929-127">API de criptografía</span><span class="sxs-lookup"><span data-stu-id="a8929-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="a8929-128">Funciones de criptografía</span><span class="sxs-lookup"><span data-stu-id="a8929-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="a8929-129">Errores de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="a8929-129">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="a8929-130">Errores de documento XPS</span><span class="sxs-lookup"><span data-stu-id="a8929-130">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="a8929-131">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="a8929-131">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
