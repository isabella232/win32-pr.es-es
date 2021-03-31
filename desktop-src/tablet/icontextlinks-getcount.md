---
description: Obtiene el número de objetos IContextLink de esta colección.
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: 'IContextLinks:: GetCount (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c12fae76eb41bf05d60712cf9f69639c713066c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275477"
---
# <a name="icontextlinksgetcount-method"></a><span data-ttu-id="d0e59-103">IContextLinks:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="d0e59-103">IContextLinks::GetCount method</span></span>

<span data-ttu-id="d0e59-104">Obtiene el número de objetos [**IContextLink**](icontextlink.md) de esta colección.</span><span class="sxs-lookup"><span data-stu-id="d0e59-104">Gets the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e59-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0e59-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="d0e59-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0e59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e59-107">*pulCount* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d0e59-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e59-108">Número de objetos [**IContextLink**](icontextlink.md) contenidos en esta colección.</span><span class="sxs-lookup"><span data-stu-id="d0e59-108">The number of [**IContextLink**](icontextlink.md) objects that are contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e59-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0e59-109">Return value</span></span>

<span data-ttu-id="d0e59-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d0e59-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e59-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0e59-111">Requirements</span></span>



| <span data-ttu-id="d0e59-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0e59-112">Requirement</span></span> | <span data-ttu-id="d0e59-113">Value</span><span class="sxs-lookup"><span data-stu-id="d0e59-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e59-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0e59-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e59-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d0e59-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d0e59-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0e59-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e59-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d0e59-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d0e59-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0e59-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0e59-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d0e59-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d0e59-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0e59-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0e59-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0e59-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d0e59-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0e59-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e59-123">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="d0e59-123">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="d0e59-124">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="d0e59-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




