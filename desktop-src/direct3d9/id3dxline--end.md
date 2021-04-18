---
description: 'Restaura el estado del dispositivo al modo en que se encontraba cuando se llamó a ID3DXLine:: Begin.'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'ID3DXLine:: end (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698376"
---
# <a name="id3dxlineend-method"></a><span data-ttu-id="c8ff3-103">ID3DXLine:: end (método)</span><span class="sxs-lookup"><span data-stu-id="c8ff3-103">ID3DXLine::End method</span></span>

<span data-ttu-id="c8ff3-104">Restaura el estado del dispositivo al modo en que se encontraba cuando se llamó a [**ID3DXLine:: Begin**](id3dxline--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="c8ff3-104">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ff3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8ff3-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="c8ff3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8ff3-106">Parameters</span></span>

<span data-ttu-id="c8ff3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8ff3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8ff3-108">Return value</span></span>

<span data-ttu-id="c8ff3-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8ff3-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8ff3-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c8ff3-111">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8ff3-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8ff3-112">Remarks</span></span>

<span data-ttu-id="c8ff3-113">**ID3DXLine:: end** no se puede usar como sustituto de [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="c8ff3-113">**ID3DXLine::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8ff3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8ff3-114">Requirements</span></span>



| <span data-ttu-id="c8ff3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8ff3-115">Requirement</span></span> | <span data-ttu-id="c8ff3-116">Value</span><span class="sxs-lookup"><span data-stu-id="c8ff3-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ff3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8ff3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c8ff3-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8ff3-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c8ff3-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8ff3-119">Library</span></span><br/> | <dl> <span data-ttu-id="c8ff3-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8ff3-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8ff3-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8ff3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ff3-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="c8ff3-122">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="c8ff3-123">**ID3DXLine:: Begin**</span><span class="sxs-lookup"><span data-stu-id="c8ff3-123">**ID3DXLine::Begin**</span></span>](id3dxline--begin.md)
</dt> </dl>

 

 




