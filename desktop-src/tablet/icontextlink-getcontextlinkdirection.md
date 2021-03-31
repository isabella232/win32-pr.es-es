---
description: Recupera el tipo de relación que representa este IContextLink.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'IContextLink:: GetContextLinkDirection (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47ad3e6c8d28126c010e5cc1c1419b99d9cde4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275479"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a><span data-ttu-id="c385d-103">IContextLink:: GetContextLinkDirection (método)</span><span class="sxs-lookup"><span data-stu-id="c385d-103">IContextLink::GetContextLinkDirection method</span></span>

<span data-ttu-id="c385d-104">Recupera el tipo de relación que representa este [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="c385d-104">Retrieves the type of relationship this [**IContextLink**](icontextlink.md) represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="c385d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c385d-105">Syntax</span></span>


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a><span data-ttu-id="c385d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c385d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c385d-107">*pContextLinkDirection* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c385d-107">*pContextLinkDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c385d-108">Dirección que representa este [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="c385d-108">The direction this [**IContextLink**](icontextlink.md) represents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c385d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c385d-109">Return value</span></span>

<span data-ttu-id="c385d-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c385d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c385d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c385d-111">Requirements</span></span>



| <span data-ttu-id="c385d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c385d-112">Requirement</span></span> | <span data-ttu-id="c385d-113">Value</span><span class="sxs-lookup"><span data-stu-id="c385d-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c385d-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c385d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c385d-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c385d-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c385d-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c385d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c385d-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c385d-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c385d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c385d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c385d-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c385d-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c385d-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c385d-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c385d-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c385d-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c385d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c385d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c385d-123">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="c385d-123">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="c385d-124">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="c385d-124">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="c385d-125">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c385d-125">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




