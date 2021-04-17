---
description: El \_ método put FullScreenMode establece el modo de pantalla completa del representador.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Método CBaseControlWindow.put_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660626"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a><span data-ttu-id="98f8c-103">CBaseControlWindow. put \_ FullScreenMode (método)</span><span class="sxs-lookup"><span data-stu-id="98f8c-103">CBaseControlWindow.put\_FullScreenMode method</span></span>

<span data-ttu-id="98f8c-104">El `put_FullScreenMode` método establece el modo de pantalla completa del representador.</span><span class="sxs-lookup"><span data-stu-id="98f8c-104">The `put_FullScreenMode` method sets the full-screen mode of the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f8c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98f8c-105">Syntax</span></span>


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="98f8c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98f8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98f8c-107">*FullScreenMode*</span><span class="sxs-lookup"><span data-stu-id="98f8c-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="98f8c-108">Modo de pantalla completa que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="98f8c-108">Full-screen mode to apply.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98f8c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98f8c-109">Return value</span></span>

<span data-ttu-id="98f8c-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98f8c-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="98f8c-111">La implementación actual devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="98f8c-111">The current implementation returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="98f8c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98f8c-112">Remarks</span></span>

<span data-ttu-id="98f8c-113">Un representador de vídeo que implementa un modo de pantalla completa debe reemplazar esta función miembro e implementar cualquier modo que admita.</span><span class="sxs-lookup"><span data-stu-id="98f8c-113">A video renderer that implements a full-screen mode should override this member function and implement whatever modes it supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="98f8c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98f8c-114">Requirements</span></span>



| <span data-ttu-id="98f8c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="98f8c-115">Requirement</span></span> | <span data-ttu-id="98f8c-116">Value</span><span class="sxs-lookup"><span data-stu-id="98f8c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f8c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98f8c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="98f8c-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98f8c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98f8c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98f8c-119">Library</span></span><br/> | <dl> <span data-ttu-id="98f8c-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="98f8c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98f8c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="98f8c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f8c-122">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="98f8c-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




