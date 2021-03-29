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
# <a name="how-to-programmatically-sign-an-app-package-c"></a><span data-ttu-id="65ddb-103">Cómo firmar un paquete de aplicación mediante programación (C++)</span><span class="sxs-lookup"><span data-stu-id="65ddb-103">How to programmatically sign an app package (C++)</span></span>

<span data-ttu-id="65ddb-104">Obtenga información sobre cómo firmar un paquete de aplicación mediante la función [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .</span><span class="sxs-lookup"><span data-stu-id="65ddb-104">Learn how to sign an app package by using the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span>

<span data-ttu-id="65ddb-105">Si desea crear paquetes de aplicaciones de Windows mediante programación con la [API de empaquetado](interfaces.md), también debe firmar los paquetes de la aplicación antes de que se puedan implementar.</span><span class="sxs-lookup"><span data-stu-id="65ddb-105">If you want to programmatically create Windows app packages by using the [Packaging API](interfaces.md), you also need to sign the app packages before they can be deployed.</span></span> <span data-ttu-id="65ddb-106">La API de empaquetado no proporciona un método especializado para firmar paquetes de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="65ddb-106">The Packaging API doesn't provide a specialized method for signing app packages.</span></span> <span data-ttu-id="65ddb-107">En su lugar, use las [funciones de criptografía](/windows/desktop/SecCrypto/cryptography-functions) estándar para firmar los paquetes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65ddb-107">Instead, use the standard [cryptography functions](/windows/desktop/SecCrypto/cryptography-functions) to sign your app packages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="65ddb-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="65ddb-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="65ddb-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="65ddb-109">Technologies</span></span>

-   <span data-ttu-id="65ddb-110">[Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65ddb-110">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   [<span data-ttu-id="65ddb-111">Empaquetado, implementación y consulta de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="65ddb-111">Packaging, deployment, and query of Windows apps</span></span>](appx-portal.md)
-   [<span data-ttu-id="65ddb-112">funciones de criptografía</span><span class="sxs-lookup"><span data-stu-id="65ddb-112">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a><span data-ttu-id="65ddb-113">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="65ddb-113">Prerequisites</span></span>

-   <span data-ttu-id="65ddb-114">Debe tener una aplicación de Windows empaquetada.</span><span class="sxs-lookup"><span data-stu-id="65ddb-114">You need to have a packaged Windows app.</span></span> <span data-ttu-id="65ddb-115">Para obtener información sobre cómo crear un paquete de la aplicación, consulte [Cómo crear un paquete de la aplicación](how-to-create-a-package.md).</span><span class="sxs-lookup"><span data-stu-id="65ddb-115">For info about creating an app package, see [How to create an app package](how-to-create-a-package.md).</span></span>
-   <span data-ttu-id="65ddb-116">Debe tener un certificado de firma de código adecuado para firmar el paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65ddb-116">You need to have a code signing certificate that is appropriate for signing the app package.</span></span> <span data-ttu-id="65ddb-117">Para obtener información sobre cómo crear un certificado de firma de código de prueba, consulte [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="65ddb-117">For info about creating a test code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span> <span data-ttu-id="65ddb-118">Cargue este certificado de firma en una estructura de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="65ddb-118">Load this signing certificate into a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="65ddb-119">Por ejemplo, puede usar [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) y [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) para cargar un certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="65ddb-119">For example, you can use [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) and [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) to load a signing certificate.</span></span>
-   <span data-ttu-id="65ddb-120">Windows 8 presenta la función [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .</span><span class="sxs-lookup"><span data-stu-id="65ddb-120">Windows 8 introduces the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span> <span data-ttu-id="65ddb-121">Use **SignerSignEx2** al firmar paquetes de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="65ddb-121">Use **SignerSignEx2** when you sign Windows app packages.</span></span>

## <a name="instructions"></a><span data-ttu-id="65ddb-122">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="65ddb-122">Instructions</span></span>

### <a name="step-1-define-the-required-structures-for-signersignex2"></a><span data-ttu-id="65ddb-123">Paso 1: definición de las estructuras necesarias para SignerSignEx2</span><span class="sxs-lookup"><span data-stu-id="65ddb-123">Step 1: Define the required structures for SignerSignEx2</span></span>

<span data-ttu-id="65ddb-124">Además del encabezado Wincrypt. h, la función [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) depende de muchas estructuras que no están definidas en ningún archivo de encabezado del SDK.</span><span class="sxs-lookup"><span data-stu-id="65ddb-124">In addition to the Wincrypt.h header, the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function depends on many structures that aren't defined in any SDK header file.</span></span> <span data-ttu-id="65ddb-125">Para usar **SignerSignEx2**, debe definir estas estructuras por su cuenta:</span><span class="sxs-lookup"><span data-stu-id="65ddb-125">To use **SignerSignEx2**, you must define these structures yourself:</span></span>


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



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a><span data-ttu-id="65ddb-126">Paso 2: llamar a SignerSignEx2 para firmar el paquete de la aplicación</span><span class="sxs-lookup"><span data-stu-id="65ddb-126">Step 2: Call SignerSignEx2 to sign the app package</span></span>

<span data-ttu-id="65ddb-127">Después de definir las estructuras necesarias que se especifican en el paso anterior, puede utilizar cualquiera de las opciones disponibles en la función [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) para firmar un paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65ddb-127">After you define the required structures that are specified in the previous step, you can use any of the options available on the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function to sign an app package.</span></span> <span data-ttu-id="65ddb-128">Cuando se usa **SignerSignEx2** con paquetes de aplicaciones de Windows, estas restricciones se aplican:</span><span class="sxs-lookup"><span data-stu-id="65ddb-128">When you use **SignerSignEx2** with Windows app packages, these restrictions apply:</span></span>

-   <span data-ttu-id="65ddb-129">Debe proporcionar un puntero a una estructura **de \_ \_ \_ datos de cliente SIP de appx** como el parámetro *pSipData* al firmar un paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="65ddb-129">You must provide a pointer to an **APPX\_SIP\_CLIENT\_DATA** structure as the *pSipData* parameter when you sign an app package.</span></span> <span data-ttu-id="65ddb-130">Debe rellenar el miembro **pSignerParams** de los **\_ \_ \_ datos del cliente SIP de appx** con los mismos parámetros que usa para firmar el paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65ddb-130">You must populate the **pSignerParams** member of **APPX\_SIP\_CLIENT\_DATA** with the same parameters that you use to sign the app package.</span></span> <span data-ttu-id="65ddb-131">Para ello, defina los parámetros deseados en la estructura Signer **\_ Sign \_ EX2 \_ params** , asigne la dirección de esta estructura a **pSignerParams** y, a continuación, haga referencia directamente a los miembros de la estructura cuando llame a [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).</span><span class="sxs-lookup"><span data-stu-id="65ddb-131">To do this, define your desired parameters on the **SIGNER\_SIGN\_EX2\_PARAMS** structure, assign the address of this structure to **pSignerParams**, and then directly reference the structure's members as well when you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).</span></span>
-   <span data-ttu-id="65ddb-132">Después de llamar a [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), debe liberar **pAppxSipState** en *pSipData* llamando a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en **pAppxSipState** si no es **null**.</span><span class="sxs-lookup"><span data-stu-id="65ddb-132">After you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), you must free the **pAppxSipState** on the *pSipData* by calling [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on **pAppxSipState** if it's not **NULL**.</span></span>
-   <span data-ttu-id="65ddb-133">El miembro **algidHash** de la estructura de **\_ \_ información de firma del firmante** debe ser el mismo algoritmo hash que se usó para crear el paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65ddb-133">The **algidHash** member of the **SIGNER\_SIGNATURE\_INFO** structure must be the same hash algorithm that was used in creating the app package.</span></span> <span data-ttu-id="65ddb-134">Para obtener información sobre cómo determinar el algoritmo hash del paquete de la aplicación, consulte [cómo firmar un paquete de aplicación mediante SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="65ddb-134">For info about how to determine the hash algorithm from the app package, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="65ddb-135">El algoritmo predeterminado de Windows 8 que se usa en [MakeAppx](make-appx-package--makeappx-exe-.md) y Visual Studio para crear paquetes de aplicaciones es "ALGIDHASH = CALG \_ Sha \_ 256".</span><span class="sxs-lookup"><span data-stu-id="65ddb-135">The Windows 8 default algorithm that [MakeAppx](make-appx-package--makeappx-exe-.md) and Visual Studio use to create app packages is “algidHash = CALG\_SHA\_256”.</span></span>
-   <span data-ttu-id="65ddb-136">Si desea marcar la firma en el paquete de la aplicación, debe hacerlo durante la llamada a [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) proporcionando los parámetros opcionales de marca de tiempo de **SignerSignEx2**(*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*).</span><span class="sxs-lookup"><span data-stu-id="65ddb-136">If you want to time stamp the signature on the app package as well, you must do so during the call to [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) by providing **SignerSignEx2**'s optional time stamping parameters (*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*).</span></span> <span data-ttu-id="65ddb-137">No se admite la llamada a [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) o sus variantes en un paquete de aplicación que ya está firmado.</span><span class="sxs-lookup"><span data-stu-id="65ddb-137">Calling [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) or its variants on an app package that is already signed is unsupported.</span></span>

<span data-ttu-id="65ddb-138">Este es un ejemplo de código que muestra cómo llamar a [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):</span><span class="sxs-lookup"><span data-stu-id="65ddb-138">Here is some example code that shows how to call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):</span></span>


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



## <a name="remarks"></a><span data-ttu-id="65ddb-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65ddb-139">Remarks</span></span>

<span data-ttu-id="65ddb-140">Después de firmar el paquete de la aplicación, también puede intentar validar la firma mediante programación con la función [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) con la **\_ acción wintrust \_ genérica \_ Verify \_ V2**.</span><span class="sxs-lookup"><span data-stu-id="65ddb-140">After you sign the app package, you can also attempt to validate the signature programmatically by using the [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) function with **WINTRUST\_ACTION\_GENERIC\_VERIFY\_V2**.</span></span> <span data-ttu-id="65ddb-141">En este caso, no hay ninguna consideración especial para usar **WinVerifyTrust** con paquetes de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="65ddb-141">There are no special considerations in this case for using **WinVerifyTrust** with Windows app packages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65ddb-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65ddb-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="65ddb-143">[Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65ddb-143">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="65ddb-144">API de empaquetado</span><span class="sxs-lookup"><span data-stu-id="65ddb-144">Packaging API</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="65ddb-145">funciones de criptografía</span><span class="sxs-lookup"><span data-stu-id="65ddb-145">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 