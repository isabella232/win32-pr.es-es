---
description: Crea un objeto Sprite que está asociado a un dispositivo determinado. Los objetos Sprite se usan para dibujar imágenes 2D en la pantalla.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: Función D3DXCreateSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718215"
---
# <a name="d3dxcreatesprite-function"></a><span data-ttu-id="c4ba0-104">D3DXCreateSprite función)</span><span class="sxs-lookup"><span data-stu-id="c4ba0-104">D3DXCreateSprite function</span></span>

<span data-ttu-id="c4ba0-105">Crea un objeto Sprite que está asociado a un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-105">Creates a sprite object which is associated with a particular device.</span></span> <span data-ttu-id="c4ba0-106">Los objetos Sprite se usan para dibujar imágenes 2D en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-106">Sprite objects are used to draw 2D images to the screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ba0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4ba0-107">Syntax</span></span>


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="c4ba0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4ba0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ba0-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4ba0-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ba0-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c4ba0-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c4ba0-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el dispositivo que se va a asociar al Sprite.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="c4ba0-112">*ppSprite* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c4ba0-112">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ba0-113">Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4ba0-113">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)\***</span></span>

<span data-ttu-id="c4ba0-114">Dirección de un puntero a una interfaz [**ID3DXSprite**](id3dxsprite.md) .</span><span class="sxs-lookup"><span data-stu-id="c4ba0-114">Address of a pointer to an [**ID3DXSprite**](id3dxsprite.md) interface.</span></span> <span data-ttu-id="c4ba0-115">Esta interfaz permite al usuario tener acceso a las funciones de Sprite.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-115">This interface allows the user to access sprite functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ba0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4ba0-116">Return value</span></span>

<span data-ttu-id="c4ba0-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4ba0-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4ba0-118">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-118">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c4ba0-119">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4ba0-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4ba0-120">Remarks</span></span>

<span data-ttu-id="c4ba0-121">Esta interfaz se puede usar para dibujar dos imágenes dimensionales en el espacio de pantalla del dispositivo asociado.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-121">This interface can be used to draw two dimensional images in screen space of the associated device.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ba0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4ba0-122">Requirements</span></span>



| <span data-ttu-id="c4ba0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4ba0-123">Requirement</span></span> | <span data-ttu-id="c4ba0-124">Value</span><span class="sxs-lookup"><span data-stu-id="c4ba0-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ba0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4ba0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c4ba0-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ba0-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c4ba0-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4ba0-127">Library</span></span><br/> | <dl> <span data-ttu-id="c4ba0-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4ba0-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4ba0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4ba0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ba0-130">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="c4ba0-130">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
