---
description: 'Método ID3DXRenderToSurface::OnLostDevice: use este método para liberar todas las referencias a recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.'
ms.assetid: 8962236d-4801-46a3-9944-a7c4ad762882
title: Método ID3DXRenderToSurface::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 772b678dc4260954c2e03c13d7259565cd896bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093123"
---
# <a name="id3dxrendertosurfaceonlostdevice-method"></a><span data-ttu-id="b7cef-104">Método ID3DXRenderToSurface::OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="b7cef-104">ID3DXRenderToSurface::OnLostDevice method</span></span>

<span data-ttu-id="b7cef-105">Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado.</span><span class="sxs-lookup"><span data-stu-id="b7cef-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="b7cef-106">Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7cef-106">This method should be called whenever a device is lost or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7cef-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7cef-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="b7cef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7cef-108">Parameters</span></span>

<span data-ttu-id="b7cef-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b7cef-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7cef-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7cef-110">Return value</span></span>

<span data-ttu-id="b7cef-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7cef-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7cef-112">Si el método se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b7cef-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b7cef-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b7cef-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7cef-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7cef-114">Remarks</span></span>

<span data-ttu-id="b7cef-115">Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset).</span><span class="sxs-lookup"><span data-stu-id="b7cef-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset).</span></span> <span data-ttu-id="b7cef-116">Incluso si el dispositivo no se perdió realmente, ID3DXRenderToSurface::OnLostDevice es responsable de liberar los bloques de estado y otros recursos que es posible que deba liberar antes de restablecer el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7cef-116">Even if the device was not actually lost, ID3DXRenderToSurface::OnLostDevice is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="b7cef-117">Como resultado, el objeto de fuente no se puede usar de nuevo antes de llamar a **IDirect3DDevice9::Reset** y, a continuación, ID3DXRenderToSurface::OnResetDevice.</span><span class="sxs-lookup"><span data-stu-id="b7cef-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then ID3DXRenderToSurface::OnResetDevice.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7cef-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7cef-118">Requirements</span></span>



| <span data-ttu-id="b7cef-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7cef-119">Requirement</span></span> | <span data-ttu-id="b7cef-120">Value</span><span class="sxs-lookup"><span data-stu-id="b7cef-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7cef-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b7cef-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="b7cef-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b7cef-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7cef-123">Library</span></span><br/> | <dl> <span data-ttu-id="b7cef-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7cef-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7cef-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b7cef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7cef-126">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="b7cef-126">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
