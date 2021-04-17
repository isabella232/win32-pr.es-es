---
description: Prepara un dispositivo para dibujar líneas.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'ID3DXLine:: Begin (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698379"
---
# <a name="id3dxlinebegin-method"></a><span data-ttu-id="cd9d9-103">ID3DXLine:: Begin (método)</span><span class="sxs-lookup"><span data-stu-id="cd9d9-103">ID3DXLine::Begin method</span></span>

<span data-ttu-id="cd9d9-104">Prepara un dispositivo para dibujar líneas.</span><span class="sxs-lookup"><span data-stu-id="cd9d9-104">Prepares a device for drawing lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd9d9-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="cd9d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd9d9-106">Parameters</span></span>

<span data-ttu-id="cd9d9-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cd9d9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd9d9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd9d9-108">Return value</span></span>

<span data-ttu-id="cd9d9-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd9d9-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd9d9-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd9d9-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cd9d9-111">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="cd9d9-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd9d9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd9d9-112">Remarks</span></span>

<span data-ttu-id="cd9d9-113">La llamada a **ID3DXLine:: Begin** es opcional.</span><span class="sxs-lookup"><span data-stu-id="cd9d9-113">Calling **ID3DXLine::Begin** is optional.</span></span> <span data-ttu-id="cd9d9-114">Si se llama fuera de una secuencia ID3DXLine:: Begin/ID3DXLine:: end, las funciones Draw llamarán internamente a ID3DXLine:: Begin y ID3DXLine:: end.</span><span class="sxs-lookup"><span data-stu-id="cd9d9-114">If called outside of a ID3DXLine::Begin/ID3DXLine::End sequence, the draw functions will internally call ID3DXLine::Begin and ID3DXLine::End.</span></span> <span data-ttu-id="cd9d9-115">Para evitar una sobrecarga adicional, este método se debe usar si se llama a más de una función Draw sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="cd9d9-115">To avoid extra overhead, this method should be used if more than one draw function will be called successively.</span></span>

<span data-ttu-id="cd9d9-116">Se debe llamar a este método desde una secuencia [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) y [**IDirect3DDevice9:: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="cd9d9-116">This method must be called from inside an [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) and [**IDirect3DDevice9::EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) sequence.</span></span>

<span data-ttu-id="cd9d9-117">ID3DXLine:: Begin no se puede usar como sustituto de [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="cd9d9-117">ID3DXLine::Begin cannot be used as a substitute for either [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9d9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd9d9-118">Requirements</span></span>



| <span data-ttu-id="cd9d9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd9d9-119">Requirement</span></span> | <span data-ttu-id="cd9d9-120">Value</span><span class="sxs-lookup"><span data-stu-id="cd9d9-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9d9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd9d9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cd9d9-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9d9-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="cd9d9-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd9d9-123">Library</span></span><br/> | <dl> <span data-ttu-id="cd9d9-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd9d9-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd9d9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd9d9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9d9-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="cd9d9-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
