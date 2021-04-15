---
description: Describe una región rectangular bloqueada.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: D3DLOCKED_RECT estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547966"
---
# <a name="d3dlocked_rect-structure"></a><span data-ttu-id="862a2-103">D3DLOCKED \_ Rect (estructura)</span><span class="sxs-lookup"><span data-stu-id="862a2-103">D3DLOCKED\_RECT structure</span></span>

<span data-ttu-id="862a2-104">Describe una región rectangular bloqueada.</span><span class="sxs-lookup"><span data-stu-id="862a2-104">Describes a locked rectangular region.</span></span>

## <a name="syntax"></a><span data-ttu-id="862a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="862a2-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a><span data-ttu-id="862a2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="862a2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="862a2-107">**Inclinación**</span><span class="sxs-lookup"><span data-stu-id="862a2-107">**Pitch**</span></span>
</dt> <dd>

<span data-ttu-id="862a2-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="862a2-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="862a2-109">Número de bytes en una fila de la superficie.</span><span class="sxs-lookup"><span data-stu-id="862a2-109">Number of bytes in one row of the surface.</span></span>

</dd> <dt>

<span data-ttu-id="862a2-110">**pBits**</span><span class="sxs-lookup"><span data-stu-id="862a2-110">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="862a2-111">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="862a2-111">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="862a2-112">Puntero a los bits bloqueados.</span><span class="sxs-lookup"><span data-stu-id="862a2-112">Pointer to the locked bits.</span></span> <span data-ttu-id="862a2-113">Si se proporcionó un [**Rect**](/previous-versions//dd162897(v=vs.85)) a la llamada [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , pBits se desplazará correctamente desde el inicio de la superficie.</span><span class="sxs-lookup"><span data-stu-id="862a2-113">If a [**RECT**](/previous-versions//dd162897(v=vs.85)) was provided to the [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) call, pBits will be appropriately offset from the start of the surface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="862a2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="862a2-114">Remarks</span></span>

<span data-ttu-id="862a2-115">El paso de los formatos DXTn es diferente de lo que se devolvió en DirectX 7.</span><span class="sxs-lookup"><span data-stu-id="862a2-115">The pitch for DXTn formats is different from what was returned in DirectX 7.</span></span> <span data-ttu-id="862a2-116">Ahora hace referencia al número de bytes de una fila de bloques.</span><span class="sxs-lookup"><span data-stu-id="862a2-116">It now refers to the number of bytes in a row of blocks.</span></span> <span data-ttu-id="862a2-117">Por ejemplo, si tiene un ancho de 16, tendrá un paso de 4 bloques (4 \* 8 para DXT1, 4 \* 16 para DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="862a2-117">For example, if you have a width of 16, then you will have a pitch of 4 blocks (4\*8 for DXT1, 4\*16 for DXT2-5.)</span></span>

## <a name="requirements"></a><span data-ttu-id="862a2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="862a2-118">Requirements</span></span>



| <span data-ttu-id="862a2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="862a2-119">Requirement</span></span> | <span data-ttu-id="862a2-120">Value</span><span class="sxs-lookup"><span data-stu-id="862a2-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="862a2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="862a2-121">Header</span></span><br/> | <dl> <span data-ttu-id="862a2-122"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="862a2-122"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="862a2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="862a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862a2-124">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="862a2-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="862a2-125">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="862a2-125">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="862a2-126">**IDirect3DSurface9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="862a2-126">**IDirect3DSurface9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[<span data-ttu-id="862a2-127">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="862a2-127">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
