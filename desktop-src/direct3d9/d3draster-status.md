---
description: Describe el estado de la trama.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: D3DRASTER_STATUS estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707926"
---
# <a name="d3draster_status-structure"></a><span data-ttu-id="d899f-103">Estructura de estado de D3DRASTER \_</span><span class="sxs-lookup"><span data-stu-id="d899f-103">D3DRASTER\_STATUS structure</span></span>

<span data-ttu-id="d899f-104">Describe el estado de la trama.</span><span class="sxs-lookup"><span data-stu-id="d899f-104">Describes the raster status.</span></span>

## <a name="syntax"></a><span data-ttu-id="d899f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d899f-105">Syntax</span></span>


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a><span data-ttu-id="d899f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d899f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d899f-107">**InVBlank**</span><span class="sxs-lookup"><span data-stu-id="d899f-107">**InVBlank**</span></span>
</dt> <dd>

<span data-ttu-id="d899f-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d899f-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d899f-109">**True** si la trama está en el período en blanco vertical.</span><span class="sxs-lookup"><span data-stu-id="d899f-109">**TRUE** if the raster is in the vertical blank period.</span></span> <span data-ttu-id="d899f-110">**False** si la trama no está en el período en blanco vertical.</span><span class="sxs-lookup"><span data-stu-id="d899f-110">**FALSE** if the raster is not in the vertical blank period.</span></span>

</dd> <dt>

<span data-ttu-id="d899f-111">**ScanLine**</span><span class="sxs-lookup"><span data-stu-id="d899f-111">**ScanLine**</span></span>
</dt> <dd>

<span data-ttu-id="d899f-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d899f-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d899f-113">Si InVBlank es **false**, este valor es un entero que se corresponde aproximadamente con la línea de recorrido actual dibujada por la trama.</span><span class="sxs-lookup"><span data-stu-id="d899f-113">If InVBlank is **FALSE**, then this value is an integer roughly corresponding to the current scan line painted by the raster.</span></span> <span data-ttu-id="d899f-114">Las líneas de recorrido se numeran de la misma manera que las coordenadas de la superficie de Direct3D: 0 es la parte superior de la superficie principal, que se extiende hasta el valor (alto de la superficie-1) en la parte inferior de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="d899f-114">Scan lines are numbered in the same way as Direct3D surface coordinates: 0 is the top of the primary surface, extending to the value (height of the surface - 1) at the bottom of the display.</span></span>

<span data-ttu-id="d899f-115">Si InVBlank es **true**, este valor se establece en cero y se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="d899f-115">If InVBlank is **TRUE**, then this value is set to zero and can be ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d899f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d899f-116">Requirements</span></span>



| <span data-ttu-id="d899f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d899f-117">Requirement</span></span> | <span data-ttu-id="d899f-118">Value</span><span class="sxs-lookup"><span data-stu-id="d899f-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d899f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d899f-119">Header</span></span><br/> | <dl> <span data-ttu-id="d899f-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d899f-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d899f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d899f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d899f-122">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="d899f-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d899f-123">**GetRasterStatus**</span><span class="sxs-lookup"><span data-stu-id="d899f-123">**GetRasterStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
