---
description: Recupera el dispositivo asociado al objeto Sprite.
ms.assetid: 9ce18623-893e-4395-bdf7-8d16a641a557
title: 'ID3DXSprite:: GetDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf98eb932971a22232a5dbc8f0d5449f8639db97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424460"
---
# <a name="id3dxspritegetdevice-method"></a><span data-ttu-id="4d4f4-103">ID3DXSprite:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="4d4f4-103">ID3DXSprite::GetDevice method</span></span>

<span data-ttu-id="4d4f4-104">Recupera el dispositivo asociado al objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-104">Retrieves the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d4f4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d4f4-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="4d4f4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d4f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d4f4-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4d4f4-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4d4f4-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="4d4f4-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="4d4f4-109">Dirección de un puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo Direct3D asociado al objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d4f4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d4f4-110">Return value</span></span>

<span data-ttu-id="4d4f4-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4d4f4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4d4f4-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4d4f4-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4d4f4-113">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="4d4f4-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="4d4f4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d4f4-114">Remarks</span></span>

<span data-ttu-id="4d4f4-115">Al llamar a este método, se aumentará el recuento de referencias interno en la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="4d4f4-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d4f4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d4f4-116">Requirements</span></span>



| <span data-ttu-id="4d4f4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d4f4-117">Requirement</span></span> | <span data-ttu-id="4d4f4-118">Value</span><span class="sxs-lookup"><span data-stu-id="4d4f4-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4f4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d4f4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4d4f4-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d4f4-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="4d4f4-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d4f4-121">Library</span></span><br/> | <dl> <span data-ttu-id="4d4f4-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d4f4-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d4f4-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d4f4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d4f4-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="4d4f4-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 
