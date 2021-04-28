---
description: 'Método ID3DXBaseMesh::D rawSubset: dibuja un subconjunto de una malla.'
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: Método ID3DXBaseMesh::D rawSubset (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 252c9b9921c7eafd8f0c2a54cfa14a85e91b8f7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115473"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="2840f-103">Método ID3DXBaseMesh::D rawSubset</span><span class="sxs-lookup"><span data-stu-id="2840f-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="2840f-104">Dibuja un subconjunto de una malla.</span><span class="sxs-lookup"><span data-stu-id="2840f-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="2840f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2840f-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="2840f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2840f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2840f-107">*AttribId* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2840f-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2840f-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2840f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2840f-109">DWORD que especifica qué subconjunto de la malla se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="2840f-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="2840f-110">Este valor se usa para diferenciar las caras de una malla como pertenecientes a uno o varios grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="2840f-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2840f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2840f-111">Return value</span></span>

<span data-ttu-id="2840f-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2840f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2840f-113">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2840f-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2840f-114">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2840f-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2840f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2840f-115">Remarks</span></span>

<span data-ttu-id="2840f-116">El subconjunto especificado por AttribId se representará mediante el método [**IDirect3DDevice9::D rawIndexedPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) mediante el tipo primitivo D3DPT TRIANGLELIST, por lo que se debe inicializar correctamente un búfer de \_ índice.</span><span class="sxs-lookup"><span data-stu-id="2840f-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="2840f-117">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras.</span><span class="sxs-lookup"><span data-stu-id="2840f-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="2840f-118">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado (*AttribId*) al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="2840f-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="2840f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2840f-119">Requirements</span></span>



| <span data-ttu-id="2840f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2840f-120">Requirement</span></span> | <span data-ttu-id="2840f-121">Value</span><span class="sxs-lookup"><span data-stu-id="2840f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2840f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2840f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2840f-123"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="2840f-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2840f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2840f-124">Library</span></span><br/> | <dl> <span data-ttu-id="2840f-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2840f-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2840f-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2840f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2840f-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="2840f-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
