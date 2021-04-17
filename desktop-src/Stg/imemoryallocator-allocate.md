---
title: IMemoryAllocator allocate (método)
description: El método allocate asigna memoria para la función StgConvertPropertyToVariant cuando la función convierte un tipo de datos SERIALIZEDPROPERTYVALUE en un tipo de datos PROPVARIANT.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Asignar almacenamiento estructurado de método
- Asignar almacenamiento estructurado de método, interfaz IMemoryAllocator
- IMemoryAllocator interface Structured Storage, allocate (método)
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665913"
---
# <a name="imemoryallocatorallocate-method"></a><span data-ttu-id="2ba4a-106">IMemoryAllocator:: Allocate (método)</span><span class="sxs-lookup"><span data-stu-id="2ba4a-106">IMemoryAllocator::Allocate method</span></span>

<span data-ttu-id="2ba4a-107">El método **allocate asigna** memoria para la función [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) cuando la función convierte un tipo de datos **SERIALIZEDPROPERTYVALUE** en un tipo de datos **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="2ba4a-107">The **Allocate** method allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba4a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ba4a-108">Syntax</span></span>


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="2ba4a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ba4a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ba4a-110">*cbSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ba4a-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba4a-111">Especifica el tamaño de la memoria que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="2ba4a-111">Specifies the size of memory to be allocated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ba4a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ba4a-112">Requirements</span></span>



| <span data-ttu-id="2ba4a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ba4a-113">Requirement</span></span> | <span data-ttu-id="2ba4a-114">Value</span><span class="sxs-lookup"><span data-stu-id="2ba4a-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba4a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ba4a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2ba4a-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2ba4a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2ba4a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ba4a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2ba4a-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ba4a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2ba4a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ba4a-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ba4a-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ba4a-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

