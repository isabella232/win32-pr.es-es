---
description: Signos y hora marca el archivo especificado, lo que permite varias firmas anidadas.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: SignerSignEx2 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278424"
---
# <a name="signersignex2-function"></a><span data-ttu-id="85e7b-103">SignerSignEx2 función)</span><span class="sxs-lookup"><span data-stu-id="85e7b-103">SignerSignEx2 function</span></span>

<span data-ttu-id="85e7b-104">La función **SignerSignEx2** firma y marca la hora del archivo especificado, lo que permite varias firmas anidadas.</span><span class="sxs-lookup"><span data-stu-id="85e7b-104">The **SignerSignEx2** function signs and time stamps the specified file, allowing multiple nested signatures.</span></span>

> [!Note]  
> <span data-ttu-id="85e7b-105">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="85e7b-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="85e7b-106">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="85e7b-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85e7b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85e7b-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="85e7b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85e7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85e7b-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-110">Modifica el comportamiento de esta función.</span><span class="sxs-lookup"><span data-stu-id="85e7b-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="85e7b-111">Si el archivo que se va a firmar es un archivo ejecutable portable (PE), puede ser cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="85e7b-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="85e7b-112">Value</span><span class="sxs-lookup"><span data-stu-id="85e7b-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="85e7b-113">Significado</span><span class="sxs-lookup"><span data-stu-id="85e7b-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="85e7b-114"><dt>**SPC \_ \_Marca de \_ \_ hash \_ de página del PE de EXC**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-114"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="85e7b-115">Excluya los hash de página al crear datos indirectos de SIP para el archivo PE.</span><span class="sxs-lookup"><span data-stu-id="85e7b-115">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="85e7b-116">Esta marca tiene prioridad sobre la marca de **marca de hash de página de SPC \_ Inc \_ PE \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="85e7b-116">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="85e7b-117">Si no se especifica la marca **hash de página de PE de SPC \_ EXC \_ \_ \_ \_** o la marca hash de **Página de SPC \_ Inc Inc \_ \_ \_ \_** , se usa el valor establecido con la función [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) para esta configuración.</span><span class="sxs-lookup"><span data-stu-id="85e7b-117">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="85e7b-118">El valor predeterminado para esta opción es excluir los valores hash de página al crear datos indirectos SIP para archivos PE.</span><span class="sxs-lookup"><span data-stu-id="85e7b-118">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="85e7b-119">Este valor se define en el archivo de encabezado Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="85e7b-119">This value is defined in the Mssip.h header file.</span></span><br/> <span data-ttu-id="85e7b-120">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="85e7b-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="85e7b-121"><dt>**SPC \_ El \_ marcador de la tabla de direcciones de importación PE de \_ \_ \_ \_ PE**</dt> es <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="85e7b-122">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="85e7b-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="85e7b-123"><dt>**SPC \_ \_Marca de \_ \_ información de \_ depuración PE de PE**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="85e7b-124">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="85e7b-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="85e7b-125"><dt>**SPC \_ \_Indicador de \_ recursos \_ de PE de PE**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="85e7b-126">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="85e7b-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="85e7b-127"><dt>**SPC \_ \_Marca de \_ \_ hash \_ de página de PE de PE**</dt> <dt>0x100</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="85e7b-128">Incluir hashes de página al crear datos indirectos de SIP para el archivo PE.</span><span class="sxs-lookup"><span data-stu-id="85e7b-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="85e7b-129">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="85e7b-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> <span data-ttu-id="85e7b-130">Este valor se define en el archivo de encabezado Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="85e7b-130">This value is defined in the Mssip.h header file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <span data-ttu-id="85e7b-131"><dt>**SIG \_ ANEXAr**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-131"><dt>**SIG\_APPEND**</dt> <dt>0x1000</dt></span></span> </dl>                                                                         | <span data-ttu-id="85e7b-132">La firma se anidará.</span><span class="sxs-lookup"><span data-stu-id="85e7b-132">The signature will be nested.</span></span> <span data-ttu-id="85e7b-133">Si establece esta marca antes de que se agregue cualquier firma, la firma generada se agregará como la firma externa.</span><span class="sxs-lookup"><span data-stu-id="85e7b-133">If you set this flag before any signature has been added, the generated signature will be added as the outer signature.</span></span> <span data-ttu-id="85e7b-134">Si no establece esta marca, la firma generada reemplaza la firma externa y elimina todas las firmas internas.</span><span class="sxs-lookup"><span data-stu-id="85e7b-134">If you do not set this flag, the generated signature replaces the outer signature, deleting all inner signatures.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="85e7b-135">*pSubjectInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-135">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-136">Puntero a una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que especifica el sujeto que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="85e7b-136">Pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-137">*pSignerCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-137">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-138">Puntero a una estructura de [**\_ certificado de firmante**](signer-cert.md) que especifica el certificado que se va a utilizar para crear la firma digital.</span><span class="sxs-lookup"><span data-stu-id="85e7b-138">Pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-139">*pSignatureInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-139">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-140">Puntero a una estructura de [**\_ \_ información de firma de firmante**](signer-signature-info.md) que contiene información sobre la firma digital.</span><span class="sxs-lookup"><span data-stu-id="85e7b-140">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-141">*pProviderInfo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-141">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-142">Puntero a una estructura de [**\_ \_ información del proveedor de firmante**](signer-provider-info.md) que especifica el proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) y la información de clave privada que se usa para crear la firma digital.</span><span class="sxs-lookup"><span data-stu-id="85e7b-142">Pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="85e7b-143">Si el valor de este parámetro es **null**, el parámetro *pSignerCert* debe especificar un certificado asociado a un CSP.</span><span class="sxs-lookup"><span data-stu-id="85e7b-143">If the value of this parameter is **NULL**, the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-144">*dwTimestampFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-144">*dwTimestampFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-145">Marcas que se pasarán a [**SignerTimeStampEx3**](signertimestampex3.md) si el parámetro *PwszHttpTimeStamp* no es **null**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-145">Flags that will be passed to [**SignerTimeStampEx3**](signertimestampex3.md) if the *pwszHttpTimeStamp* parameter is not **NULL**.</span></span> <span data-ttu-id="85e7b-146">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="85e7b-146">This can be one of the following values.</span></span>



