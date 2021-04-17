---
description: Carga la identidad en la matriz actual.
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: 'ID3DXMATRIXStack:: LoadIdentity (método) (D3dx9math. h)'
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
ms.openlocfilehash: e7ebc7b61679dc3938c2a57aa2346a45b136e5a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717650"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a><span data-ttu-id="fc4ed-103">ID3DXMATRIXStack:: LoadIdentity (método) (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fc4ed-103">ID3DXMATRIXStack::LoadIdentity method (D3dx9math.h)</span></span>

<span data-ttu-id="fc4ed-104">Carga la identidad en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="fc4ed-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc4ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc4ed-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="fc4ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc4ed-106">Parameters</span></span>

<span data-ttu-id="fc4ed-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fc4ed-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc4ed-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc4ed-108">Return value</span></span>

<span data-ttu-id="fc4ed-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc4ed-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc4ed-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc4ed-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fc4ed-111">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fc4ed-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc4ed-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc4ed-112">Remarks</span></span>

<span data-ttu-id="fc4ed-113">La matriz de identidad es una matriz en la que todos los coeficientes son 0,0 excepto los \[ \] \[ coeficientes 1, 1 2, 2 \] \[ 3, 3 \] \[ 4, 4 \] , que se establecen en 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc4ed-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="fc4ed-114">La matriz de identidad es especial, ya que, cuando se aplica a los vértices, no cambian.</span><span class="sxs-lookup"><span data-stu-id="fc4ed-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="fc4ed-115">La matriz de identidad se usa como punto de partida para las matrices que modificarán los valores de los vértices para crear giros, traducciones y otras transformaciones que se pueden representar mediante una matriz de 4x4.</span><span class="sxs-lookup"><span data-stu-id="fc4ed-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc4ed-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc4ed-116">Requirements</span></span>



| <span data-ttu-id="fc4ed-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc4ed-117">Requirement</span></span> | <span data-ttu-id="fc4ed-118">Value</span><span class="sxs-lookup"><span data-stu-id="fc4ed-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4ed-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc4ed-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fc4ed-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc4ed-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fc4ed-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc4ed-121">Library</span></span><br/> | <dl> <span data-ttu-id="fc4ed-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc4ed-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc4ed-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc4ed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc4ed-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="fc4ed-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="fc4ed-125">**ID3DXMATRIXStack::LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="fc4ed-125">**ID3DXMATRIXStack::LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




