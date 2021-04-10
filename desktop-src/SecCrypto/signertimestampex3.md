---
description: Marca de tiempo el sujeto especificado y permite establecer marcas de tiempo en varias firmas.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153732"
---
# <a name="signertimestampex3-function"></a><span data-ttu-id="29f85-103">SignerTimeStampEx3 función)</span><span class="sxs-lookup"><span data-stu-id="29f85-103">SignerTimeStampEx3 function</span></span>

<span data-ttu-id="29f85-104">El tiempo de la función **SignerTimeStampEx3** marca el sujeto especificado y permite establecer marcas de tiempo en varias firmas.</span><span class="sxs-lookup"><span data-stu-id="29f85-104">The **SignerTimeStampEx3** function time stamps the specified subject and supports setting time stamps on multiple signatures.</span></span>

> [!Note]  
> <span data-ttu-id="29f85-105">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="29f85-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="29f85-106">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="29f85-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="29f85-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29f85-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="29f85-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29f85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29f85-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29f85-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29f85-110">Marca que especifica el tipo de marca de tiempo que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="29f85-110">Flag that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="29f85-111">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="29f85-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="29f85-112">Los valores son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="29f85-112">The values are mutually exclusive.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29f85-113">Value</span><span class="sxs-lookup"><span data-stu-id="29f85-113">Value</span></span></th>
<th><span data-ttu-id="29f85-114">Significado</span><span class="sxs-lookup"><span data-stu-id="29f85-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="29f85-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29f85-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="29f85-116">Especifica una marca de tiempo de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="29f85-116">Specifies an Authenticode time stamp.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="29f85-117">Authenticode ya no es el tipo preferido de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="29f85-117">Authenticode is no longer the preferred type of time stamp.</span></span> <span data-ttu-id="29f85-118">La compatibilidad con las marcas de tiempo de Authenticode puede quitarse en el futuro.</span><span class="sxs-lookup"><span data-stu-id="29f85-118">Support for Authenticode time stamps may be removed in the future.</span></span> <span data-ttu-id="29f85-119">En su lugar, se recomienda usar RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="29f85-119">We recommend that you use RFC 3161 instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="29f85-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29f85-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="29f85-121">Especifica una marca de tiempo compatible con RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="29f85-121">Specifies an RFC 3161–compliant time stamp.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="29f85-122">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29f85-122">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29f85-123">Especifica el número de secuencia de la firma a la que se agregará la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="29f85-123">Specifies the sequence number of the signature to which the timestamp will be added.</span></span> <span data-ttu-id="29f85-124">Si este valor es cero (0), la firma externa será con marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="29f85-124">If this value is zero (0), the outer signature will be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="29f85-125">*pSubjectInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29f85-125">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29f85-126">Dirección de una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que representa el sujeto de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="29f85-126">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="29f85-127">*pwszHttpTimeStamp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29f85-127">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29f85-128">Dirección de una cadena Unicode terminada en null que contiene la dirección URL de un servidor de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="29f85-128">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="29f85-129">*pszAlgorithmOid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29f85-129">*pszAlgorithmOid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29f85-130">Algoritmo hash que se va a usar para realizar las marcas de tiempo compatibles con RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="29f85-130">A hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="29f85-131">Este parámetro se omite para las marcas de tiempo de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="29f85-131">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="29f85-132">*psRequest* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="29f85-132">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29f85-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29f85-133">Optional.</span></span> <span data-ttu-id="29f85-134">Dirección de una estructura [**de \_ atributos de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="29f85-134">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="29f85-135">Este parámetro es opcional y puede ser **null** si no se incluye.</span><span class="sxs-lookup"><span data-stu-id="29f85-135">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="29f85-136">*pSipData* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="29f85-136">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29f85-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29f85-137">Optional.</span></span> <span data-ttu-id="29f85-138">Valor de 32 bits que se pasa como datos adicionales a las funciones del [*paquete de interfaz de asunto*](../secgloss/s-gly.md) (SIP).</span><span class="sxs-lookup"><span data-stu-id="29f85-138">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="29f85-139">El proveedor SIP define el formato y el contenido de este parámetro.</span><span class="sxs-lookup"><span data-stu-id="29f85-139">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="29f85-140">Este parámetro es opcional y puede ser **null** si no se incluye.</span><span class="sxs-lookup"><span data-stu-id="29f85-140">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="29f85-141">*ppSignerContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="29f85-141">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29f85-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29f85-142">Optional.</span></span> <span data-ttu-id="29f85-143">Dirección de un puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que contiene el BLOB firmado.</span><span class="sxs-lookup"><span data-stu-id="29f85-143">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="29f85-144">Cuando haya terminado de usar la estructura de **\_ contexto del firmante** , libere la llamada a la función [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="29f85-144">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="29f85-145">*pCryptoPolicy* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="29f85-145">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29f85-146">Si está presente, es un puntero a un [**certificado de \_ \_ firma segura \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) la estructura que contiene los parámetros utilizados para comprobar las signaturas seguras.</span><span class="sxs-lookup"><span data-stu-id="29f85-146">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="29f85-147">La marca de tiempo debe pasar esta directiva de cifrado.</span><span class="sxs-lookup"><span data-stu-id="29f85-147">The time stamp must pass this cryptographic policy.</span></span>

</dd> <dt>

<span data-ttu-id="29f85-148">*Van*</span><span class="sxs-lookup"><span data-stu-id="29f85-148">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="29f85-149">Reservado.</span><span class="sxs-lookup"><span data-stu-id="29f85-149">Reserved.</span></span> <span data-ttu-id="29f85-150">Este valor debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="29f85-150">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29f85-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29f85-151">Return value</span></span>

<span data-ttu-id="29f85-152">Si la función se ejecuta correctamente, la función devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29f85-152">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="29f85-153">Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="29f85-153">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="29f85-154">Los códigos de error posibles devueltos por esta función incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="29f85-154">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="29f85-155">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="29f85-155">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29f85-156">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="29f85-156">Return code</span></span></th>
<th><span data-ttu-id="29f85-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="29f85-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="29f85-158"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29f85-158"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="29f85-159">Este error se puede devolver en las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="29f85-159">This error can be returned for the following conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="29f85-160">Debe establecer <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> o <strong>SIGNER_TIMESTAMP_RFC3161</strong> para el parámetro <em>dwFlags</em> .</span><span class="sxs-lookup"><span data-stu-id="29f85-160">You must set either <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> or <strong>SIGNER_TIMESTAMP_RFC3161</strong> for the <em>dwFlags</em> parameter.</span></span></li>
<li><span data-ttu-id="29f85-161">El parámetro <em>Reserved</em> debe ser <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="29f85-161">The <em>pReserved</em> parameter must be <strong>NULL</strong>.</span></span></li>
<li><span data-ttu-id="29f85-162">Si establece la marca <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> en el parámetro <em>dwFlags</em> , debe establecer el parámetro <em>dwIndex</em> en cero.</span><span class="sxs-lookup"><span data-stu-id="29f85-162">If you set the <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> flag in the <em>dwFlags</em> parameter, you must set the <em>dwIndex</em> parameter to zero.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="29f85-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29f85-163">Requirements</span></span>



| <span data-ttu-id="29f85-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="29f85-164">Requirement</span></span> | <span data-ttu-id="29f85-165">Value</span><span class="sxs-lookup"><span data-stu-id="29f85-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29f85-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29f85-166">Minimum supported client</span></span><br/> | <span data-ttu-id="29f85-167">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="29f85-167">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="29f85-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29f85-168">Minimum supported server</span></span><br/> | <span data-ttu-id="29f85-169">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="29f85-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="29f85-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29f85-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29f85-171"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29f85-171"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29f85-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="29f85-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29f85-173">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="29f85-173">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="29f85-174">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="29f85-174">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> <dt>

[<span data-ttu-id="29f85-175">**SignerTimeStampEx2**</span><span class="sxs-lookup"><span data-stu-id="29f85-175">**SignerTimeStampEx2**</span></span>](signertimestampex2.md)
</dt> </dl>

 

 
