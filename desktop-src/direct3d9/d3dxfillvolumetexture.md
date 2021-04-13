---
description: Utiliza una función proporcionada por el usuario para rellenar cada textura de cada nivel de MIP de una textura de volumen determinada.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: Función D3DXFillVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362571"
---
# <a name="d3dxfillvolumetexture-function"></a><span data-ttu-id="0ef63-103">D3DXFillVolumeTexture función)</span><span class="sxs-lookup"><span data-stu-id="0ef63-103">D3DXFillVolumeTexture function</span></span>

<span data-ttu-id="0ef63-104">Utiliza una función proporcionada por el usuario para rellenar cada textura de cada nivel de MIP de una textura de volumen determinada.</span><span class="sxs-lookup"><span data-stu-id="0ef63-104">Uses a user-provided function to fill each texel of each mip level of a given volume texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef63-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ef63-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a><span data-ttu-id="0ef63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ef63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef63-107">*pTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0ef63-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef63-108">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="0ef63-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="0ef63-109">Puntero a una interfaz [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa la textura rellenada.</span><span class="sxs-lookup"><span data-stu-id="0ef63-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="0ef63-110">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ef63-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef63-111">Tipo: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef63-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="0ef63-112">Puntero a una función evaluadora proporcionada por el usuario, que se utilizará para calcular el valor de cada textura.</span><span class="sxs-lookup"><span data-stu-id="0ef63-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="0ef63-113">La función sigue el prototipo de [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="0ef63-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ef63-114">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ef63-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef63-115">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef63-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ef63-116">Puntero a un bloque arbitrario de datos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0ef63-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="0ef63-117">Este puntero se pasará a la función proporcionada en *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="0ef63-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef63-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ef63-118">Return value</span></span>

<span data-ttu-id="0ef63-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ef63-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ef63-120">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ef63-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ef63-121">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0ef63-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef63-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ef63-122">Remarks</span></span>

<span data-ttu-id="0ef63-123">Si el volumen no es dinámico (porque el uso se establece en 0 cuando se crea) y se encuentra en la memoria de vídeo (el grupo de memoria se establece en el \_ valor predeterminado de D3DPOOL), **D3DXFillVolumeTexture** producirá un error porque el volumen no se puede bloquear.</span><span class="sxs-lookup"><span data-stu-id="0ef63-123">If the volume is non-dynamic (because usage is set to 0 when it is created), and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXFillVolumeTexture** will fail because the volume cannot be locked.</span></span>

<span data-ttu-id="0ef63-124">En este ejemplo se crea una función denominada ColorVolumeFill, que se basa en D3DXFillVolumeTexture.</span><span class="sxs-lookup"><span data-stu-id="0ef63-124">This example creates a function called ColorVolumeFill, which relies on D3DXFillVolumeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0ef63-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ef63-125">Requirements</span></span>



| <span data-ttu-id="0ef63-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ef63-126">Requirement</span></span> | <span data-ttu-id="0ef63-127">Value</span><span class="sxs-lookup"><span data-stu-id="0ef63-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef63-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ef63-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef63-129"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef63-129"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0ef63-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ef63-130">Library</span></span><br/> | <dl> <span data-ttu-id="0ef63-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ef63-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0ef63-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ef63-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef63-133">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0ef63-133">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
