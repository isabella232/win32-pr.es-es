---
title: Función UtilLoadStringWithAlloc (Ndattributils. h)
description: Asigna y carga una cadena fuera de la tabla de recursos.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- UtilLoadStringWithAlloc función NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151226"
---
# <a name="utilloadstringwithalloc-function"></a><span data-ttu-id="e630d-104">UtilLoadStringWithAlloc función)</span><span class="sxs-lookup"><span data-stu-id="e630d-104">UtilLoadStringWithAlloc function</span></span>

<span data-ttu-id="e630d-105">La función **UtilLoadStringWithAlloc** asigna y carga una cadena fuera de la tabla de recursos.</span><span class="sxs-lookup"><span data-stu-id="e630d-105">The **UtilLoadStringWithAlloc** function allocates and loads a string out of the resource table.</span></span>

## <a name="syntax"></a><span data-ttu-id="e630d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e630d-106">Syntax</span></span>


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a><span data-ttu-id="e630d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e630d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e630d-108">*uID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e630d-108">*uID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e630d-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e630d-109">Type: **UINT**</span></span>

<span data-ttu-id="e630d-110">Identificador de de la cadena que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="e630d-110">Identifier of of the string to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e630d-111">*ppwzBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e630d-111">*ppwzBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e630d-112">Tipo: \**LPWStr \** _</span><span class="sxs-lookup"><span data-stu-id="e630d-112">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="e630d-113">Ubicación donde se colocará la cadena recién asignada.</span><span class="sxs-lookup"><span data-stu-id="e630d-113">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="e630d-114">La cadena se debe liberar mediante [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) cuando ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="e630d-114">The string must be freed using [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) when it is no longer needed.</span></span>

</dd> <dt>

<span data-ttu-id="e630d-115">*cchBufferMax* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e630d-115">*cchBufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e630d-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e630d-116">Type: **UINT**</span></span>

<span data-ttu-id="e630d-117">Número máximo de caracteres que se van a cargar desde la tabla de recursos.</span><span class="sxs-lookup"><span data-stu-id="e630d-117">The maximum number of characters to load from the resource table.</span></span> <span data-ttu-id="e630d-118">Si la cadena de recursos es mayor que el número de caracteres especificado, se trunca y termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="e630d-118">If the resource string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="e630d-119">Este parámetro no se puede establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="e630d-119">This parameter may not be set to zero.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e630d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e630d-120">Return value</span></span>

<span data-ttu-id="e630d-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e630d-121">Type: **HRESULT**</span></span>

<span data-ttu-id="e630d-122">Los valores devueltos posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="e630d-122">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="e630d-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e630d-123">Return code</span></span>                                                                                  | <span data-ttu-id="e630d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e630d-124">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e630d-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e630d-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e630d-126">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e630d-126">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="e630d-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e630d-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e630d-128">No se ha proporcionado correctamente uno o más parámetros.</span><span class="sxs-lookup"><span data-stu-id="e630d-128">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e630d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e630d-129">Requirements</span></span>



| <span data-ttu-id="e630d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e630d-130">Requirement</span></span> | <span data-ttu-id="e630d-131">Value</span><span class="sxs-lookup"><span data-stu-id="e630d-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e630d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e630d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e630d-133">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e630d-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e630d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e630d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e630d-135">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e630d-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e630d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e630d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e630d-137"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="e630d-137"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e630d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e630d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e630d-139">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="e630d-139">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="e630d-140">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="e630d-140">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="e630d-141">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="e630d-141">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

