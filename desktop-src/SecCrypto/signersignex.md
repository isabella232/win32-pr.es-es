---
description: Firma el archivo especificado y devuelve un puntero a los datos firmados.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: SignerSignEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812823"
---
# <a name="signersignex-function"></a><span data-ttu-id="42880-103">SignerSignEx función)</span><span class="sxs-lookup"><span data-stu-id="42880-103">SignerSignEx function</span></span>

<span data-ttu-id="42880-104">La función **SignerSignEx** firma el archivo especificado y devuelve un puntero a los datos firmados.</span><span class="sxs-lookup"><span data-stu-id="42880-104">The **SignerSignEx** function signs the specified file and returns a pointer to the signed data.</span></span>

> [!Note]  
> <span data-ttu-id="42880-105">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="42880-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="42880-106">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="42880-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="42880-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42880-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="42880-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42880-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42880-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="42880-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42880-110">Modifica el comportamiento de esta función.</span><span class="sxs-lookup"><span data-stu-id="42880-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="42880-111">Si el archivo que se va a firmar es un archivo ejecutable portable (PE), puede ser cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="42880-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="42880-112">Estos identificadores se definen en Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="42880-112">These identifiers are defined in Mssip.h.</span></span>



| <span data-ttu-id="42880-113">Value</span><span class="sxs-lookup"><span data-stu-id="42880-113">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="42880-114">Significado</span><span class="sxs-lookup"><span data-stu-id="42880-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="42880-115"><dt>**SPC \_ \_Marca de \_ \_ hash \_ de página del PE de EXC**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="42880-115"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="42880-116">Excluya los hash de página al crear datos indirectos de SIP para el archivo PE.</span><span class="sxs-lookup"><span data-stu-id="42880-116">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="42880-117">Esta marca tiene prioridad sobre la marca de **marca de hash de página de SPC \_ Inc \_ PE \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="42880-117">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="42880-118">Si no se especifica la marca **hash de página de PE de SPC \_ EXC \_ \_ \_ \_** o la marca hash de **Página de SPC \_ Inc Inc \_ \_ \_ \_** , se usa el valor establecido con la función [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) para esta configuración.</span><span class="sxs-lookup"><span data-stu-id="42880-118">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="42880-119">El valor predeterminado para esta opción es excluir los valores hash de página al crear datos indirectos SIP para archivos PE.</span><span class="sxs-lookup"><span data-stu-id="42880-119">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="42880-120">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="42880-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="42880-121"><dt>**SPC \_ El \_ marcador de la tabla de direcciones de importación PE de \_ \_ \_ \_ PE**</dt> es <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="42880-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="42880-122">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="42880-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="42880-123"><dt>**SPC \_ \_Marca de \_ \_ información de \_ depuración PE de PE**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="42880-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="42880-124">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="42880-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="42880-125"><dt>**SPC \_ \_Indicador de \_ recursos \_ de PE de PE**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="42880-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="42880-126">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="42880-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="42880-127"><dt>**SPC \_ \_Marca de \_ \_ hash \_ de página de PE de PE**</dt> <dt>0x100</dt></span><span class="sxs-lookup"><span data-stu-id="42880-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="42880-128">Incluir hashes de página al crear datos indirectos de SIP para el archivo PE.</span><span class="sxs-lookup"><span data-stu-id="42880-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="42880-129">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="42880-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="42880-130">*pSubjectInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="42880-130">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42880-131">Puntero a una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que especifica el sujeto que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="42880-131">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="42880-132">*pSignerCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="42880-132">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42880-133">Puntero a una estructura de [**\_ certificado de firmante**](signer-cert.md) que especifica el certificado que se va a utilizar para crear la firma digital.</span><span class="sxs-lookup"><span data-stu-id="42880-133">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="42880-134">*pSignatureInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="42880-134">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42880-135">Puntero a una estructura de [**\_ \_ información de firma de firmante**](signer-signature-info.md) que contiene información sobre la firma digital.</span><span class="sxs-lookup"><span data-stu-id="42880-135">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="42880-136">*pProviderInfo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="42880-136">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42880-137">Puntero a una estructura de [**\_ \_ información del proveedor de firmante**](signer-provider-info.md) que especifica el proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) y la información de clave privada que se usa para crear la firma digital.</span><span class="sxs-lookup"><span data-stu-id="42880-137">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="42880-138">Si el valor de este parámetro es **null**, el valor del parámetro *pSignerCert* debe especificar un certificado asociado a un CSP.</span><span class="sxs-lookup"><span data-stu-id="42880-138">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="42880-139">*pwszHttpTimeStamp* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="42880-139">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42880-140">Dirección URL de un servidor de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="42880-140">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="42880-141">*psRequest* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="42880-141">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42880-142">Puntero a una matriz de estructuras [**de \_ atributo de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) que se agregan a una solicitud de firma.</span><span class="sxs-lookup"><span data-stu-id="42880-142">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="42880-143">Este parámetro se omite si el parámetro *pwszHttpTimeStamp* no contiene un valor válido que no sea **null**.</span><span class="sxs-lookup"><span data-stu-id="42880-143">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42880-144">*pSipData* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="42880-144">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42880-145">Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP.</span><span class="sxs-lookup"><span data-stu-id="42880-145">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="42880-146">El proveedor SIP define el formato y el contenido de este.</span><span class="sxs-lookup"><span data-stu-id="42880-146">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="42880-147">*ppSignerContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="42880-147">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42880-148">Dirección de un puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que contiene el [*BLOB*](../secgloss/b-gly.md)firmado.</span><span class="sxs-lookup"><span data-stu-id="42880-148">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="42880-149">Cuando haya terminado de usar la estructura de **\_ contexto del firmante** , libere la estructura del **\_ contexto del firmante** llamando a la función [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="42880-149">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42880-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42880-150">Return value</span></span>

<span data-ttu-id="42880-151">Si la función se ejecuta correctamente, la función devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="42880-151">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="42880-152">Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="42880-152">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="42880-153">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="42880-153">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42880-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42880-154">Requirements</span></span>



| <span data-ttu-id="42880-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="42880-155">Requirement</span></span> | <span data-ttu-id="42880-156">Value</span><span class="sxs-lookup"><span data-stu-id="42880-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42880-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42880-157">Minimum supported client</span></span><br/> | <span data-ttu-id="42880-158">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="42880-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="42880-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42880-159">Minimum supported server</span></span><br/> | <span data-ttu-id="42880-160">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="42880-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="42880-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42880-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42880-162"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42880-162"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42880-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="42880-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42880-164">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="42880-164">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="42880-165">**SignerFreeSignerContext**</span><span class="sxs-lookup"><span data-stu-id="42880-165">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
