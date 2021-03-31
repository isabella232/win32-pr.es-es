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
# <a name="verify-the-system-supports-a-digest-method"></a>Comprobar que el sistema admite un método de síntesis

En este tema se describe cómo comprobar que el sistema admite un método de síntesis.

Las firmas digitales XPS usan la API de cifrado, que proporciona métodos para comprobar que el sistema admite un método de síntesis específico. Para usar la función **CryptXmlEnumAlgorithmInfo** de la API de Crypto con el fin de enumerar los métodos de síntesis admitidos por el sistema, el llamador debe proporcionar un método de devolución de llamada y una estructura de datos. La función **CryptXmlEnumAlgorithmInfo** devuelve los datos de la enumeración al llamador mediante el método de devolución de llamada.

La estructura de datos usada en este ejemplo se muestra en el ejemplo de código siguiente y contiene los siguientes campos:

| Campo                            | Descripción                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| **userDigestAlgorithm**          | Un campo **LPWStr** que apunta a la cadena que contiene el URI del algoritmo de resumen que se va a comprobar. |
| **userDigestAlgorithmSupported** | Un valor **booleano** que indica si el algoritmo de síntesis es compatible con el certificado.           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



El método de la API de cifrado que enumera los métodos de síntesis utiliza un método de devolución de llamada para devolver datos al llamador. **CryptXmlEnumAlgorithmInfo** enumera los métodos de síntesis que admite el sistema y llama al método de devolución de llamada para cada método de síntesis que enumera, hasta que el método de devolución de llamada devuelve **false** o hasta que se enumeran todos los métodos de síntesis admitidos por el sistema. En este ejemplo, el método de devolución de llamada compara el método de síntesis que **CryptXmlEnumAlgorithmInfo** pasa con el método de síntesis proporcionado por el método de llamada.


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



En el ejemplo de código siguiente se incluye la funcionalidad de validación en un único método, que devuelve un valor **booleano** que indica si el sistema admite el método de síntesis.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Cargar un certificado desde un archivo](load-a-certificate-from-a-file.md)
</dt> <dt>

[Comprobar que un certificado admite un método de firma](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Insertar cadenas de certificado en un documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Se usa en este ejemplo**
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

 

 
