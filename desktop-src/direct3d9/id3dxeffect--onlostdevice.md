---
description: 'Método ID3DXEffect::OnLostDevice: use este método para liberar todas las referencias a recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.'
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: Método ID3DXEffect::OnLostDevice (D3DX9Effect.h)
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
ms.openlocfilehash: 1aacdbae268b58a966256a99081b9943d0bfcc92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114973"
---
# <a name="id3dxeffectonlostdevice-method"></a><span data-ttu-id="538fd-104">Método ID3DXEffect::OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="538fd-104">ID3DXEffect::OnLostDevice method</span></span>

<span data-ttu-id="538fd-105">Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado.</span><span class="sxs-lookup"><span data-stu-id="538fd-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="538fd-106">Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="538fd-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="538fd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="538fd-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="538fd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="538fd-108">Parameters</span></span>

<span data-ttu-id="538fd-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="538fd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="538fd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="538fd-110">Return value</span></span>

<span data-ttu-id="538fd-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="538fd-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="538fd-112">Si el método se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="538fd-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="538fd-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="538fd-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="538fd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="538fd-114">Remarks</span></span>

<span data-ttu-id="538fd-115">Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="538fd-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="538fd-116">Incluso si el dispositivo no se perdió realmente, **ID3DXEffect::OnLostDevice** es responsable de liberar los bloques de estado y otros recursos que es posible que deba liberar antes de restablecer el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="538fd-116">Even if the device was not actually lost, **ID3DXEffect::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="538fd-117">Como resultado, el objeto de fuente no se puede volver a usar antes de llamar a **IDirect3DDevice9::Reset** y, a continuación, [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="538fd-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="538fd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="538fd-118">Requirements</span></span>



| <span data-ttu-id="538fd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="538fd-119">Requirement</span></span> | <span data-ttu-id="538fd-120">Value</span><span class="sxs-lookup"><span data-stu-id="538fd-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="538fd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="538fd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="538fd-122"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="538fd-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="538fd-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="538fd-123">Library</span></span><br/> | <dl> <span data-ttu-id="538fd-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="538fd-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="538fd-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="538fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="538fd-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="538fd-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




