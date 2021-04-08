---
description: Marca de tiempo el sujeto especificado. Esta función admite la marca de tiempo de Authenticode. Para realizar una marca de tiempo de la infraestructura de clave pública (RFC 3161) de X. 509, utilice la función SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: SignerTimeStamp función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002667"
---
# <a name="signertimestamp-function"></a><span data-ttu-id="d3066-105">SignerTimeStamp función)</span><span class="sxs-lookup"><span data-stu-id="d3066-105">SignerTimeStamp function</span></span>

<span data-ttu-id="d3066-106">El tiempo de la función **SignerTimeStamp** marca el sujeto especificado.</span><span class="sxs-lookup"><span data-stu-id="d3066-106">The **SignerTimeStamp** function time stamps the specified subject.</span></span> <span data-ttu-id="d3066-107">Esta función admite la marca de tiempo de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="d3066-107">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="d3066-108">Para realizar una marca de tiempo de la infraestructura de clave pública (RFC 3161) de X. 509, utilice la función [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="d3066-108">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="d3066-109">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="d3066-109">This function has no associated header file or import library.</span></span> <span data-ttu-id="d3066-110">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="d3066-110">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d3066-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3066-111">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="d3066-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3066-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3066-113">*pSubjectInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3066-113">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3066-114">Dirección de una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que representa el sujeto de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d3066-114">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="d3066-115">*pwszHttpTimeStamp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3066-115">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3066-116">Dirección de una cadena Unicode terminada en null que contiene la dirección URL de un servidor de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d3066-116">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="d3066-117">*psRequest* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d3066-117">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3066-118">Dirección de una estructura [**de \_ atributos de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d3066-118">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="d3066-119">Este parámetro es opcional y puede ser **null** si no se incluye.</span><span class="sxs-lookup"><span data-stu-id="d3066-119">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="d3066-120">*pSipData* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d3066-120">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3066-121">Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP.</span><span class="sxs-lookup"><span data-stu-id="d3066-121">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="d3066-122">El proveedor SIP define el formato y el contenido de este.</span><span class="sxs-lookup"><span data-stu-id="d3066-122">The format and content of this is defined by the SIP provider.</span></span>

<span data-ttu-id="d3066-123">Este parámetro es opcional y puede ser **null** si no se incluye.</span><span class="sxs-lookup"><span data-stu-id="d3066-123">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3066-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3066-124">Return value</span></span>

<span data-ttu-id="d3066-125">Si la función se ejecuta correctamente, la función devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d3066-125">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="d3066-126">Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="d3066-126">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="d3066-127">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="d3066-127">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3066-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3066-128">Requirements</span></span>



| <span data-ttu-id="d3066-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3066-129">Requirement</span></span> | <span data-ttu-id="d3066-130">Value</span><span class="sxs-lookup"><span data-stu-id="d3066-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3066-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3066-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d3066-132">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d3066-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d3066-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3066-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d3066-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3066-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d3066-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d3066-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3066-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3066-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
