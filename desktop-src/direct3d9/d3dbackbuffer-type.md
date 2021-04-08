---
description: Define constantes que describen el tipo de búfer de reserva.
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: Enumeración D3DBACKBUFFER_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1641b37242339173fc5f591280d8e2beeff6a9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003783"
---
# <a name="d3dbackbuffer_type-enumeration"></a><span data-ttu-id="739bc-103">\_Enumeración de tipo D3DBACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="739bc-103">D3DBACKBUFFER\_TYPE enumeration</span></span>

<span data-ttu-id="739bc-104">Define constantes que describen el tipo de búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="739bc-104">Defines constants that describe the type of back buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="739bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="739bc-105">Syntax</span></span>


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="739bc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="739bc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="739bc-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER \_ tipo \_ mono**</span><span class="sxs-lookup"><span data-stu-id="739bc-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER\_TYPE\_MONO**</span></span>
</dt> <dd>

<span data-ttu-id="739bc-108">Especifica una cadena de intercambio no estéreo.</span><span class="sxs-lookup"><span data-stu-id="739bc-108">Specifies a nonstereo swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="739bc-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER \_ tipo \_ izquierdo**</span><span class="sxs-lookup"><span data-stu-id="739bc-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER\_TYPE\_LEFT**</span></span>
</dt> <dd>

<span data-ttu-id="739bc-110">Especifica el lado izquierdo de un par estéreo en una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="739bc-110">Specifies the left side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="739bc-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER \_ tipo \_ derecho**</span><span class="sxs-lookup"><span data-stu-id="739bc-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER\_TYPE\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="739bc-112">Especifica el lado derecho de un par estéreo en una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="739bc-112">Specifies the right side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="739bc-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER \_ tipo \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="739bc-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER\_TYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="739bc-114">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="739bc-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="739bc-115">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="739bc-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="739bc-116">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="739bc-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="739bc-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="739bc-117">Remarks</span></span>

<span data-ttu-id="739bc-118">Direct3D 9 no admite la vista estéreo, por lo que Direct3D no usa los \_ \_ valores de tipo D3DBACKBUFFER izquierdo y D3DBACKBUFFER \_ tipo \_ right de este tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="739bc-118">Direct3D 9 does not support stereo view, so Direct3D does not use the D3DBACKBUFFER\_TYPE\_LEFT and D3DBACKBUFFER\_TYPE\_RIGHT values of this enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="739bc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="739bc-119">Requirements</span></span>



| <span data-ttu-id="739bc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="739bc-120">Requirement</span></span> | <span data-ttu-id="739bc-121">Value</span><span class="sxs-lookup"><span data-stu-id="739bc-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="739bc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="739bc-122">Header</span></span><br/> | <dl> <span data-ttu-id="739bc-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="739bc-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="739bc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="739bc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="739bc-125">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="739bc-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="739bc-126">**IDirect3DDevice9::GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="739bc-126">**IDirect3DDevice9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[<span data-ttu-id="739bc-127">**IDirect3DSwapChain9::GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="739bc-127">**IDirect3DSwapChain9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
