---
description: La \_ estructura de elementos KSMULTIPLE describe el tamaño y el recuento de las propiedades de longitud variable en los pin de modo kernel.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: KSMULTIPLE_ITEM estructura (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680614"
---
# <a name="ksmultiple_item-structure"></a><span data-ttu-id="0d3fc-103">\_Estructura del elemento KSMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="0d3fc-103">KSMULTIPLE\_ITEM structure</span></span>

<span data-ttu-id="0d3fc-104">La `KSMULTIPLE_ITEM` estructura describe el tamaño y el recuento de las propiedades de longitud variable en los pin de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-104">The `KSMULTIPLE_ITEM` structure describes the size and count of variable-length properties on kernel-mode pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d3fc-105">Syntax</span></span>


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a><span data-ttu-id="0d3fc-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d3fc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d3fc-107">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="0d3fc-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="0d3fc-108">Tamaño del bloque de memoria devuelto, en bytes.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-108">Size of the returned memory block, in bytes.</span></span> <span data-ttu-id="0d3fc-109">El tamaño incluye la estructura del **\_ elemento KSMULTIPLE** y los elementos que lo siguen.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-109">The size includes the **KSMULTIPLE\_ITEM** structure and the items that follow it.</span></span>

</dd> <dt>

<span data-ttu-id="0d3fc-110">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="0d3fc-110">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="0d3fc-111">Especifica el número total de elementos que siguen a esta estructura.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-111">Specifies the total number of items that follow this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d3fc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d3fc-112">Requirements</span></span>



| <span data-ttu-id="0d3fc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3fc-113">Requirement</span></span> | <span data-ttu-id="0d3fc-114">Value</span><span class="sxs-lookup"><span data-stu-id="0d3fc-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="0d3fc-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d3fc-115">Header</span></span><br/> | <dl> <span data-ttu-id="0d3fc-116"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d3fc-116"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d3fc-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d3fc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3fc-118">Estructuras de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0d3fc-118">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="0d3fc-119">**IKsPin::KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="0d3fc-119">**IKsPin::KsQueryMediums**</span></span>](ikspin-ksquerymediums.md)
</dt> <dt>

[<span data-ttu-id="0d3fc-120">**REGPINMEDIUM**</span><span class="sxs-lookup"><span data-stu-id="0d3fc-120">**REGPINMEDIUM**</span></span>](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




