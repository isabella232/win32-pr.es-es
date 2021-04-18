---
title: Función UtilStringCopyWithAlloc (Ndattributils. h)
description: Asigna y copia una cadena de origen.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- UtilStringCopyWithAlloc función NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676691"
---
# <a name="utilstringcopywithalloc-function"></a><span data-ttu-id="70f66-104">UtilStringCopyWithAlloc función)</span><span class="sxs-lookup"><span data-stu-id="70f66-104">UtilStringCopyWithAlloc function</span></span>

<span data-ttu-id="70f66-105">La función **UtilStringCopyWithAlloc** asigna y copia una cadena de origen.</span><span class="sxs-lookup"><span data-stu-id="70f66-105">The **UtilStringCopyWithAlloc** function allocates and copies a source string.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f66-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70f66-106">Syntax</span></span>


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a><span data-ttu-id="70f66-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70f66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70f66-108">*Búfer* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="70f66-108">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70f66-109">Tipo: \**LPWStr \** _</span><span class="sxs-lookup"><span data-stu-id="70f66-109">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="70f66-110">La ubicación donde se almacena el puntero a la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="70f66-110">The location where the pointer to the allocated memory is stored.</span></span> <span data-ttu-id="70f66-111">Cuando ya no se necesiten, se debe liberar con [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="70f66-111">When no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="70f66-112">Este búfer siempre termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="70f66-112">This buffer is always null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="70f66-113">*BufferMax* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70f66-113">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70f66-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="70f66-114">Type: **UINT**</span></span>

<span data-ttu-id="70f66-115">Número máximo de caracteres que se van a leer del *origen*.</span><span class="sxs-lookup"><span data-stu-id="70f66-115">The maximum number of characters to read from *Source*.</span></span>

</dd> <dt>

<span data-ttu-id="70f66-116">*Origen* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="70f66-116">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70f66-117">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="70f66-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="70f66-118">Cadena que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="70f66-118">The string to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70f66-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70f66-119">Return value</span></span>

<span data-ttu-id="70f66-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="70f66-120">Type: **HRESULT**</span></span>

<span data-ttu-id="70f66-121">Los valores devueltos posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70f66-121">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="70f66-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="70f66-122">Return code</span></span>                                                                                  | <span data-ttu-id="70f66-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="70f66-123">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="70f66-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="70f66-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="70f66-125">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="70f66-125">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="70f66-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="70f66-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="70f66-127">No se ha proporcionado correctamente uno o más parámetros.</span><span class="sxs-lookup"><span data-stu-id="70f66-127">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="70f66-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70f66-128">Requirements</span></span>



| <span data-ttu-id="70f66-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="70f66-129">Requirement</span></span> | <span data-ttu-id="70f66-130">Value</span><span class="sxs-lookup"><span data-stu-id="70f66-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f66-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70f66-131">Minimum supported client</span></span><br/> | <span data-ttu-id="70f66-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="70f66-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70f66-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70f66-133">Minimum supported server</span></span><br/> | <span data-ttu-id="70f66-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="70f66-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="70f66-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70f66-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="70f66-136"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="70f66-136"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70f66-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="70f66-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70f66-138">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="70f66-138">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[<span data-ttu-id="70f66-139">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="70f66-139">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="70f66-140">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="70f66-140">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> </dl>

 

