---
description: Especifica una referencia a una superficie sin comprimir.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: DXVA_PicEntry_HEVC estructura (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648173"
---
# <a name="dxva_picentry_hevc-structure"></a><span data-ttu-id="17e2b-103">PicEntry de DXVA \_ \_ HEVC estructura</span><span class="sxs-lookup"><span data-stu-id="17e2b-103">DXVA\_PicEntry\_HEVC structure</span></span>

<span data-ttu-id="17e2b-104">Especifica una referencia a una superficie sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="17e2b-104">Specifies a reference to an uncompressed surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e2b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17e2b-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a><span data-ttu-id="17e2b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="17e2b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="17e2b-107">**Index7Bits**</span><span class="sxs-lookup"><span data-stu-id="17e2b-107">**Index7Bits**</span></span>
</dt> <dd>

<span data-ttu-id="17e2b-108">Índice que identifica una superficie sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="17e2b-108">An index that identifies an uncompressed surface .</span></span>

</dd> <dt>

<span data-ttu-id="17e2b-109">**AssociatedFlag**</span><span class="sxs-lookup"><span data-stu-id="17e2b-109">**AssociatedFlag**</span></span> 
</dt> <dd>

<span data-ttu-id="17e2b-110">Marca de 1 bit opcional asociada a la superficie.</span><span class="sxs-lookup"><span data-stu-id="17e2b-110">Optional 1-bit flag associated with the surface.</span></span> <span data-ttu-id="17e2b-111">El significado de la marca depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="17e2b-111">The meaning of the flag depends on the context.</span></span> <span data-ttu-id="17e2b-112">Por ejemplo, puede especificar si el marco de referencia es una referencia a largo plazo o una referencia a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="17e2b-112">For example, it can specify whether the reference frame is a long-term reference or a short-term reference.</span></span>

</dd> <dt>

<span data-ttu-id="17e2b-113">**bPicEntry**</span><span class="sxs-lookup"><span data-stu-id="17e2b-113">**bPicEntry**</span></span>
</dt> <dd>

<span data-ttu-id="17e2b-114">Obtiene acceso a los 8 bits completos de la Unión.</span><span class="sxs-lookup"><span data-stu-id="17e2b-114">Accesses the entire 8 bits of the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17e2b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17e2b-115">Requirements</span></span>



| <span data-ttu-id="17e2b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="17e2b-116">Requirement</span></span> | <span data-ttu-id="17e2b-117">Value</span><span class="sxs-lookup"><span data-stu-id="17e2b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="17e2b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17e2b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17e2b-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="17e2b-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="17e2b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17e2b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17e2b-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="17e2b-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="17e2b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17e2b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="17e2b-123"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="17e2b-123"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e2b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="17e2b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e2b-125">Media Foundation estructuras</span><span class="sxs-lookup"><span data-stu-id="17e2b-125">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




