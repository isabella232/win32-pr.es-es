---
description: Utiliza una función proporcionada por el usuario para rellenar cada textura de cada nivel de MIP de una textura determinada.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: Función D3DXFillTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362572"
---
# <a name="d3dxfilltexture-function"></a><span data-ttu-id="f38c9-103">D3DXFillTexture función)</span><span class="sxs-lookup"><span data-stu-id="f38c9-103">D3DXFillTexture function</span></span>

<span data-ttu-id="f38c9-104">Utiliza una función proporcionada por el usuario para rellenar cada textura de cada nivel de MIP de una textura determinada.</span><span class="sxs-lookup"><span data-stu-id="f38c9-104">Uses a user-provided function to fill each texel of each mip level of a given texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f38c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f38c9-105">Syntax</span></span>


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a><span data-ttu-id="f38c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f38c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f38c9-107">*pTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f38c9-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f38c9-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="f38c9-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="f38c9-109">Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura rellenada.</span><span class="sxs-lookup"><span data-stu-id="f38c9-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="f38c9-110">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f38c9-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f38c9-111">Tipo: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span><span class="sxs-lookup"><span data-stu-id="f38c9-111">Type: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span></span>

<span data-ttu-id="f38c9-112">Puntero a una función evaluadora proporcionada por el usuario, que se utilizará para calcular el valor de cada textura.</span><span class="sxs-lookup"><span data-stu-id="f38c9-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="f38c9-113">La función sigue el prototipo de [LPD3DXFILL2D](lpd3dxfill2d.md).</span><span class="sxs-lookup"><span data-stu-id="f38c9-113">The function follows the prototype of [LPD3DXFILL2D](lpd3dxfill2d.md).</span></span>

</dd> <dt>

<span data-ttu-id="f38c9-114">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f38c9-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f38c9-115">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f38c9-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f38c9-116">Puntero a un bloque arbitrario de datos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f38c9-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="f38c9-117">Este puntero se pasará a la función proporcionada en *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="f38c9-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f38c9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f38c9-118">Return value</span></span>

<span data-ttu-id="f38c9-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f38c9-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f38c9-120">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f38c9-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f38c9-121">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f38c9-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f38c9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f38c9-122">Remarks</span></span>

<span data-ttu-id="f38c9-123">Este es un ejemplo en el que se crea una función denominada ColorFill, que se basa en D3DXFillTexture.</span><span class="sxs-lookup"><span data-stu-id="f38c9-123">Here is an example that creates a function called ColorFill, which relies on D3DXFillTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="f38c9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f38c9-124">Requirements</span></span>



| <span data-ttu-id="f38c9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f38c9-125">Requirement</span></span> | <span data-ttu-id="f38c9-126">Value</span><span class="sxs-lookup"><span data-stu-id="f38c9-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f38c9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f38c9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f38c9-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f38c9-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f38c9-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f38c9-129">Library</span></span><br/> | <dl> <span data-ttu-id="f38c9-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f38c9-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f38c9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f38c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38c9-132">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f38c9-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
