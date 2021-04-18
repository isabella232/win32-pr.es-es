---
description: El método OnPaletteChange controla los mensajes de cambio de paleta.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Método CBaseWindow. OnPaletteChange (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679182"
---
# <a name="cbasewindowonpalettechange-method"></a><span data-ttu-id="cc0cf-103">CBaseWindow. OnPaletteChange, método</span><span class="sxs-lookup"><span data-stu-id="cc0cf-103">CBaseWindow.OnPaletteChange method</span></span>

<span data-ttu-id="cc0cf-104">El `OnPaletteChange` método controla los mensajes de cambio de paleta.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-104">The `OnPaletteChange` method handles palette-change messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc0cf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc0cf-105">Syntax</span></span>


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a><span data-ttu-id="cc0cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc0cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc0cf-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="cc0cf-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="cc0cf-108">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="cc0cf-109">*Message*</span><span class="sxs-lookup"><span data-stu-id="cc0cf-109">*Message*</span></span> 
</dt> <dd>

<span data-ttu-id="cc0cf-110">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-110">Message identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc0cf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc0cf-111">Return value</span></span>

<span data-ttu-id="cc0cf-112">Devuelve 0 si se procesó el mensaje o 1 si no se procesó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-112">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc0cf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc0cf-113">Remarks</span></span>

<span data-ttu-id="cc0cf-114">Este método controla \_ los mensajes de WM PALETTECHANGED y WM \_ QUERYNEWPALETTE.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-114">This method handles WM\_PALETTECHANGED and WM\_QUERYNEWPALETTE messages.</span></span> <span data-ttu-id="cc0cf-115">Llama al método [**CBaseWindow::D orealisepalette**](cbasewindow-dorealisepalette.md) para obtener la nueva paleta.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-115">It calls the [**CBaseWindow::DoRealisePalette**](cbasewindow-dorealisepalette.md) method to realize the new palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc0cf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc0cf-116">Requirements</span></span>



| <span data-ttu-id="cc0cf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc0cf-117">Requirement</span></span> | <span data-ttu-id="cc0cf-118">Value</span><span class="sxs-lookup"><span data-stu-id="cc0cf-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc0cf-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc0cf-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cc0cf-120"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc0cf-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc0cf-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc0cf-121">Library</span></span><br/> | <dl> <span data-ttu-id="cc0cf-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cc0cf-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc0cf-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc0cf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc0cf-124">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="cc0cf-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




