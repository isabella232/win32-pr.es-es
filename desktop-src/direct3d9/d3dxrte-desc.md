---
description: Describe un destino de representación fuera de la pantalla utilizado por una instancia de ID3DXRenderToEnvMap.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: D3DXRTE_DESC estructura (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280307"
---
# <a name="d3dxrte_desc-structure"></a><span data-ttu-id="e41c8-103">D3DXRTE \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="e41c8-103">D3DXRTE\_DESC structure</span></span>

<span data-ttu-id="e41c8-104">Describe un destino de representación fuera de la pantalla utilizado por una instancia de [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span><span class="sxs-lookup"><span data-stu-id="e41c8-104">Describes an off-screen render target used by an instance of [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e41c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e41c8-105">Syntax</span></span>


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a><span data-ttu-id="e41c8-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e41c8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e41c8-107">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="e41c8-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="e41c8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e41c8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e41c8-109">Ancho y alto en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e41c8-109">Width and height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e41c8-110">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="e41c8-110">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="e41c8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e41c8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e41c8-112">Número máximo de niveles de detalle (LOD).</span><span class="sxs-lookup"><span data-stu-id="e41c8-112">Maximum level of detail (LOD) number.</span></span>

</dd> <dt>

<span data-ttu-id="e41c8-113">**Format**</span><span class="sxs-lookup"><span data-stu-id="e41c8-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="e41c8-114">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e41c8-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e41c8-115">Formato de búfer de color.</span><span class="sxs-lookup"><span data-stu-id="e41c8-115">Color buffer format.</span></span>

</dd> <dt>

<span data-ttu-id="e41c8-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="e41c8-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="e41c8-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e41c8-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e41c8-118">Indica si se necesita el búfer z.</span><span class="sxs-lookup"><span data-stu-id="e41c8-118">Indicates if the z-buffer is needed.</span></span>

</dd> <dt>

<span data-ttu-id="e41c8-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="e41c8-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="e41c8-120">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e41c8-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e41c8-121">Formato del búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="e41c8-121">Format of the depth buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e41c8-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e41c8-122">Remarks</span></span>

<span data-ttu-id="e41c8-123">Este método se usa para devolver los parámetros de creación que se usan al crear un objeto [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="e41c8-123">This method is used to return the creation parameters used when creating an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41c8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e41c8-124">Requirements</span></span>



| <span data-ttu-id="e41c8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e41c8-125">Requirement</span></span> | <span data-ttu-id="e41c8-126">Value</span><span class="sxs-lookup"><span data-stu-id="e41c8-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e41c8-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e41c8-127">Header</span></span><br/> | <dl> <span data-ttu-id="e41c8-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e41c8-128"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e41c8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e41c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41c8-130">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="e41c8-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
