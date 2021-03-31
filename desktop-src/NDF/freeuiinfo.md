---
title: Función FreeUiInfo (Ndattributils. h)
description: Desasigna la memoria asignada internamente a una estructura UiInfo.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- FreeUiInfo función NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a96d859faa80e3e2269981d206c96e780d05c37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150096"
---
# <a name="freeuiinfo-function"></a><span data-ttu-id="80061-104">FreeUiInfo función)</span><span class="sxs-lookup"><span data-stu-id="80061-104">FreeUiInfo function</span></span>

<span data-ttu-id="80061-105">La función **FreeUiInfo** desasigna la memoria asignada internamente a una estructura [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) .</span><span class="sxs-lookup"><span data-stu-id="80061-105">The **FreeUiInfo** function deallocates the memory allocated internally to a [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) structure.</span></span> <span data-ttu-id="80061-106">Esta función llama a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desasignar memoria.</span><span class="sxs-lookup"><span data-stu-id="80061-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="80061-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80061-107">Syntax</span></span>


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="80061-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80061-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80061-109">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80061-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80061-110">Tipo: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="80061-110">Type: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\** _</span></span>

<span data-ttu-id="80061-111">Estructura.</span><span class="sxs-lookup"><span data-stu-id="80061-111">The structure.</span></span> <span data-ttu-id="80061-112">La memoria asignada a la que apunta esta estructura se liberará.</span><span class="sxs-lookup"><span data-stu-id="80061-112">The allocated memory pointed to by this structure will be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80061-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80061-113">Return value</span></span>

<span data-ttu-id="80061-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="80061-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="80061-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80061-115">Requirements</span></span>



| <span data-ttu-id="80061-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="80061-116">Requirement</span></span> | <span data-ttu-id="80061-117">Value</span><span class="sxs-lookup"><span data-stu-id="80061-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="80061-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80061-118">Minimum supported client</span></span><br/> | <span data-ttu-id="80061-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="80061-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="80061-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80061-120">Minimum supported server</span></span><br/> | <span data-ttu-id="80061-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="80061-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="80061-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80061-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="80061-123"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="80061-123"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80061-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="80061-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80061-125">_ *UiInfo*\*</span><span class="sxs-lookup"><span data-stu-id="80061-125">_ *UiInfo*\*</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[<span data-ttu-id="80061-126">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="80061-126">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

