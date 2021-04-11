---
description: Determina si una matriz es una matriz de identidad.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: Función D3DXMatrixIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c2ca91f74512b432d7cc18b28cef44d713cfc11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362686"
---
# <a name="d3dxmatrixisidentity-function"></a><span data-ttu-id="6a30b-103">D3DXMatrixIsIdentity función)</span><span class="sxs-lookup"><span data-stu-id="6a30b-103">D3DXMatrixIsIdentity function</span></span>

<span data-ttu-id="6a30b-104">Determina si una matriz es una matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="6a30b-104">Determines if a matrix is an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a30b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a30b-105">Syntax</span></span>


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="6a30b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a30b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a30b-107">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a30b-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a30b-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a30b-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6a30b-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) cuya identidad se probará.</span><span class="sxs-lookup"><span data-stu-id="6a30b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a30b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a30b-110">Return value</span></span>

<span data-ttu-id="6a30b-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a30b-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a30b-112">Si la matriz es una matriz de identidad, esta función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="6a30b-112">If the matrix is an identity matrix, this function returns **TRUE**.</span></span> <span data-ttu-id="6a30b-113">De lo contrario, esta función devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="6a30b-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a30b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a30b-114">Requirements</span></span>



| <span data-ttu-id="6a30b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a30b-115">Requirement</span></span> | <span data-ttu-id="6a30b-116">Value</span><span class="sxs-lookup"><span data-stu-id="6a30b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a30b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a30b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6a30b-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a30b-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6a30b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a30b-119">Library</span></span><br/> | <dl> <span data-ttu-id="6a30b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a30b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a30b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a30b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a30b-122">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="6a30b-122">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6a30b-123">**D3DXMatrixIdentity**</span><span class="sxs-lookup"><span data-stu-id="6a30b-123">**D3DXMatrixIdentity**</span></span>](d3dxmatrixidentity.md)
</dt> </dl>

 

 
