---
description: 'Método ID3DX10Mesh::D rawSubset: dibuja un subconjunto de una malla.'
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: Método ID3DX10Mesh::D rawSubset (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8441bfe4c5d965733a40816ff2def1015f3eb79c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084043"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="92432-103">Método ID3DX10Mesh::D rawSubset</span><span class="sxs-lookup"><span data-stu-id="92432-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="92432-104">Dibuja un subconjunto de una malla.</span><span class="sxs-lookup"><span data-stu-id="92432-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="92432-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92432-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="92432-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92432-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92432-107">*AttribId* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="92432-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92432-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92432-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92432-109">Especifica qué subconjunto de la malla se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="92432-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="92432-110">Este valor se usa para diferenciar las caras de una malla como pertenecientes a uno o varios grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="92432-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92432-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92432-111">Return value</span></span>

<span data-ttu-id="92432-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92432-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92432-113">El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="92432-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92432-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92432-114">Remarks</span></span>

<span data-ttu-id="92432-115">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras.</span><span class="sxs-lookup"><span data-stu-id="92432-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="92432-116">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado (AttribId) al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="92432-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="92432-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92432-117">Requirements</span></span>



| <span data-ttu-id="92432-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="92432-118">Requirement</span></span> | <span data-ttu-id="92432-119">Value</span><span class="sxs-lookup"><span data-stu-id="92432-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92432-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92432-120">Header</span></span><br/>  | <dl> <span data-ttu-id="92432-121"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="92432-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="92432-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92432-122">Library</span></span><br/> | <dl> <span data-ttu-id="92432-123"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="92432-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92432-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="92432-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92432-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="92432-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="92432-126">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="92432-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
