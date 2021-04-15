---
description: Obtiene el nombre de una animación, según su índice.
ms.assetid: vs|directx_sdk|~\id3dxanimationset__getanimationnamebyindex.htm
title: 'ID3DXAnimationSet:: GetAnimationNameByIndex (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationNameByIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 820b21fa69fd7007bdd1971e83ea44368dce5cc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707959"
---
# <a name="id3dxanimationsetgetanimationnamebyindex-method"></a><span data-ttu-id="0c75b-103">ID3DXAnimationSet:: GetAnimationNameByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="0c75b-103">ID3DXAnimationSet::GetAnimationNameByIndex method</span></span>

<span data-ttu-id="0c75b-104">Obtiene el nombre de una animación, según su índice.</span><span class="sxs-lookup"><span data-stu-id="0c75b-104">Gets the name of an animation, given its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c75b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c75b-105">Syntax</span></span>


```C++
HRESULT GetAnimationNameByIndex(
  [in]  UINT   Index,
  [out] LPCSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="0c75b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c75b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c75b-107">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0c75b-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c75b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c75b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c75b-109">Índice de la animación.</span><span class="sxs-lookup"><span data-stu-id="0c75b-109">Index of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="0c75b-110">*ppName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0c75b-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c75b-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c75b-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0c75b-112">Dirección de un puntero a una cadena que recibe el nombre de la animación.</span><span class="sxs-lookup"><span data-stu-id="0c75b-112">Address of a pointer to a string that receives the animation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c75b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c75b-113">Return value</span></span>

<span data-ttu-id="0c75b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c75b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c75b-115">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="0c75b-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="0c75b-116">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0c75b-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="0c75b-117">En caso contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="0c75b-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c75b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c75b-118">Requirements</span></span>



| <span data-ttu-id="0c75b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c75b-119">Requirement</span></span> | <span data-ttu-id="0c75b-120">Value</span><span class="sxs-lookup"><span data-stu-id="0c75b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c75b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c75b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0c75b-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c75b-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0c75b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c75b-123">Library</span></span><br/> | <dl> <span data-ttu-id="0c75b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c75b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c75b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c75b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c75b-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="0c75b-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
