---
description: Recupera el número de objetos IContextNode contenidos en esta colección.
ms.assetid: 7cc60bea-9a4c-4ac8-ad1a-0fca5e941c5e
title: 'IContextNodes:: GetCount (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d694849b3436f9f30a687579362d01a111ace80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154429"
---
# <a name="icontextnodesgetcount-method"></a><span data-ttu-id="aa6f2-103">IContextNodes:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="aa6f2-103">IContextNodes::GetCount method</span></span>

<span data-ttu-id="aa6f2-104">Recupera el número de objetos [**IContextNode**](icontextnode.md) contenidos en esta colección.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-104">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa6f2-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="aa6f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa6f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa6f2-107">*pulCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa6f2-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6f2-108">Número de objetos [**IContextNode**](icontextnode.md) contenidos en esta colección.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-108">The number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa6f2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa6f2-109">Return value</span></span>

<span data-ttu-id="aa6f2-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="aa6f2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa6f2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa6f2-111">Requirements</span></span>



| <span data-ttu-id="aa6f2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa6f2-112">Requirement</span></span> | <span data-ttu-id="aa6f2-113">Value</span><span class="sxs-lookup"><span data-stu-id="aa6f2-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa6f2-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa6f2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="aa6f2-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="aa6f2-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aa6f2-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa6f2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="aa6f2-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="aa6f2-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="aa6f2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa6f2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa6f2-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="aa6f2-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="aa6f2-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa6f2-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa6f2-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa6f2-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="aa6f2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa6f2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa6f2-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="aa6f2-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="aa6f2-124">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="aa6f2-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