| <span data-ttu-id="85e7b-147">Value</span><span class="sxs-lookup"><span data-stu-id="85e7b-147">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="85e7b-148">Significado</span><span class="sxs-lookup"><span data-stu-id="85e7b-148">Meaning</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="85e7b-149"><dt>**marca de tiempo del firmante \_ \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-149"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="85e7b-150">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="85e7b-150">Default value.</span></span> <span data-ttu-id="85e7b-151">Especifica una marca de tiempo de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="85e7b-151">Specifies an Authenticode timestamp.</span></span><br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="85e7b-152"><dt>**Marca de tiempo del firmante \_ \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-152"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="85e7b-153">Especifica una marca de tiempo RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="85e7b-153">Specifies an RFC 3161 timestamp.</span></span><br/>                    |



 

<span data-ttu-id="85e7b-154">Este parámetro se omite si el parámetro *pwszHttpTimeStamp* es **null**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-154">This parameter is ignored if the *pwszHttpTimeStamp* parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-155">*pszTimestampAlgorithmOid* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-155">*pszTimestampAlgorithmOid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-156">Identificador de objeto del algoritmo que se va a usar para crear una marca de tiempo RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="85e7b-156">Object identifier of the algorithm to be used for creating an RFC 3161 timestamp.</span></span> <span data-ttu-id="85e7b-157">Este parámetro se omite para las marcas de tiempo de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="85e7b-157">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-158">*pwszHttpTimeStamp* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-158">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-159">Dirección URL del servidor de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="85e7b-159">URL of the time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-160">*psRequest* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-160">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-161">Puntero a una matriz de estructuras de [**\_ atributo de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) que se agregan a una solicitud de firma.</span><span class="sxs-lookup"><span data-stu-id="85e7b-161">Pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="85e7b-162">Este parámetro se omite si el parámetro *pwszHttpTimeStamp* no contiene un valor válido o es **null**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-162">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value or is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-163">*pSipData* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-163">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-164">Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP.</span><span class="sxs-lookup"><span data-stu-id="85e7b-164">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="85e7b-165">El proveedor SIP define el formato y el contenido de este.</span><span class="sxs-lookup"><span data-stu-id="85e7b-165">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-166">*ppSignerContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-166">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-167">Dirección de un puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que contiene el [*BLOB*](../secgloss/b-gly.md)firmado.</span><span class="sxs-lookup"><span data-stu-id="85e7b-167">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="85e7b-168">Cuando haya terminado de usar la estructura de **\_ contexto del firmante** , libere la estructura del **\_ contexto del firmante** llamando a la función [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="85e7b-168">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-169">*pCryptoPolicy* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-169">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-170">Si está presente, es un puntero a un [**certificado de \_ \_ firma segura \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) la estructura que contiene los parámetros utilizados para comprobar las signaturas seguras.</span><span class="sxs-lookup"><span data-stu-id="85e7b-170">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="85e7b-171">Si un certificado o su cadena no pasa, el archivo no se modifica de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="85e7b-171">If either a certificate or its chain does not pass, the file is not altered in any way.</span></span> <span data-ttu-id="85e7b-172">Si se pasa una dirección URL para especificar una autoridad de marca de tiempo (TSA), esta Directiva también se aplica a la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="85e7b-172">If a URL is passed in to specify a Time Stamping Authority (TSA), this policy is also applied to the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="85e7b-173">*Van*</span><span class="sxs-lookup"><span data-stu-id="85e7b-173">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="85e7b-174">Reservado.</span><span class="sxs-lookup"><span data-stu-id="85e7b-174">Reserved.</span></span> <span data-ttu-id="85e7b-175">Este valor debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-175">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85e7b-176">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85e7b-176">Return value</span></span>

