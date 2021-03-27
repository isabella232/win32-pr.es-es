---
title: Estructura XMUINT4
description: Describe un vector entero de 4D sin signo.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- HLSL de la estructura XMUINT4
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986772"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="63471-104">Estructura XMUINT4</span><span class="sxs-lookup"><span data-stu-id="63471-104">XMUINT4 structure</span></span>

<span data-ttu-id="63471-105">Describe un vector entero de 4D sin signo.</span><span class="sxs-lookup"><span data-stu-id="63471-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="63471-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63471-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="63471-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="63471-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="63471-108">**x**</span><span class="sxs-lookup"><span data-stu-id="63471-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="63471-109">componente x del vector.</span><span class="sxs-lookup"><span data-stu-id="63471-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="63471-110">**y**</span><span class="sxs-lookup"><span data-stu-id="63471-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="63471-111">componente y del vector.</span><span class="sxs-lookup"><span data-stu-id="63471-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="63471-112">**z**</span><span class="sxs-lookup"><span data-stu-id="63471-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="63471-113">componente z del vector.</span><span class="sxs-lookup"><span data-stu-id="63471-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="63471-114">**w**</span><span class="sxs-lookup"><span data-stu-id="63471-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="63471-115">componente w del vector.</span><span class="sxs-lookup"><span data-stu-id="63471-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63471-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63471-116">Requirements</span></span>



| <span data-ttu-id="63471-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="63471-117">Requirement</span></span> | <span data-ttu-id="63471-118">Value</span><span class="sxs-lookup"><span data-stu-id="63471-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63471-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63471-119">Header</span></span><br/> | <dl> <span data-ttu-id="63471-120"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="63471-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63471-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="63471-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63471-122">Estructuras</span><span class="sxs-lookup"><span data-stu-id="63471-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="63471-123">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="63471-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





