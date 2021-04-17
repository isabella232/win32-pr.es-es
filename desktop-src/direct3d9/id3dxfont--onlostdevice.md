---
description: Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: 'ID3DXFont:: OnLostDevice (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae2dc711ffe57a2605a0cc43c7ba673d444105f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689890"
---
# <a name="id3dxfontonlostdevice-method"></a><span data-ttu-id="90930-104">ID3DXFont:: OnLostDevice (método)</span><span class="sxs-lookup"><span data-stu-id="90930-104">ID3DXFont::OnLostDevice method</span></span>

<span data-ttu-id="90930-105">Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks.</span><span class="sxs-lookup"><span data-stu-id="90930-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="90930-106">Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90930-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="90930-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90930-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="90930-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90930-108">Parameters</span></span>

<span data-ttu-id="90930-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="90930-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="90930-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90930-110">Return value</span></span>

<span data-ttu-id="90930-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90930-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90930-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="90930-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="90930-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="90930-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="90930-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90930-114">Remarks</span></span>

<span data-ttu-id="90930-115">Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**RESET**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="90930-115">This method should be called whenever the device is lost or before the user calls [**Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="90930-116">Incluso si el dispositivo no se perdió realmente, **OnLostDevice** es responsable de liberar stateblocks y otros recursos que puedan ser necesarios para su lanzamiento antes de restablecer el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90930-116">Even if the device was not actually lost, **OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="90930-117">Como resultado, no se puede volver a usar el objeto de fuente antes de llamar a **RESET** y, a continuación, [**OnResetDevice**](id3dxfont--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="90930-117">As a result, the font object cannot be used again before calling **Reset** and then [**OnResetDevice**](id3dxfont--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90930-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90930-118">Requirements</span></span>



| <span data-ttu-id="90930-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="90930-119">Requirement</span></span> | <span data-ttu-id="90930-120">Value</span><span class="sxs-lookup"><span data-stu-id="90930-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90930-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90930-121">Header</span></span><br/>  | <dl> <span data-ttu-id="90930-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="90930-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="90930-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90930-123">Library</span></span><br/> | <dl> <span data-ttu-id="90930-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90930-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="90930-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="90930-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90930-126">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="90930-126">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




