---
description: 'Método ID3DXMATRIXStack::LoadIdentity (D3dx9math.h): carga la identidad en la matriz actual.'
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: Método ID3DXMATRIXStack::LoadIdentity (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663559db0746b9d689066e537c1473f467341cbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093563"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a><span data-ttu-id="ba418-103">Método ID3DXMATRIXStack::LoadIdentity (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="ba418-103">ID3DXMATRIXStack::LoadIdentity method (D3dx9math.h)</span></span>

<span data-ttu-id="ba418-104">Carga la identidad en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="ba418-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba418-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba418-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="ba418-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba418-106">Parameters</span></span>

<span data-ttu-id="ba418-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ba418-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba418-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba418-108">Return value</span></span>

<span data-ttu-id="ba418-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba418-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba418-110">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ba418-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ba418-111">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ba418-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba418-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba418-112">Remarks</span></span>

<span data-ttu-id="ba418-113">La matriz de identidad es una matriz en la que todos los coeficientes son 0,0 excepto \[ los coeficientes 1,1 \] \[ 2,2 \] \[ 3,3 4,4, que se establecen en \] \[ \] 1,0.</span><span class="sxs-lookup"><span data-stu-id="ba418-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="ba418-114">La matriz de identidad es especial en que, cuando se aplica a los vértices, no se modifican.</span><span class="sxs-lookup"><span data-stu-id="ba418-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="ba418-115">La matriz de identidad se usa como punto de partida para las matrices que modificarán los valores de vértice para crear rotaciones, traducciones y cualquier otra transformación que se pueda representar mediante una matriz de 4x4.</span><span class="sxs-lookup"><span data-stu-id="ba418-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba418-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba418-116">Requirements</span></span>



| <span data-ttu-id="ba418-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba418-117">Requirement</span></span> | <span data-ttu-id="ba418-118">Value</span><span class="sxs-lookup"><span data-stu-id="ba418-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba418-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba418-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ba418-120"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ba418-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ba418-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba418-121">Library</span></span><br/> | <dl> <span data-ttu-id="ba418-122"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba418-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ba418-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ba418-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba418-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="ba418-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ba418-125">**ID3DXMATRIXStack::LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="ba418-125">**ID3DXMATRIXStack::LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




