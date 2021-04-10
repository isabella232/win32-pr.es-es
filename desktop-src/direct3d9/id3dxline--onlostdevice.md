---
description: Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.
ms.assetid: a5c82a58-10f9-44bd-a42f-555867b2c857
title: 'ID3DXLine:: OnLostDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40b42f5a4d027d00b458b572a28ea0c6987cf971
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003954"
---
# <a name="id3dxlineonlostdevice-method"></a><span data-ttu-id="3834f-104">ID3DXLine:: OnLostDevice (método)</span><span class="sxs-lookup"><span data-stu-id="3834f-104">ID3DXLine::OnLostDevice method</span></span>

<span data-ttu-id="3834f-105">Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks.</span><span class="sxs-lookup"><span data-stu-id="3834f-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="3834f-106">Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3834f-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3834f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3834f-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="3834f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3834f-108">Parameters</span></span>

<span data-ttu-id="3834f-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3834f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3834f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3834f-110">Return value</span></span>

<span data-ttu-id="3834f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3834f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3834f-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3834f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3834f-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3834f-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3834f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3834f-114">Remarks</span></span>

<span data-ttu-id="3834f-115">Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9:: RESET**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="3834f-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="3834f-116">Incluso si el dispositivo no se perdió realmente, **ID3DXLine:: OnLostDevice** es responsable de liberar stateblocks y otros recursos que pueden ser necesarios para su lanzamiento antes de restablecer el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3834f-116">Even if the device was not actually lost, **ID3DXLine::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="3834f-117">Como resultado, el objeto Font no se puede volver a usar antes de llamar a **IDirect3DDevice9:: RESET** y después a [**ID3DXLine:: OnResetDevice**](id3dxline--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3834f-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXLine::OnResetDevice**](id3dxline--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3834f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3834f-118">Requirements</span></span>



| <span data-ttu-id="3834f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3834f-119">Requirement</span></span> | <span data-ttu-id="3834f-120">Value</span><span class="sxs-lookup"><span data-stu-id="3834f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3834f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3834f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3834f-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3834f-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3834f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3834f-123">Library</span></span><br/> | <dl> <span data-ttu-id="3834f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3834f-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3834f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3834f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3834f-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="3834f-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 




