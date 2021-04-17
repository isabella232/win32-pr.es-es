---
description: Obtiene el índice de una animación, dado su nombre.
ms.assetid: 6e91a4fe-3202-447b-b486-d29e8da64af2
title: 'ID3DXAnimationSet:: GetAnimationIndexByName (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationIndexByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4d3e5fb39ebcfa5ce906d1f90c2c5c10bdd4b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707781"
---
# <a name="id3dxanimationsetgetanimationindexbyname-method"></a><span data-ttu-id="1639f-103">ID3DXAnimationSet:: GetAnimationIndexByName (método)</span><span class="sxs-lookup"><span data-stu-id="1639f-103">ID3DXAnimationSet::GetAnimationIndexByName method</span></span>

<span data-ttu-id="1639f-104">Obtiene el índice de una animación, dado su nombre.</span><span class="sxs-lookup"><span data-stu-id="1639f-104">Gets the index of an animation, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1639f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1639f-105">Syntax</span></span>


```C++
HRESULT GetAnimationIndexByName(
  [in]  LPCSTR pName,
  [out] UINT   *pIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1639f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1639f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1639f-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1639f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1639f-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1639f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1639f-109">Nombre de la animación.</span><span class="sxs-lookup"><span data-stu-id="1639f-109">Name of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="1639f-110">*pIndex* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1639f-110">*pIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1639f-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1639f-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1639f-112">Puntero al índice de animación.</span><span class="sxs-lookup"><span data-stu-id="1639f-112">Pointer to the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1639f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1639f-113">Return value</span></span>

<span data-ttu-id="1639f-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1639f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1639f-115">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="1639f-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="1639f-116">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1639f-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="1639f-117">En caso contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="1639f-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1639f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1639f-118">Requirements</span></span>



| <span data-ttu-id="1639f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1639f-119">Requirement</span></span> | <span data-ttu-id="1639f-120">Value</span><span class="sxs-lookup"><span data-stu-id="1639f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1639f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1639f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1639f-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1639f-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1639f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1639f-123">Library</span></span><br/> | <dl> <span data-ttu-id="1639f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1639f-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1639f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1639f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1639f-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="1639f-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
