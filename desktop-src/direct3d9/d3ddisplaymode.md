---
description: Describe el modo de presentación.
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: Estructura D3DDISPLAYMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157156"
---
# <a name="d3ddisplaymode-structure"></a><span data-ttu-id="ea4e3-103">Estructura D3DDISPLAYMODE</span><span class="sxs-lookup"><span data-stu-id="ea4e3-103">D3DDISPLAYMODE structure</span></span>

<span data-ttu-id="ea4e3-104">Describe el modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="ea4e3-104">Describes the display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea4e3-105">Syntax</span></span>


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a><span data-ttu-id="ea4e3-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ea4e3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ea4e3-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="ea4e3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea4e3-109">Ancho de la pantalla, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ea4e3-109">Screen width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ea4e3-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="ea4e3-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea4e3-112">Alto de la pantalla, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ea4e3-112">Screen height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ea4e3-113">**Frecuencia**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-113">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="ea4e3-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea4e3-115">Frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="ea4e3-115">Refresh rate.</span></span> <span data-ttu-id="ea4e3-116">El valor 0 indica un valor predeterminado del adaptador.</span><span class="sxs-lookup"><span data-stu-id="ea4e3-116">The value of 0 indicates an adapter default.</span></span>

</dd> <dt>

<span data-ttu-id="ea4e3-117">**Format**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-117">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="ea4e3-118">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea4e3-119">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de superficie del modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="ea4e3-119">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the display mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea4e3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea4e3-120">Requirements</span></span>



| <span data-ttu-id="ea4e3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea4e3-121">Requirement</span></span> | <span data-ttu-id="ea4e3-122">Value</span><span class="sxs-lookup"><span data-stu-id="ea4e3-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4e3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea4e3-123">Header</span></span><br/> | <dl> <span data-ttu-id="ea4e3-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea4e3-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4e3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea4e3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4e3-126">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="ea4e3-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="ea4e3-127">**EnumAdapterModes**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-127">**EnumAdapterModes**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[<span data-ttu-id="ea4e3-128">**GetAdapterDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-128">**GetAdapterDisplayMode**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[<span data-ttu-id="ea4e3-129">**GetDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="ea4e3-129">**GetDisplayMode**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
