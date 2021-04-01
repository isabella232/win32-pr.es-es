---
description: Especifica las opciones de simplificación para una malla.
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: Enumeración D3DXMESHSIMP (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157180"
---
# <a name="d3dxmeshsimp-enumeration"></a><span data-ttu-id="9fa32-103">Enumeración D3DXMESHSIMP</span><span class="sxs-lookup"><span data-stu-id="9fa32-103">D3DXMESHSIMP enumeration</span></span>

<span data-ttu-id="9fa32-104">Especifica las opciones de simplificación para una malla.</span><span class="sxs-lookup"><span data-stu-id="9fa32-104">Specifies simplification options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa32-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fa32-105">Syntax</span></span>


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a><span data-ttu-id="9fa32-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9fa32-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9fa32-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**\_Vértice D3DXMESHSIMP**</span><span class="sxs-lookup"><span data-stu-id="9fa32-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP\_VERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="9fa32-108">La malla se simplificará según el número de vértices especificado en el parámetro MinValue.</span><span class="sxs-lookup"><span data-stu-id="9fa32-108">The mesh will be simplified by the number of vertices specified in the MinValue parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9fa32-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP \_**</span><span class="sxs-lookup"><span data-stu-id="9fa32-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP\_FACE**</span></span>
</dt> <dd>

<span data-ttu-id="9fa32-110">La malla se simplificará según el número de caras especificadas en el parámetro MinValue.</span><span class="sxs-lookup"><span data-stu-id="9fa32-110">The mesh will be simplified by the number of faces specified in the MinValue parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fa32-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fa32-111">Requirements</span></span>



| <span data-ttu-id="9fa32-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fa32-112">Requirement</span></span> | <span data-ttu-id="9fa32-113">Value</span><span class="sxs-lookup"><span data-stu-id="9fa32-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa32-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fa32-114">Header</span></span><br/> | <dl> <span data-ttu-id="9fa32-115"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fa32-115"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fa32-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fa32-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa32-117">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="9fa32-117">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="9fa32-118">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="9fa32-118">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 




