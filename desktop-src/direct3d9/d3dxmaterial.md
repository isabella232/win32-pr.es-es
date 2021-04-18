---
description: Devuelve información de material guardada en archivos de Direct3D (. x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: Estructura D3DXMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707741"
---
# <a name="d3dxmaterial-structure"></a><span data-ttu-id="97c12-103">Estructura D3DXMATERIAL</span><span class="sxs-lookup"><span data-stu-id="97c12-103">D3DXMATERIAL structure</span></span>

<span data-ttu-id="97c12-104">Devuelve información de material guardada en archivos de Direct3D (. x).</span><span class="sxs-lookup"><span data-stu-id="97c12-104">Returns material information saved in Direct3D (.x) files.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c12-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97c12-105">Syntax</span></span>


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a><span data-ttu-id="97c12-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="97c12-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="97c12-107">**MatD3D**</span><span class="sxs-lookup"><span data-stu-id="97c12-107">**MatD3D**</span></span>
</dt> <dd>

<span data-ttu-id="97c12-108">Tipo: **[ **D3DMATERIAL9**](d3dmaterial9.md)**</span><span class="sxs-lookup"><span data-stu-id="97c12-108">Type: **[**D3DMATERIAL9**](d3dmaterial9.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97c12-109">Estructura [**D3DMATERIAL9**](d3dmaterial9.md) que describe las propiedades del material.</span><span class="sxs-lookup"><span data-stu-id="97c12-109">[**D3DMATERIAL9**](d3dmaterial9.md) structure that describes the material properties.</span></span>

</dd> <dt>

<span data-ttu-id="97c12-110">**pTextureFilename**</span><span class="sxs-lookup"><span data-stu-id="97c12-110">**pTextureFilename**</span></span>
</dt> <dd>

<span data-ttu-id="97c12-111">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="97c12-111">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="97c12-112">Puntero a una cadena que especifica el nombre de archivo de la textura.</span><span class="sxs-lookup"><span data-stu-id="97c12-112">Pointer to a string that specifies the file name of the texture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97c12-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97c12-113">Remarks</span></span>

<span data-ttu-id="97c12-114">Las funciones [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) y [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) devuelven una matriz de estructuras **D3DXMATERIAL** que especifican el color del material y el nombre de la textura de cada material de la malla.</span><span class="sxs-lookup"><span data-stu-id="97c12-114">The [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) and [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) functions return an array of **D3DXMATERIAL** structures that specify the material color and name of the texture for each material in the mesh.</span></span> <span data-ttu-id="97c12-115">A continuación, se requiere la aplicación para cargar la textura.</span><span class="sxs-lookup"><span data-stu-id="97c12-115">The application is then required to load the texture.</span></span>

<span data-ttu-id="97c12-116">El tipo LPD3DXMATERIAL se define como un puntero a la estructura **D3DXMATERIAL** .</span><span class="sxs-lookup"><span data-stu-id="97c12-116">The LPD3DXMATERIAL type is defined as a pointer to the **D3DXMATERIAL** structure.</span></span>


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a><span data-ttu-id="97c12-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97c12-117">Requirements</span></span>



| <span data-ttu-id="97c12-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c12-118">Requirement</span></span> | <span data-ttu-id="97c12-119">Value</span><span class="sxs-lookup"><span data-stu-id="97c12-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97c12-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97c12-120">Header</span></span><br/> | <dl> <span data-ttu-id="97c12-121"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="97c12-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c12-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="97c12-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c12-123">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="97c12-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="97c12-124">**D3DXLoadMeshFromX**</span><span class="sxs-lookup"><span data-stu-id="97c12-124">**D3DXLoadMeshFromX**</span></span>](d3dxloadmeshfromx.md)
</dt> <dt>

[<span data-ttu-id="97c12-125">**D3DXLoadMeshFromXof**</span><span class="sxs-lookup"><span data-stu-id="97c12-125">**D3DXLoadMeshFromXof**</span></span>](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




