---
description: Utiliza una función proporcionada por el usuario para rellenar cada textura de cada nivel de MIP de una textura de cubo determinada.
ms.assetid: 0390a1b6-6675-42e1-bc45-65dd7b2d83c5
title: Función D3DXFillCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9fda70aa42d6982c40eb1ec926b6823e7ac7d997
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698248"
---
# <a name="d3dxfillcubetexture-function"></a><span data-ttu-id="b8fde-103">D3DXFillCubeTexture función)</span><span class="sxs-lookup"><span data-stu-id="b8fde-103">D3DXFillCubeTexture function</span></span>

<span data-ttu-id="b8fde-104">Utiliza una función proporcionada por el usuario para rellenar cada textura de cada nivel de MIP de una textura de cubo determinada.</span><span class="sxs-lookup"><span data-stu-id="b8fde-104">Uses a user-provided function to fill each texel of each mip level of a given cube texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8fde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8fde-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTexture(
  _Out_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D           pFunction,
  _In_  LPVOID                 pData
);
```



## <a name="parameters"></a><span data-ttu-id="b8fde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8fde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8fde-107">*pTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b8fde-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8fde-108">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="b8fde-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="b8fde-109">Puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa la textura rellenada.</span><span class="sxs-lookup"><span data-stu-id="b8fde-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="b8fde-110">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8fde-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8fde-111">Tipo: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="b8fde-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="b8fde-112">Puntero a una función evaluadora proporcionada por el usuario, que se utilizará para calcular el valor de cada textura.</span><span class="sxs-lookup"><span data-stu-id="b8fde-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="b8fde-113">La función sigue el prototipo de [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="b8fde-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8fde-114">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8fde-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8fde-115">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8fde-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8fde-116">Puntero a un bloque arbitrario de datos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b8fde-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="b8fde-117">Este puntero se pasará a la función proporcionada en *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="b8fde-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8fde-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8fde-118">Return value</span></span>

<span data-ttu-id="b8fde-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8fde-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8fde-120">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8fde-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b8fde-121">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b8fde-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8fde-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8fde-122">Remarks</span></span>

<span data-ttu-id="b8fde-123">Este es un ejemplo en el que se crea una función denominada ColorCubeFill, que se basa en D3DXFillCubeTexture.</span><span class="sxs-lookup"><span data-stu-id="b8fde-123">Here is an example that creates a function called ColorCubeFill, which relies on D3DXFillCubeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorCubeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill the texture using D3DXFillCubeTexture
if (FAILED (hr = D3DXFillCubeTexture (m_pTexture, ColorCubeFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="b8fde-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8fde-124">Requirements</span></span>



| <span data-ttu-id="b8fde-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8fde-125">Requirement</span></span> | <span data-ttu-id="b8fde-126">Value</span><span class="sxs-lookup"><span data-stu-id="b8fde-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8fde-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8fde-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b8fde-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8fde-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b8fde-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8fde-129">Library</span></span><br/> | <dl> <span data-ttu-id="b8fde-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8fde-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b8fde-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8fde-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8fde-132">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b8fde-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
