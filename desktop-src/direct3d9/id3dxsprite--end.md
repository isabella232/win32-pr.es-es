---
description: 'Llama a ID3DXSprite:: Flush y restaura el estado del dispositivo al modo en que se encontraba antes de que se llamara a ID3DXSprite:: Begin.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'ID3DXSprite:: end (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424452"
---
# <a name="id3dxspriteend-method"></a><span data-ttu-id="bd65a-103">ID3DXSprite:: end (método)</span><span class="sxs-lookup"><span data-stu-id="bd65a-103">ID3DXSprite::End method</span></span>

<span data-ttu-id="bd65a-104">Llama a [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) y restaura el estado del dispositivo al modo en que se encontraba antes de que se llamara a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="bd65a-104">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd65a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd65a-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="bd65a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd65a-106">Parameters</span></span>

<span data-ttu-id="bd65a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bd65a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd65a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd65a-108">Return value</span></span>

<span data-ttu-id="bd65a-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd65a-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd65a-110">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bd65a-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bd65a-111">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="bd65a-111">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="bd65a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd65a-112">Remarks</span></span>

<span data-ttu-id="bd65a-113">**ID3DXSprite:: end** no se puede usar como sustituto de [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="bd65a-113">**ID3DXSprite::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd65a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd65a-114">Requirements</span></span>



| <span data-ttu-id="bd65a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd65a-115">Requirement</span></span> | <span data-ttu-id="bd65a-116">Value</span><span class="sxs-lookup"><span data-stu-id="bd65a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd65a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd65a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bd65a-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd65a-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="bd65a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd65a-119">Library</span></span><br/> | <dl> <span data-ttu-id="bd65a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd65a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd65a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd65a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd65a-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="bd65a-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="bd65a-123">**ID3DXSprite:: Begin**</span><span class="sxs-lookup"><span data-stu-id="bd65a-123">**ID3DXSprite::Begin**</span></span>](id3dxsprite--begin.md)
</dt> </dl>

 

 




