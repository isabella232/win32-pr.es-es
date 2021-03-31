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
# <a name="verify-that-a-certificate-supports-a-signature-method"></a>Comprobar que un certificado admite un método de firma

En este tema se describe cómo comprobar que un certificado admite un método de firma específico.

El **CryptXmlEnumAlgorithmInfo** de Microsoft Crypto API enumera las propiedades de un certificado y se usa en este ejemplo de código para enumerar los métodos de firma que admite el certificado. Para usar **CryptXmlEnumAlgorithmInfo** con el fin de enumerar los métodos de firma que admite el certificado, el llamador debe proporcionar un método de devolución de llamada y una estructura de datos en la llamada a **CryptXmlEnumAlgorithmInfo**, lo que permite pasar datos al método de devolución de llamada.

La estructura de datos utilizada en el siguiente ejemplo de código tiene los siguientes campos:

| Campo                               | Descripción                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **userSignatureAlgorithmToCheck**   | Un campo **LPWStr** que apunta a la cadena que contiene el URI del algoritmo de firma que se va a comprobar.                             |
| **certificateAlgorithmInfo**        | Puntero a una estructura **de \_ \_ información de OID de cifrado** que contiene información sobre un algoritmo de firma que es compatible con el certificado. |
| **userSignatureAlgorithmSupported** | Valor **booleano** que indica si el algoritmo de firma es compatible con el certificado.                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



El método Crypto API que comprueba el certificado usa un método de devolución de llamada para devolver datos al llamador. **CryptXmlEnumAlgorithmInfo** enumera los métodos de firma que admite el certificado y llama al método de devolución de llamada para cada método de firma hasta que el método de devolución de llamada devuelve **false** o hasta que se han enumerado todos los métodos de firma del certificado.

El método de devolución de llamada en el siguiente ejemplo de código busca un método de firma pasado por **CryptXmlEnumAlgorithmInfo** que coincida con el método de firma proporcionado por el método de llamada. Cuando se encuentra una coincidencia, el método de devolución de llamada comprueba si el sistema también admite el método de firma. Si los métodos de firma coinciden y son compatibles con el sistema, el método de firma se marca como compatible con el sistema y el método de devolución de llamada devuelve **false**.


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



En el ejemplo de código siguiente se incluye la funcionalidad de validación en un único método. Este método devuelve un valor **booleano** que indica si el certificado admite el método Signature y si el sistema admite el método Signature.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Cargar un certificado desde un archivo](load-a-certificate-from-a-file.md)
</dt> <dt>

[Comprobar que el sistema admite un método de síntesis](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Insertar cadenas de certificado en un documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Se usa en este ejemplo**
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[**CIFRAr \_ información de OID \_**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

**CryptXmlEnumAlgorithmInfo**
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[API de criptografía](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funciones de criptografía](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Errores de la API de firma digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errores de documento XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
