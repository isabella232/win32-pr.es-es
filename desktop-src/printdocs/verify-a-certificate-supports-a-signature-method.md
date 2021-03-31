---
description: En este tema se describe cómo comprobar que un certificado admite un método de firma específico.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Comprobar que un certificado admite un método de firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27da9ae31c3cf0c4e453a5507d93d1505606e859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912630"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a><span data-ttu-id="b453a-103">Comprobar que un certificado admite un método de firma</span><span class="sxs-lookup"><span data-stu-id="b453a-103">Verify That a Certificate Supports a Signature Method</span></span>

<span data-ttu-id="b453a-104">En este tema se describe cómo comprobar que un certificado admite un método de firma específico.</span><span class="sxs-lookup"><span data-stu-id="b453a-104">This topic describes how to verify that a certificate supports a specific signature method.</span></span>

<span data-ttu-id="b453a-105">El **CryptXmlEnumAlgorithmInfo** de Microsoft Crypto API enumera las propiedades de un certificado y se usa en este ejemplo de código para enumerar los métodos de firma que admite el certificado.</span><span class="sxs-lookup"><span data-stu-id="b453a-105">The **CryptXmlEnumAlgorithmInfo** in the Microsoft Crypto API enumerates the properties of a certificate and is used in this code example to enumerate the signature methods that the certificate supports.</span></span> <span data-ttu-id="b453a-106">Para usar **CryptXmlEnumAlgorithmInfo** con el fin de enumerar los métodos de firma que admite el certificado, el llamador debe proporcionar un método de devolución de llamada y una estructura de datos en la llamada a **CryptXmlEnumAlgorithmInfo**, lo que permite pasar datos al método de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b453a-106">To use **CryptXmlEnumAlgorithmInfo** to enumerate the signature methods that the certificate supports, the caller must provide a callback method and a data structure in the call to **CryptXmlEnumAlgorithmInfo**, allowing it to pass data to the callback method.</span></span>

<span data-ttu-id="b453a-107">La estructura de datos utilizada en el siguiente ejemplo de código tiene los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="b453a-107">The data structure used in the next code example has the following fields:</span></span>

| <span data-ttu-id="b453a-108">Campo</span><span class="sxs-lookup"><span data-stu-id="b453a-108">Field</span></span>                               | <span data-ttu-id="b453a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b453a-109">Description</span></span>                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b453a-110">**userSignatureAlgorithmToCheck**</span><span class="sxs-lookup"><span data-stu-id="b453a-110">**userSignatureAlgorithmToCheck**</span></span>   | <span data-ttu-id="b453a-111">Un campo **LPWStr** que apunta a la cadena que contiene el URI del algoritmo de firma que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="b453a-111">An **LPWSTR** field that points to the string that contains the URI of the signature algorithm to be checked.</span></span>                             |
| <span data-ttu-id="b453a-112">**certificateAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="b453a-112">**certificateAlgorithmInfo**</span></span>        | <span data-ttu-id="b453a-113">Puntero a una estructura **de \_ \_ información de OID de cifrado** que contiene información sobre un algoritmo de firma que es compatible con el certificado.</span><span class="sxs-lookup"><span data-stu-id="b453a-113">A pointer to a **CRYPT\_OID\_INFO** structure that contains information about a signature algorithm that is supported by the certificate.</span></span> |
| <span data-ttu-id="b453a-114">**userSignatureAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="b453a-114">**userSignatureAlgorithmSupported**</span></span> | <span data-ttu-id="b453a-115">Valor **booleano** que indica si el algoritmo de firma es compatible con el certificado.</span><span class="sxs-lookup"><span data-stu-id="b453a-115">A **Boolean** value that indicates whether the signature algorithm is supported by the certificate.</span></span>                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



<span data-ttu-id="b453a-116">El método Crypto API que comprueba el certificado usa un método de devolución de llamada para devolver datos al llamador.</span><span class="sxs-lookup"><span data-stu-id="b453a-116">The Crypto API method that checks the certificate uses a callback method to return data to the caller.</span></span> <span data-ttu-id="b453a-117">**CryptXmlEnumAlgorithmInfo** enumera los métodos de firma que admite el certificado y llama al método de devolución de llamada para cada método de firma hasta que el método de devolución de llamada devuelve **false** o hasta que se han enumerado todos los métodos de firma del certificado.</span><span class="sxs-lookup"><span data-stu-id="b453a-117">**CryptXmlEnumAlgorithmInfo** enumerates the signature methods that the certificate supports, and calls the callback method for each signature method until the callback method returns **FALSE** or until all signature methods in the certificate have been enumerated.</span></span>

<span data-ttu-id="b453a-118">El método de devolución de llamada en el siguiente ejemplo de código busca un método de firma pasado por **CryptXmlEnumAlgorithmInfo** que coincida con el método de firma proporcionado por el método de llamada.</span><span class="sxs-lookup"><span data-stu-id="b453a-118">The callback method in the next code example searches for a signature method passed in by **CryptXmlEnumAlgorithmInfo** that matches the signature method provided by the calling method.</span></span> <span data-ttu-id="b453a-119">Cuando se encuentra una coincidencia, el método de devolución de llamada comprueba si el sistema también admite el método de firma.</span><span class="sxs-lookup"><span data-stu-id="b453a-119">When a match is found, the callback method checks whether the signature method is also supported by the system.</span></span> <span data-ttu-id="b453a-120">Si los métodos de firma coinciden y son compatibles con el sistema, el método de firma se marca como compatible con el sistema y el método de devolución de llamada devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="b453a-120">If the signature methods match and are supported by the system, the signature method is marked as system-supported and the callback method returns **FALSE**.</span></span>


