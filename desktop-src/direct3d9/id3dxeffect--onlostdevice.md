---
description: Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: 'ID3DXEffect:: OnLostDevice (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af2d17c99f0b694a8b27924c34faa2a1f633fafb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707797"
---
# <a name="id3dxeffectonlostdevice-method"></a><span data-ttu-id="3ba18-104">ID3DXEffect:: OnLostDevice (método)</span><span class="sxs-lookup"><span data-stu-id="3ba18-104">ID3DXEffect::OnLostDevice method</span></span>

<span data-ttu-id="3ba18-105">Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks.</span><span class="sxs-lookup"><span data-stu-id="3ba18-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="3ba18-106">Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ba18-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba18-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ba18-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="3ba18-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ba18-108">Parameters</span></span>

<span data-ttu-id="3ba18-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3ba18-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ba18-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ba18-110">Return value</span></span>

<span data-ttu-id="3ba18-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ba18-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ba18-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3ba18-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3ba18-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3ba18-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba18-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ba18-114">Remarks</span></span>

<span data-ttu-id="3ba18-115">Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9:: RESET**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="3ba18-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="3ba18-116">Incluso si el dispositivo no se perdió realmente, **ID3DXEffect:: OnLostDevice** es responsable de liberar stateblocks y otros recursos que pueden ser necesarios para su lanzamiento antes de restablecer el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ba18-116">Even if the device was not actually lost, **ID3DXEffect::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="3ba18-117">Como resultado, el objeto Font no se puede volver a usar antes de llamar a **IDirect3DDevice9:: RESET** y después a [**ID3DXEffect:: OnResetDevice**](id3dxeffect--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3ba18-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba18-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ba18-118">Requirements</span></span>



| <span data-ttu-id="3ba18-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba18-119">Requirement</span></span> | <span data-ttu-id="3ba18-120">Value</span><span class="sxs-lookup"><span data-stu-id="3ba18-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba18-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ba18-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3ba18-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba18-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3ba18-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ba18-123">Library</span></span><br/> | <dl> <span data-ttu-id="3ba18-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ba18-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3ba18-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ba18-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba18-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="3ba18-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




