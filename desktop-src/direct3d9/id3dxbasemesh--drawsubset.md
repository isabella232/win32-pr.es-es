---
description: Dibuja un subconjunto de una malla.
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: ID3DXBaseMesh::D método rawSubset (D3DX9Mesh. h)
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
ms.openlocfilehash: d0da6e9fc57e0fc5e7b4b263ba3d97185333881c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707851"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="a2dc6-103">ID3DXBaseMesh::D método rawSubset</span><span class="sxs-lookup"><span data-stu-id="a2dc6-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="a2dc6-104">Dibuja un subconjunto de una malla.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2dc6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2dc6-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="a2dc6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2dc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2dc6-107">*AttribId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2dc6-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2dc6-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2dc6-109">DWORD que especifica el subconjunto de la malla que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="a2dc6-110">Este valor se usa para diferenciar caras en una malla como perteneciente a uno o varios grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2dc6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2dc6-111">Return value</span></span>

<span data-ttu-id="a2dc6-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2dc6-113">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a2dc6-114">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2dc6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2dc6-115">Remarks</span></span>

<span data-ttu-id="a2dc6-116">El subconjunto especificado por AttribId se representará mediante el método [**rawindexedprimitive de IDirect3DDevice9::D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) , mediante el \_ tipo primitivo D3DPT TRIANGLELIST, por lo que un búfer de índice debe estar inicializado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="a2dc6-117">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con distintas texturas, Estados de representación, materiales, etc.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="a2dc6-118">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla sin dibujar un identificador de atributo determinado (*AttribId*) al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2dc6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2dc6-119">Requirements</span></span>



| <span data-ttu-id="a2dc6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2dc6-120">Requirement</span></span> | <span data-ttu-id="a2dc6-121">Value</span><span class="sxs-lookup"><span data-stu-id="a2dc6-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2dc6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2dc6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a2dc6-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2dc6-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a2dc6-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2dc6-124">Library</span></span><br/> | <dl> <span data-ttu-id="a2dc6-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2dc6-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a2dc6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2dc6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2dc6-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="a2dc6-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
