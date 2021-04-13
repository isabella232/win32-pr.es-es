---
description: Use este método para volver a adquirir recursos y guardar el estado inicial.
ms.assetid: 3e231ad6-858e-4b6a-bbea-0839794bbac7
title: 'ID3DXRenderToEnvMap:: OnResetDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d429c08d8bad23652a080998b6a4735132522ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362503"
---
# <a name="id3dxrendertoenvmaponresetdevice-method"></a><span data-ttu-id="75e24-103">ID3DXRenderToEnvMap:: OnResetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="75e24-103">ID3DXRenderToEnvMap::OnResetDevice method</span></span>

<span data-ttu-id="75e24-104">Use este método para volver a adquirir recursos y guardar el estado inicial.</span><span class="sxs-lookup"><span data-stu-id="75e24-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75e24-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="75e24-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75e24-106">Parameters</span></span>

<span data-ttu-id="75e24-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="75e24-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75e24-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75e24-108">Return value</span></span>

<span data-ttu-id="75e24-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75e24-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75e24-110">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75e24-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="75e24-111">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="75e24-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="75e24-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75e24-112">Remarks</span></span>

<span data-ttu-id="75e24-113">Se debe llamar a **ID3DXRenderToEnvMap:: OnResetDevice** cada vez que se restablezca el dispositivo (mediante [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), antes de que se llame a cualquier otro método.</span><span class="sxs-lookup"><span data-stu-id="75e24-113">**ID3DXRenderToEnvMap::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="75e24-114">Este es un buen lugar para volver a adquirir recursos de memoria de vídeo y capturar bloques de estado.</span><span class="sxs-lookup"><span data-stu-id="75e24-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="75e24-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75e24-115">Requirements</span></span>



| <span data-ttu-id="75e24-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="75e24-116">Requirement</span></span> | <span data-ttu-id="75e24-117">Value</span><span class="sxs-lookup"><span data-stu-id="75e24-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75e24-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75e24-118">Header</span></span><br/>  | <dl> <span data-ttu-id="75e24-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="75e24-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="75e24-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75e24-120">Library</span></span><br/> | <dl> <span data-ttu-id="75e24-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75e24-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75e24-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="75e24-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e24-123">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="75e24-123">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
