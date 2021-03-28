---
title: Estructura XMINT4
description: Describe un vector entero 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- HLSL de la estructura XMINT4
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302d820428fafb1561bd38850c4f75240ce9094f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362675"
---
# <a name="xmint4-structure"></a><span data-ttu-id="fd792-104">Estructura XMINT4</span><span class="sxs-lookup"><span data-stu-id="fd792-104">XMINT4 structure</span></span>

<span data-ttu-id="fd792-105">Describe un vector entero 4D.</span><span class="sxs-lookup"><span data-stu-id="fd792-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd792-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd792-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="fd792-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd792-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd792-108">**x**</span><span class="sxs-lookup"><span data-stu-id="fd792-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="fd792-109">componente x del vector.</span><span class="sxs-lookup"><span data-stu-id="fd792-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="fd792-110">**y**</span><span class="sxs-lookup"><span data-stu-id="fd792-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="fd792-111">componente y del vector.</span><span class="sxs-lookup"><span data-stu-id="fd792-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="fd792-112">**z**</span><span class="sxs-lookup"><span data-stu-id="fd792-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="fd792-113">componente z del vector.</span><span class="sxs-lookup"><span data-stu-id="fd792-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="fd792-114">**w**</span><span class="sxs-lookup"><span data-stu-id="fd792-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="fd792-115">componente w del vector.</span><span class="sxs-lookup"><span data-stu-id="fd792-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd792-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd792-116">Requirements</span></span>



| <span data-ttu-id="fd792-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd792-117">Requirement</span></span> | <span data-ttu-id="fd792-118">Value</span><span class="sxs-lookup"><span data-stu-id="fd792-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd792-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd792-119">Header</span></span><br/> | <dl> <span data-ttu-id="fd792-120"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="fd792-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd792-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd792-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd792-122">Estructuras</span><span class="sxs-lookup"><span data-stu-id="fd792-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="fd792-123">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="fd792-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





