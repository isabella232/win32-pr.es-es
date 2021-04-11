---
description: Estas marcas las utilizan las funciones que operan en uno o varios canales de una textura.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Enumeración D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362726"
---
# <a name="d3dx10_channel_flag-enumeration"></a><span data-ttu-id="a7088-103">\_Enumeración de marcas de canal de D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="a7088-103">D3DX10\_CHANNEL\_FLAG enumeration</span></span>

<span data-ttu-id="a7088-104">Estas marcas las utilizan las funciones que operan en uno o varios canales de una textura.</span><span class="sxs-lookup"><span data-stu-id="a7088-104">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7088-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7088-105">Syntax</span></span>


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="a7088-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a7088-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a7088-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**\_Canal \_ rojo de D3DX10**</span><span class="sxs-lookup"><span data-stu-id="a7088-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="a7088-108">Indica que se debe usar el canal rojo.</span><span class="sxs-lookup"><span data-stu-id="a7088-108">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="a7088-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**\_Azul canal \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="a7088-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="a7088-110">Indica que se debe usar el canal azul.</span><span class="sxs-lookup"><span data-stu-id="a7088-110">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="a7088-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**\_Canal \_ verde de D3DX10**</span><span class="sxs-lookup"><span data-stu-id="a7088-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="a7088-112">Indica que se debe usar el canal verde.</span><span class="sxs-lookup"><span data-stu-id="a7088-112">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="a7088-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**\_Alfa del canal de D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="a7088-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a7088-114">Indica que se debe usar el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="a7088-114">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="a7088-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_Luminancia del canal de D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="a7088-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3DX10\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="a7088-116">Indica el luminaces de los canales rojo, verde y azul que se deben usar.</span><span class="sxs-lookup"><span data-stu-id="a7088-116">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7088-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7088-117">Requirements</span></span>



| <span data-ttu-id="a7088-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7088-118">Requirement</span></span> | <span data-ttu-id="a7088-119">Value</span><span class="sxs-lookup"><span data-stu-id="a7088-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7088-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7088-120">Header</span></span><br/> | <dl> <span data-ttu-id="a7088-121"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7088-121"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7088-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7088-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7088-123">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="a7088-123">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