```C++
BOOL WINAPI 
EnumSignatureMethodCallback (
    __in const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt void *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, you might consider
    // setting this value dynamically.
    static const size_t MAX_ALG_ID_LEN = 128;
    SignatureMethodData *certificateAlgorithmData = NULL;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (SignatureMethodData*)userArg;
    } else {
        // Unable to continue this enumeration 
        //   without data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see if the URI 
    //  of the algorithm supported by the certificate matches the URI 
    //  of the algorithm being tested.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userSignatureAlgorithmToCheck, 
        MAX_ALG_ID_LEN );
    if ( 0 == cmpResult )
    {
        // This is a match...
        // Check to see if the algorithm supported by the 
        //  certificate matches any of the supported algorithms 
        //  on the system.
        cmpResult = wcsncmp(
            certMethodInfo->wszCNGExtraAlgid, 
            certificateAlgorithmData->certificateAlgorithmInfo->pwszCNGAlgid, 
            MAX_ALG_ID_LEN );
        if ( 0 == cmpResult )
        {
            // This is also a match so set the field in the data structure
            //   provided by the calling method.
            certificateAlgorithmData->userSignatureAlgorithmSupported = TRUE;
            // A match was found so there is no point in continuing 
            //  the enumeration.
            return FALSE;
        }
    }
    // The enumeration stops when the callback method returns FALSE. 
    //   If here, then return TRUE because a matching algorithm has
    //   not been found.
    return TRUE;
}
```



<span data-ttu-id="b453a-121">En el ejemplo de código siguiente se incluye la funcionalidad de validación en un único método.</span><span class="sxs-lookup"><span data-stu-id="b453a-121">The following code example wraps the validation functionality into a single method.</span></span> <span data-ttu-id="b453a-122">Este método devuelve un valor **booleano** que indica si el certificado admite el método Signature y si el sistema admite el método Signature.</span><span class="sxs-lookup"><span data-stu-id="b453a-122">This method returns a **Boolean** value that indicates whether the certificate supports the signature method and whether the signature method is supported by the system.</span></span>


```C++
BOOL 
SupportsSignatureAlgorithm (
    __in LPCWSTR signingMethodToCheck,
    __in PCCERT_CONTEXT certificateToCheck
)
{
    HRESULT     hr = S_OK;

    // Initialize the structure that contains the   
    //  information about the signature algorithm to check
    SignatureMethodData        certificateAlgorithmData;

    certificateAlgorithmData.userSignatureAlgorithmSupported = 
        FALSE;
    certificateAlgorithmData.userSignatureAlgorithmToCheck = 
        signingMethodToCheck;

    // Call the crypt API to get information about the algorithms
    //   that are supported by the certificate and initialize 
    //   certificateAlgorithmData
    certificateAlgorithmData.certificateAlgorithmInfo = CryptFindOIDInfo (
        CRYPT_OID_INFO_OID_KEY,
        certificateToCheck->pCertInfo->SubjectPublicKeyInfo.Algorithm.pszObjId,
        CRYPT_PUBKEY_ALG_OID_GROUP_ID | CRYPT_OID_PREFER_CNG_ALGID_FLAG);

    if (certificateAlgorithmData.certificateAlgorithmInfo != NULL)
    {
        // Enumerate the algorithms that are supported by the 
        //   certificate, and use our callback method to determine if
        //   the user supplied signature algorithm is supported by 
        //     the certificate.
        //
        // Note that CRYPT_XML_GROUP_ID_SIGN is used to enumerate
        //  the signature methods
        hr = CryptXmlEnumAlgorithmInfo(
            CRYPT_XML_GROUP_ID_SIGN,  // NOTE: CRYPT_XML_GROUP_ID_SIGN
            CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
            (void*)&certificateAlgorithmData,
            EnumSignatureMethodCallback);
        // when the enumeration has returned successfully, 
        //  certificateAlgorithmData.userSignatureAlgorithmSupported
        //  will be TRUE if the signing method is supported by
        //  the certificate
    }
    return certificateAlgorithmData.userSignatureAlgorithmSupported;
}
```



## <a name="related-topics"></a><span data-ttu-id="b453a-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b453a-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b453a-124">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="b453a-124">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="b453a-125">Cargar un certificado desde un archivo</span><span class="sxs-lookup"><span data-stu-id="b453a-125">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="b453a-126">Comprobar que el sistema admite un método de síntesis</span><span class="sxs-lookup"><span data-stu-id="b453a-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="b453a-127">Insertar cadenas de certificado en un documento</span><span class="sxs-lookup"><span data-stu-id="b453a-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="b453a-128">**Se usa en este ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b453a-128">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="b453a-129">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="b453a-129">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[<span data-ttu-id="b453a-130">**CIFRAr \_ información de OID \_**</span><span class="sxs-lookup"><span data-stu-id="b453a-130">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

<span data-ttu-id="b453a-131">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="b453a-131">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="b453a-132">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="b453a-132">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="b453a-133">API de criptografía</span><span class="sxs-lookup"><span data-stu-id="b453a-133">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="b453a-134">Funciones de criptografía</span><span class="sxs-lookup"><span data-stu-id="b453a-134">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="b453a-135">Errores de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="b453a-135">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="b453a-136">Errores de documento XPS</span><span class="sxs-lookup"><span data-stu-id="b453a-136">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="b453a-137">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="b453a-137">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
