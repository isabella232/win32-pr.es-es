---
description: 'Método ID3DXMATRIXStack::LoadIdentity (D3DX10.h): carga la identidad en la matriz actual.'
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: Método ID3DXMATRIXStack::LoadIdentity (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f056a911b19c0ea18f5f728a6ce8c4403dd14587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107993"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="2033b-103">Método ID3DXMATRIXStack::LoadIdentity (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="2033b-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="2033b-104">Carga la identidad en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="2033b-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2033b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2033b-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="2033b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2033b-106">Parameters</span></span>

<span data-ttu-id="2033b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2033b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2033b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2033b-108">Return value</span></span>

<span data-ttu-id="2033b-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2033b-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2033b-110">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2033b-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2033b-111">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2033b-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2033b-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2033b-112">Remarks</span></span>

<span data-ttu-id="2033b-113">La matriz de identidad es una matriz en la que todos los coeficientes son 0,0 excepto \[ los coeficientes 1,1 \] \[ 2,2 \] \[ 3,3 4,4, que se establecen en \] \[ \] 1,0.</span><span class="sxs-lookup"><span data-stu-id="2033b-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="2033b-114">La matriz de identidad es especial en que, cuando se aplica a los vértices, no se modifican.</span><span class="sxs-lookup"><span data-stu-id="2033b-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="2033b-115">La matriz de identidad se usa como punto de partida para las matrices que modificarán los valores de vértice para crear rotaciones, traducciones y cualquier otra transformación que se pueda representar mediante una matriz de 4x4.</span><span class="sxs-lookup"><span data-stu-id="2033b-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="2033b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2033b-116">Requirements</span></span>



| <span data-ttu-id="2033b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2033b-117">Requirement</span></span> | <span data-ttu-id="2033b-118">Value</span><span class="sxs-lookup"><span data-stu-id="2033b-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2033b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2033b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2033b-120"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="2033b-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2033b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2033b-121">Library</span></span><br/> | <dl> <span data-ttu-id="2033b-122"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2033b-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2033b-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2033b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2033b-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="2033b-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2033b-125">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="2033b-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




