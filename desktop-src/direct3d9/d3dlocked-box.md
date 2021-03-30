---
description: Describe un cuadro bloqueado (volumen).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: D3DLOCKED_BOX estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280374"
---
# <a name="d3dlocked_box-structure"></a><span data-ttu-id="d8b05-103">Estructura del cuadro de D3DLOCKED \_</span><span class="sxs-lookup"><span data-stu-id="d8b05-103">D3DLOCKED\_BOX structure</span></span>

<span data-ttu-id="d8b05-104">Describe un cuadro bloqueado (volumen).</span><span class="sxs-lookup"><span data-stu-id="d8b05-104">Describes a locked box (volume).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b05-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8b05-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a><span data-ttu-id="d8b05-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d8b05-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8b05-107">**RowPitch**</span><span class="sxs-lookup"><span data-stu-id="d8b05-107">**RowPitch**</span></span>
</dt> <dd>

<span data-ttu-id="d8b05-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8b05-108">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d8b05-109">Desplazamiento en bytes desde el borde izquierdo de una fila hasta el borde izquierdo de la fila siguiente.</span><span class="sxs-lookup"><span data-stu-id="d8b05-109">Byte offset from the left edge of one row to the left edge of the next row.</span></span>

</dd> <dt>

<span data-ttu-id="d8b05-110">**SlicePitch**</span><span class="sxs-lookup"><span data-stu-id="d8b05-110">**SlicePitch**</span></span>
</dt> <dd>

<span data-ttu-id="d8b05-111">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8b05-111">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d8b05-112">Desplazamiento de bytes desde la parte superior izquierda de un segmento hasta la parte superior izquierda del siguiente segmento más profundo.</span><span class="sxs-lookup"><span data-stu-id="d8b05-112">Byte offset from the top-left of one slice to the top-left of the next deepest slice.</span></span>

</dd> <dt>

<span data-ttu-id="d8b05-113">**pBits**</span><span class="sxs-lookup"><span data-stu-id="d8b05-113">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="d8b05-114">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="d8b05-114">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="d8b05-115">Puntero al principio del cuadro volumen.</span><span class="sxs-lookup"><span data-stu-id="d8b05-115">Pointer to the beginning of the volume box.</span></span> <span data-ttu-id="d8b05-116">Si se proporcionó un [**D3DBOX**](d3dbox.md) a la llamada de Lockbox, pBits se desplazará correctamente desde el inicio del volumen.</span><span class="sxs-lookup"><span data-stu-id="d8b05-116">If a [**D3DBOX**](d3dbox.md) was provided to the LockBox call, pBits will be appropriately offset from the start of the volume.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8b05-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8b05-117">Remarks</span></span>

<span data-ttu-id="d8b05-118">Los volúmenes se pueden visualizar como organizados en segmentos de superficies 2D de ancho x alto apiladas para crear un volumen x alto x de profundidad.</span><span class="sxs-lookup"><span data-stu-id="d8b05-118">Volumes can be visualized as being organized into slices of width x height 2D surfaces stacked up to make a width x height x depth volume.</span></span> <span data-ttu-id="d8b05-119">Para obtener más información, vea [recursos de textura de volumen (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="d8b05-119">For more information, see [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b05-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8b05-120">Requirements</span></span>



| <span data-ttu-id="d8b05-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8b05-121">Requirement</span></span> | <span data-ttu-id="d8b05-122">Value</span><span class="sxs-lookup"><span data-stu-id="d8b05-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b05-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8b05-123">Header</span></span><br/> | <dl> <span data-ttu-id="d8b05-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b05-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b05-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8b05-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b05-126">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="d8b05-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d8b05-127">**IDirect3DVolume9:: LockBox**</span><span class="sxs-lookup"><span data-stu-id="d8b05-127">**IDirect3DVolume9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="d8b05-128">**IDirect3DVolumeTexture9:: LockBox**</span><span class="sxs-lookup"><span data-stu-id="d8b05-128">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
