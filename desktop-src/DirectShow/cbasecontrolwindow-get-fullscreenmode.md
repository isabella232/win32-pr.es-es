---
description: El \_ método get FullScreenMode recupera el modo de pantalla completa actual.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: Método CBaseControlWindow.get_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671168"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a><span data-ttu-id="914f6-103">CBaseControlWindow. Get \_ FullScreenMode (método)</span><span class="sxs-lookup"><span data-stu-id="914f6-103">CBaseControlWindow.get\_FullScreenMode method</span></span>

<span data-ttu-id="914f6-104">El `get_FullScreenMode` método recupera el modo de pantalla completa actual.</span><span class="sxs-lookup"><span data-stu-id="914f6-104">The `get_FullScreenMode` method retrieves the current full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="914f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="914f6-105">Syntax</span></span>


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="914f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="914f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="914f6-107">*FullScreenMode*</span><span class="sxs-lookup"><span data-stu-id="914f6-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="914f6-108">Puntero al modo de pantalla completa actual.</span><span class="sxs-lookup"><span data-stu-id="914f6-108">Pointer to the current full-screen mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="914f6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="914f6-109">Return value</span></span>

<span data-ttu-id="914f6-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="914f6-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="914f6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="914f6-111">Remarks</span></span>

<span data-ttu-id="914f6-112">Esta función miembro devuelve E \_ NOTIMPL de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="914f6-112">This member function returns E\_NOTIMPL by default.</span></span> <span data-ttu-id="914f6-113">Esto informa al distribuidor del complemento de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) de que este representador no implementa un representador de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="914f6-113">This informs the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor that this renderer does not implement a full-screen renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="914f6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="914f6-114">Requirements</span></span>



| <span data-ttu-id="914f6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="914f6-115">Requirement</span></span> | <span data-ttu-id="914f6-116">Value</span><span class="sxs-lookup"><span data-stu-id="914f6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="914f6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="914f6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="914f6-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="914f6-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="914f6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="914f6-119">Library</span></span><br/> | <dl> <span data-ttu-id="914f6-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="914f6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="914f6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="914f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="914f6-122">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="914f6-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




