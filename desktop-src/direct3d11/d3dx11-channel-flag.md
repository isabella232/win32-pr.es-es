---
title: Enumeración D3DX11_CHANNEL_FLAG (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Estas marcas las utilizan las funciones que operan en uno o varios canales de una textura.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- Enumeración de D3DX11_CHANNEL_FLAG Direct3D 11
- LPD3DX11_CHANNEL_FLAG puntero de enumeración Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424523"
---
# <a name="d3dx11_channel_flag-enumeration"></a><span data-ttu-id="11dc6-106">\_Enumeración de marcas de canal de D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="11dc6-106">D3DX11\_CHANNEL\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="11dc6-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="11dc6-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="11dc6-108">Estas marcas las utilizan las funciones que operan en uno o varios canales de una textura.</span><span class="sxs-lookup"><span data-stu-id="11dc6-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="11dc6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11dc6-109">Syntax</span></span>


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="11dc6-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="11dc6-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="11dc6-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**\_Canal \_ rojo de D3DX11**</span><span class="sxs-lookup"><span data-stu-id="11dc6-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="11dc6-112">Indica que se debe usar el canal rojo.</span><span class="sxs-lookup"><span data-stu-id="11dc6-112">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="11dc6-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**\_Azul canal \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="11dc6-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="11dc6-114">Indica que se debe usar el canal azul.</span><span class="sxs-lookup"><span data-stu-id="11dc6-114">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="11dc6-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**\_Canal \_ verde de D3DX11**</span><span class="sxs-lookup"><span data-stu-id="11dc6-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="11dc6-116">Indica que se debe usar el canal verde.</span><span class="sxs-lookup"><span data-stu-id="11dc6-116">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="11dc6-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**\_Alfa del canal de D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="11dc6-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="11dc6-118">Indica que se debe usar el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="11dc6-118">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="11dc6-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**\_Luminancia del canal de D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="11dc6-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="11dc6-120">Indica el luminaces de los canales rojo, verde y azul que se deben usar.</span><span class="sxs-lookup"><span data-stu-id="11dc6-120">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11dc6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11dc6-121">Requirements</span></span>



| <span data-ttu-id="11dc6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="11dc6-122">Requirement</span></span> | <span data-ttu-id="11dc6-123">Value</span><span class="sxs-lookup"><span data-stu-id="11dc6-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11dc6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11dc6-124">Header</span></span><br/> | <dl> <span data-ttu-id="11dc6-125"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="11dc6-125"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11dc6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="11dc6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11dc6-127">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="11dc6-127">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





