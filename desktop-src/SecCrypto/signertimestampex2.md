---
description: Marca de tiempo el asunto especificado y, opcionalmente, devuelve un puntero a una \_ estructura de contexto del firmante que contiene un puntero a un BLOB. Esta función se puede usar para realizar la infraestructura de clave pública X. 509, RFC 3161&\# 8211; de acuerdo con las marcas de tiempo.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668325"
---
# <a name="signertimestampex2-function"></a><span data-ttu-id="3315b-104">SignerTimeStampEx2 función)</span><span class="sxs-lookup"><span data-stu-id="3315b-104">SignerTimeStampEx2 function</span></span>

<span data-ttu-id="3315b-105">El tiempo de la función **SignerTimeStampEx2** marca el asunto especificado y, opcionalmente, devuelve un puntero a una estructura de [**\_ contexto del firmante**](signer-context.md) que contiene un puntero a un [*BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3315b-105">The **SignerTimeStampEx2** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="3315b-106">Esta función se puede usar para realizar la infraestructura de clave pública X. 509, que es compatible con RFC 3161 y las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3315b-106">This function can be used to perform X.509 Public Key Infrastructure, RFC 3161–compliant, time stamps.</span></span>

> [!Note]  
> <span data-ttu-id="3315b-107">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="3315b-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="3315b-108">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="3315b-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3315b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3315b-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="3315b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3315b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3315b-111">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3315b-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3315b-112">Valor que especifica el tipo de marca de tiempo que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="3315b-112">Value that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="3315b-113">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3315b-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="3315b-114">Los valores son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="3315b-114">The values are mutually exclusive.</span></span>



| <span data-ttu-id="3315b-115">Value</span><span class="sxs-lookup"><span data-stu-id="3315b-115">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="3315b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3315b-116">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="3315b-117"><dt>**marca de tiempo del firmante \_ \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="3315b-117"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="3315b-118">Especifica una marca de tiempo de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="3315b-118">Specifies an Authenticode time stamp.</span></span><br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="3315b-119"><dt>**Marca de tiempo del firmante \_ \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="3315b-119"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="3315b-120">Especifica una marca de tiempo compatible con RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="3315b-120">Specifies an RFC 3161–compliant time stamp.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3315b-121">*pSubjectInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3315b-121">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3315b-122">Dirección de una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que representa el sujeto de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3315b-122">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="3315b-123">*pwszHttpTimeStamp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3315b-123">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3315b-124">Dirección de una cadena Unicode terminada en null que contiene la dirección URL de un servidor de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3315b-124">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="3315b-125">*dwAlgId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3315b-125">*dwAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3315b-126">Especifica un algoritmo hash que se utilizará para realizar las marcas de tiempo compatibles con RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="3315b-126">Specifies a hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="3315b-127">Este parámetro se omite para las marcas de tiempo de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="3315b-127">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="3315b-128">*psRequest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3315b-128">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3315b-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3315b-129">Optional.</span></span> <span data-ttu-id="3315b-130">Dirección de una estructura [**de \_ atributos de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3315b-130">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="3315b-131">Este parámetro es opcional y puede ser **null** si no se incluye.</span><span class="sxs-lookup"><span data-stu-id="3315b-131">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="3315b-132">*pSipData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3315b-132">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3315b-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3315b-133">Optional.</span></span> <span data-ttu-id="3315b-134">Valor de 32 bits que se pasa como datos adicionales a las funciones del [*paquete de interfaz de asunto*](../secgloss/s-gly.md) (SIP).</span><span class="sxs-lookup"><span data-stu-id="3315b-134">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="3315b-135">El proveedor SIP define el formato y el contenido de este parámetro.</span><span class="sxs-lookup"><span data-stu-id="3315b-135">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="3315b-136">Este parámetro es opcional y puede ser **null** si no se incluye.</span><span class="sxs-lookup"><span data-stu-id="3315b-136">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="3315b-137">*ppSignerContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3315b-137">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3315b-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3315b-138">Optional.</span></span> <span data-ttu-id="3315b-139">Dirección de un puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que contiene el BLOB firmado.</span><span class="sxs-lookup"><span data-stu-id="3315b-139">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="3315b-140">Cuando haya terminado de usar la estructura de **\_ contexto del firmante** , libere la llamada a la función [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="3315b-140">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3315b-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3315b-141">Return value</span></span>

<span data-ttu-id="3315b-142">Si la función se ejecuta correctamente, la función devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3315b-142">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="3315b-143">Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="3315b-143">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="3315b-144">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="3315b-144">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3315b-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3315b-145">Requirements</span></span>



| <span data-ttu-id="3315b-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3315b-146">Requirement</span></span> | <span data-ttu-id="3315b-147">Value</span><span class="sxs-lookup"><span data-stu-id="3315b-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3315b-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3315b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3315b-149">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3315b-149">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3315b-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3315b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3315b-151">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3315b-151">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3315b-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3315b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3315b-153"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3315b-153"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3315b-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="3315b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3315b-155">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="3315b-155">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="3315b-156">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="3315b-156">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> </dl>

 

 