<span data-ttu-id="85e7b-177">Si la función se ejecuta correctamente, la función devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85e7b-177">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="85e7b-178">Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="85e7b-178">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="85e7b-179">Los códigos de error posibles devueltos por esta función incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="85e7b-179">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="85e7b-180">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="85e7b-180">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



| <span data-ttu-id="85e7b-181">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="85e7b-181">Return code</span></span>                                                                                  | <span data-ttu-id="85e7b-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="85e7b-182">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85e7b-183"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-183"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="85e7b-184">Si establece el parámetro *dwTimestampFlags* en la marca de tiempo de **firma \_ \_ AUTHENTICODE**, no puede establecer el parámetro *dwFlags* en **SIG \_ Append**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-184">If you set the *dwTimestampFlags* parameter to **SIGNER\_TIMESTAMP\_AUTHENTICODE**, you cannot set the *dwFlags* parameter to **SIG\_APPEND**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="85e7b-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85e7b-185">Requirements</span></span>



| <span data-ttu-id="85e7b-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="85e7b-186">Requirement</span></span> | <span data-ttu-id="85e7b-187">Value</span><span class="sxs-lookup"><span data-stu-id="85e7b-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85e7b-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85e7b-188">Minimum supported client</span></span><br/> | <span data-ttu-id="85e7b-189">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="85e7b-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85e7b-190">Minimum supported server</span></span><br/> | <span data-ttu-id="85e7b-191">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="85e7b-192">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85e7b-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85e7b-193"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-193"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85e7b-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="85e7b-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e7b-195">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="85e7b-195">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="85e7b-196">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="85e7b-196">**SignerSignEx**</span></span>](signersignex.md)
</dt> <dt>

[<span data-ttu-id="85e7b-197">**SignerFreeSignerContext**</span><span class="sxs-lookup"><span data-stu-id="85e7b-197">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
