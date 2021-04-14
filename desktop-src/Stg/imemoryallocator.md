---
title: Clase IMemoryAllocator
description: Implementado por el asignador de memoria para la función StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Almacenamiento estructurado de la clase IMemoryAllocator
- Clase IMemoryAllocator almacenamiento estructurado, descrito
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422366"
---
# <a name="imemoryallocator-class"></a><span data-ttu-id="a86c3-105">Clase IMemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="a86c3-105">IMemoryAllocator class</span></span>

<span data-ttu-id="a86c3-106">La clase **IMemoryAllocator** se implementa mediante el asignador de memoria para la función [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="a86c3-106">The **IMemoryAllocator** class is implemented by the memory allocator for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="methods"></a><span data-ttu-id="a86c3-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a86c3-107">Methods</span></span>



| <span data-ttu-id="a86c3-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="a86c3-108">Name</span></span>                                                     | <span data-ttu-id="a86c3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a86c3-109">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a86c3-110">**Asignación**</span><span class="sxs-lookup"><span data-stu-id="a86c3-110">**Allocate**</span></span>](imemoryallocator-allocate.md)<br/> | <span data-ttu-id="a86c3-111">Asigna memoria para la función [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) cuando la función convierte un tipo de datos **SERIALIZEDPROPERTYVALUE** en un tipo de datos **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="a86c3-111">Allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span><br/> |
| [<span data-ttu-id="a86c3-112">**Gratuito**</span><span class="sxs-lookup"><span data-stu-id="a86c3-112">**Free**</span></span>](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | <span data-ttu-id="a86c3-113">Libera la memoria asignada por el método [**allocate**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="a86c3-113">Frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span><br/>                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="a86c3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a86c3-114">Remarks</span></span>

<span data-ttu-id="a86c3-115">Esta clase solo la usa la función [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="a86c3-115">This class is only used by the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a86c3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a86c3-116">Requirements</span></span>



| <span data-ttu-id="a86c3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a86c3-117">Requirement</span></span> | <span data-ttu-id="a86c3-118">Value</span><span class="sxs-lookup"><span data-stu-id="a86c3-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a86c3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a86c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a86c3-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a86c3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a86c3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a86c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a86c3-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a86c3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a86c3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a86c3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a86c3-124"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a86c3-124"><dt>Ole32.lib</dt></span></span> </dl> |



 

