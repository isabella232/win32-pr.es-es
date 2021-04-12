---
description: Recupera el dispositivo Direct3D asociado a la superficie de representación.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: 'ID3DXRenderToSurface:: GetDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac01744887412349c71daa34194fc3a0b03b19a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362766"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a><span data-ttu-id="5b34b-103">ID3DXRenderToSurface:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="5b34b-103">ID3DXRenderToSurface::GetDevice method</span></span>

<span data-ttu-id="5b34b-104">Recupera el dispositivo Direct3D asociado a la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="5b34b-104">Retrieves the Direct3D device associated with the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b34b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b34b-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="5b34b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b34b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b34b-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5b34b-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5b34b-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="5b34b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="5b34b-109">Dirección de un puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo de Direct3D asociado a la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="5b34b-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b34b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b34b-110">Return value</span></span>

<span data-ttu-id="5b34b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b34b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b34b-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b34b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5b34b-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5b34b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="5b34b-114">Al llamar a este método, se aumentará el recuento de referencias interno en la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="5b34b-114">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="5b34b-115">Asegúrese de llamar a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) cuando haya terminado de usar esta interfaz **IDirect3DDevice9** o se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="5b34b-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b34b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b34b-116">Requirements</span></span>



| <span data-ttu-id="5b34b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b34b-117">Requirement</span></span> | <span data-ttu-id="5b34b-118">Value</span><span class="sxs-lookup"><span data-stu-id="5b34b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b34b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b34b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5b34b-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b34b-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5b34b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b34b-121">Library</span></span><br/> | <dl> <span data-ttu-id="5b34b-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b34b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5b34b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b34b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b34b-124">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="5b34b-124">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
