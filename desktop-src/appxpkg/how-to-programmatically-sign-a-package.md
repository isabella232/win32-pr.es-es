---
title: Cómo firmar un paquete de aplicación mediante programación (C++)
description: Obtenga información sobre cómo firmar un paquete de aplicación mediante la función SignerSignEx2.
ms.assetid: 1183D665-83C9-4BE7-9C8D-834484B8C57F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310ba2a934a6986809329a12afa8ee20b2f6591
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789663"
---
# <a name="how-to-programmatically-sign-an-app-package-c"></a>Cómo firmar un paquete de aplicación mediante programación (C++)

Obtenga información sobre cómo firmar un paquete de aplicación mediante la función [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .

Si desea crear paquetes de aplicaciones de Windows mediante programación con la [API de empaquetado](interfaces.md), también debe firmar los paquetes de la aplicación antes de que se puedan implementar. La API de empaquetado no proporciona un método especializado para firmar paquetes de aplicaciones. En su lugar, use las [funciones de criptografía](/windows/desktop/SecCrypto/cryptography-functions) estándar para firmar los paquetes de la aplicación.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Empaquetado, implementación y consulta de aplicaciones de Windows](appx-portal.md)
-   [funciones de criptografía](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a>Requisitos previos

-   Debe tener una aplicación de Windows empaquetada. Para obtener información sobre cómo crear un paquete de la aplicación, consulte [Cómo crear un paquete de la aplicación](how-to-create-a-package.md).
-   Debe tener un certificado de firma de código adecuado para firmar el paquete de la aplicación. Para obtener información sobre cómo crear un certificado de firma de código de prueba, consulte [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md). Cargue este certificado de firma en una estructura de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . Por ejemplo, puede usar [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) y [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) para cargar un certificado de firma.
-   Windows 8 presenta la función [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) . Use **SignerSignEx2** al firmar paquetes de aplicaciones de Windows.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-define-the-required-structures-for-signersignex2"></a>Paso 1: definición de las estructuras necesarias para SignerSignEx2

Además del encabezado Wincrypt. h, la función [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) depende de muchas estructuras que no están definidas en ningún archivo de encabezado del SDK. Para usar **SignerSignEx2**, debe definir estas estructuras por su cuenta:


```C++
typedef struct _SIGNER_FILE_INFO
{
    DWORD cbSize;
    LPCWSTR pwszFileName;
    HANDLE hFile;
}SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
 
typedef struct _SIGNER_BLOB_INFO
{
    DWORD cbSize;
    GUID *pGuidSubject;
    DWORD cbBlob;
    BYTE *pbBlob;
    LPCWSTR pwszDisplayName;
}SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
 
typedef struct _SIGNER_SUBJECT_INFO
{
    DWORD cbSize;
    DWORD *pdwIndex;
    DWORD dwSubjectChoice;
    union
    {
        SIGNER_FILE_INFO *pSignerFileInfo;
        SIGNER_BLOB_INFO *pSignerBlobInfo;
    };
}SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
 
// dwSubjectChoice should be one of the following:
#define SIGNER_SUBJECT_FILE    0x01
#define SIGNER_SUBJECT_BLOB    0x02
 
typedef struct _SIGNER_ATTR_AUTHCODE
{
    DWORD cbSize;
    BOOL fCommercial;
    BOOL fIndividual;
    LPCWSTR pwszName;
    LPCWSTR pwszInfo;
}SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
 
typedef struct _SIGNER_SIGNATURE_INFO
{
    DWORD cbSize;
    ALG_ID algidHash;
    DWORD dwAttrChoice;
    union
    {
        SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
    };
    PCRYPT_ATTRIBUTES psAuthenticated;
    PCRYPT_ATTRIBUTES psUnauthenticated;
}SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
 
// dwAttrChoice should be one of the following:
#define SIGNER_NO_ATTR          0x00
#define SIGNER_AUTHCODE_ATTR    0x01
 
typedef struct _SIGNER_PROVIDER_INFO
{
    DWORD cbSize;
    LPCWSTR pwszProviderName;
    DWORD dwProviderType;
    DWORD dwKeySpec;
    DWORD dwPvkChoice;
    union
    {
        LPWSTR pwszPvkFileName;
        LPWSTR pwszKeyContainer;
    };
}SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
 
//dwPvkChoice should be one of the following:
#define PVK_TYPE_FILE_NAME       0x01
#define PVK_TYPE_KEYCONTAINER    0x02
 
typedef struct _SIGNER_SPC_CHAIN_INFO
{
    DWORD cbSize;
    LPCWSTR pwszSpcFile;
    DWORD dwCertPolicy; 
    HCERTSTORE hCertStore;
}SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
 
typedef struct _SIGNER_CERT_STORE_INFO
{
    DWORD cbSize;
    PCCERT_CONTEXT pSigningCert;
    DWORD dwCertPolicy;
    HCERTSTORE hCertStore;
}SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
 
//dwCertPolicy can be a combination of the following flags:
#define SIGNER_CERT_POLICY_STORE            0x01
#define SIGNER_CERT_POLICY_CHAIN            0x02
#define SIGNER_CERT_POLICY_SPC              0x04
#define SIGNER_CERT_POLICY_CHAIN_NO_ROOT    0x08
 
typedef struct _SIGNER_CERT
{
    DWORD cbSize;
    DWORD dwCertChoice;
    union
    {
        LPCWSTR pwszSpcFile;
        SIGNER_CERT_STORE_INFO *pCertStoreInfo;
        SIGNER_SPC_CHAIN_INFO *pSpcChainInfo;
    };
    HWND hwnd;
}SIGNER_CERT, *PSIGNER_CERT;
 
//dwCertChoice should be one of the following
#define SIGNER_CERT_SPC_FILE     0x01
#define SIGNER_CERT_STORE        0x02
#define SIGNER_CERT_SPC_CHAIN    0x03
 
typedef struct _SIGNER_CONTEXT
{
    DWORD cbSize;
    DWORD cbBlob;
    BYTE *pbBlob;
}SIGNER_CONTEXT, *PSIGNER_CONTEXT;
 
typedef struct _SIGNER_SIGN_EX2_PARAMS
{
    DWORD dwFlags;
    PSIGNER_SUBJECT_INFO pSubjectInfo;
    PSIGNER_CERT pSigningCert;
    PSIGNER_SIGNATURE_INFO pSignatureInfo;
    PSIGNER_PROVIDER_INFO pProviderInfo;
    DWORD dwTimestampFlags;
    PCSTR pszAlgorithmOid;
    PCWSTR pwszTimestampURL;
    PCRYPT_ATTRIBUTES pCryptAttrs;
    PVOID pSipData;
    PSIGNER_CONTEXT *pSignerContext;
    PVOID pCryptoPolicy;
    PVOID pReserved;
} SIGNER_SIGN_EX2_PARAMS, *PSIGNER_SIGN_EX2_PARAMS;
 
typedef struct _APPX_SIP_CLIENT_DATA
{
    PSIGNER_SIGN_EX2_PARAMS pSignerParams;
    IUnknown* pAppxSipState;
} APPX_SIP_CLIENT_DATA, *PAPPX_SIP_CLIENT_DATA;
```



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a>Paso 2: llamar a SignerSignEx2 para firmar el paquete de la aplicación

Después de definir las estructuras necesarias que se especifican en el paso anterior, puede utilizar cualquiera de las opciones disponibles en la función [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) para firmar un paquete de la aplicación. Cuando se usa **SignerSignEx2** con paquetes de aplicaciones de Windows, estas restricciones se aplican:

-   Debe proporcionar un puntero a una estructura **de \_ \_ \_ datos de cliente SIP de appx** como el parámetro *pSipData* al firmar un paquete de aplicación. Debe rellenar el miembro **pSignerParams** de los **\_ \_ \_ datos del cliente SIP de appx** con los mismos parámetros que usa para firmar el paquete de la aplicación. Para ello, defina los parámetros deseados en la estructura Signer **\_ Sign \_ EX2 \_ params** , asigne la dirección de esta estructura a **pSignerParams** y, a continuación, haga referencia directamente a los miembros de la estructura cuando llame a [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).
-   Después de llamar a [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), debe liberar **pAppxSipState** en *pSipData* llamando a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en **pAppxSipState** si no es **null**.
-   El miembro **algidHash** de la estructura de **\_ \_ información de firma del firmante** debe ser el mismo algoritmo hash que se usó para crear el paquete de la aplicación. Para obtener información sobre cómo determinar el algoritmo hash del paquete de la aplicación, consulte [cómo firmar un paquete de aplicación mediante SignTool](how-to-sign-a-package-using-signtool.md). El algoritmo predeterminado de Windows 8 que se usa en [MakeAppx](make-appx-package--makeappx-exe-.md) y Visual Studio para crear paquetes de aplicaciones es "ALGIDHASH = CALG \_ Sha \_ 256".
-   Si desea marcar la firma en el paquete de la aplicación, debe hacerlo durante la llamada a [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) proporcionando los parámetros opcionales de marca de tiempo de **SignerSignEx2**(*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*). No se admite la llamada a [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) o sus variantes en un paquete de aplicación que ya está firmado.

Este es un ejemplo de código que muestra cómo llamar a [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):


```C++
HRESULT SignAppxPackage(
    _In_ PCCERT_CONTEXT signingCertContext,
    _In_ LPCWSTR packageFilePath)
{
    HRESULT hr = S_OK;
 
    // Initialize the parameters for SignerSignEx2
    DWORD signerIndex = 0;
 
    SIGNER_FILE_INFO fileInfo = {};
    fileInfo.cbSize = sizeof(SIGNER_FILE_INFO);
    fileInfo.pwszFileName = packageFilePath;
 
    SIGNER_SUBJECT_INFO subjectInfo = {};
    subjectInfo.cbSize = sizeof(SIGNER_SUBJECT_INFO);
    subjectInfo.pdwIndex = &signerIndex;
    subjectInfo.dwSubjectChoice = SIGNER_SUBJECT_FILE;
    subjectInfo.pSignerFileInfo = &fileInfo;
 
    SIGNER_CERT_STORE_INFO certStoreInfo = {};
    certStoreInfo.cbSize = sizeof(SIGNER_CERT_STORE_INFO);
    certStoreInfo.dwCertPolicy = SIGNER_CERT_POLICY_CHAIN_NO_ROOT;
    certStoreInfo.pSigningCert = signingCertContext;
 
    SIGNER_CERT cert = {};
    cert.cbSize = sizeof(SIGNER_CERT);
    cert.dwCertChoice = SIGNER_CERT_STORE;
    cert.pCertStoreInfo = &certStoreInfo;
 
    // The algidHash of the signature to be created must match the
    // hash algorithm used to create the app package
    SIGNER_SIGNATURE_INFO signatureInfo = {};
    signatureInfo.cbSize = sizeof(SIGNER_SIGNATURE_INFO);
    signatureInfo.algidHash = CALG_SHA_256; 
    signatureInfo.dwAttrChoice = SIGNER_NO_ATTR;
 
    SIGNER_SIGN_EX2_PARAMS signerParams = {};
    signerParams.pSubjectInfo = &subjectInfo;
    signerParams.pSigningCert = &cert;
    signerParams.pSignatureInfo = &signatureInfo;
 
    APPX_SIP_CLIENT_DATA sipClientData = {};
    sipClientData.pSignerParams = &signerParams;
    signerParams.pSipData = &sipClientData;
 
    // Type definition for invoking SignerSignEx2 via GetProcAddress
    typedef HRESULT (WINAPI *SignerSignEx2Function)(
        DWORD,
        PSIGNER_SUBJECT_INFO,
        PSIGNER_CERT,
        PSIGNER_SIGNATURE_INFO,
        PSIGNER_PROVIDER_INFO,
        DWORD,
        PCSTR,
        PCWSTR,
        PCRYPT_ATTRIBUTES,
        PVOID,
        PSIGNER_CONTEXT *,
        PVOID,
        PVOID); 
 
    // Load the SignerSignEx2 function from MSSign32.dll
    HMODULE msSignModule = LoadLibraryEx(
        L"MSSign32.dll", 
        NULL, 
        LOAD_LIBRARY_SEARCH_SYSTEM32);

    if (msSignModule)
    {
        SignerSignEx2Function SignerSignEx2 = reinterpret_cast<SignerSignEx2Function>(
            GetProcAddress(msSignModule, "SignerSignEx2"));
        if (SignerSignEx2)
        {
            hr = SignerSignEx2(
                signerParams.dwFlags,
                signerParams.pSubjectInfo,
                signerParams.pSigningCert,
                signerParams.pSignatureInfo,
                signerParams.pProviderInfo,
                signerParams.dwTimestampFlags,
                signerParams.pszAlgorithmOid,
                signerParams.pwszTimestampURL,
                signerParams.pCryptAttrs,
                signerParams.pSipData,
                signerParams.pSignerContext,
                signerParams.pCryptoPolicy,
                signerParams.pReserved);
        }
        else
        {
            DWORD lastError = GetLastError();
            hr = HRESULT_FROM_WIN32(lastError);
        }
 
        FreeLibrary(msSignModule);
    }
    else
    {
        DWORD lastError = GetLastError();
        hr = HRESULT_FROM_WIN32(lastError);
    }
 
    // Free any state used during app package signing
    if (sipClientData.pAppxSipState)
    {
        sipClientData.pAppxSipState->Release();
    }
 
    return hr;
}
```



## <a name="remarks"></a>Observaciones

Después de firmar el paquete de la aplicación, también puede intentar validar la firma mediante programación con la función [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) con la **\_ acción wintrust \_ genérica \_ Verify \_ V2**. En este caso, no hay ninguna consideración especial para usar **WinVerifyTrust** con paquetes de aplicaciones de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[API de empaquetado](interfaces.md)
</dt> <dt>

[funciones de criptografía](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 