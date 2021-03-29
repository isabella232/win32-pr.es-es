---
description: Marca de tiempo el asunto especificado y, opcionalmente, devuelve un puntero a una \_ estructura de contexto del firmante que contiene un puntero a un BLOB.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: SignerTimeStampEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816718"
---
# <a name="signertimestampex-function"></a><span data-ttu-id="6ec8f-103">SignerTimeStampEx función)</span><span class="sxs-lookup"><span data-stu-id="6ec8f-103">SignerTimeStampEx function</span></span>

<span data-ttu-id="6ec8f-104">El tiempo de la función **SignerTimeStampEx** marca el asunto especificado y, opcionalmente, devuelve un puntero a una estructura de [**\_ contexto del firmante**](signer-context.md) que contiene un puntero a un [*BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6ec8f-104">The **SignerTimeStampEx** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="6ec8f-105">Esta función admite la marca de tiempo de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-105">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="6ec8f-106">Para realizar una marca de tiempo de la infraestructura de clave pública (RFC 3161) de X. 509, utilice la función [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="6ec8f-106">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="6ec8f-107">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="6ec8f-108">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6ec8f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ec8f-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="6ec8f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ec8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec8f-111">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ec8f-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec8f-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-112">Reserved.</span></span> <span data-ttu-id="6ec8f-113">Este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-113">This parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6ec8f-114">*pSubjectInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ec8f-114">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec8f-115">Dirección de una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que representa el sujeto de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-115">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="6ec8f-116">*pwszHttpTimeStamp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ec8f-116">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec8f-117">Dirección de una cadena Unicode terminada en null que contiene la dirección URL de un servidor de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-117">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="6ec8f-118">*psRequest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ec8f-118">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec8f-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-119">Optional.</span></span> <span data-ttu-id="6ec8f-120">Dirección de una estructura [**de \_ atributos de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-120">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="6ec8f-121">Este parámetro es opcional y puede ser **null** si no se incluye.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-121">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="6ec8f-122">*pSipData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ec8f-122">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec8f-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-123">Optional.</span></span> <span data-ttu-id="6ec8f-124">Valor de 32 bits que se pasa como datos adicionales a las funciones del [*paquete de interfaz de asunto*](../secgloss/s-gly.md) (SIP).</span><span class="sxs-lookup"><span data-stu-id="6ec8f-124">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="6ec8f-125">El proveedor SIP define el formato y el contenido de este parámetro.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-125">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="6ec8f-126">Este parámetro es opcional y puede ser **null** si no se incluye.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-126">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="6ec8f-127">*ppSignerContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6ec8f-127">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec8f-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-128">Optional.</span></span> <span data-ttu-id="6ec8f-129">Dirección de un puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que contiene el BLOB firmado.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-129">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="6ec8f-130">Cuando haya terminado de usar la estructura de **\_ contexto del firmante** , libere la llamada a la función [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="6ec8f-130">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec8f-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ec8f-131">Return value</span></span>

<span data-ttu-id="6ec8f-132">Si la función se ejecuta correctamente, la función devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-132">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="6ec8f-133">Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="6ec8f-133">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="6ec8f-134">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="6ec8f-134">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec8f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec8f-135">Requirements</span></span>



| <span data-ttu-id="6ec8f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec8f-136">Requirement</span></span> | <span data-ttu-id="6ec8f-137">Value</span><span class="sxs-lookup"><span data-stu-id="6ec8f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec8f-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec8f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec8f-139">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6ec8f-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6ec8f-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec8f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec8f-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ec8f-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ec8f-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ec8f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec8f-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec8f-143"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ec8f-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ec8f-144">See also</span></span>

<dl> <span data-ttu-id="6ec8f-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6ec8f-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="6ec8f-146">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="6ec8f-146">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> </dl>

 

 
