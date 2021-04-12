---
description: El método SetPalette instala una paleta para la ventana. Este método no tiene parámetros.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: 'Método CBaseWindow. SetPalette (Winutil. h): no hay parámetros'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104280536"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a><span data-ttu-id="60fd1-104">Método CBaseWindow. SetPalette (Winutil. h): no hay parámetros</span><span class="sxs-lookup"><span data-stu-id="60fd1-104">CBaseWindow.SetPalette method (Winutil.h) - No parameters</span></span>

<span data-ttu-id="60fd1-105">El `SetPalette` método instala una paleta para la ventana.</span><span class="sxs-lookup"><span data-stu-id="60fd1-105">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="60fd1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60fd1-106">Syntax</span></span>


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a><span data-ttu-id="60fd1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60fd1-107">Parameters</span></span>

<span data-ttu-id="60fd1-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="60fd1-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="60fd1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60fd1-109">Return value</span></span>

<span data-ttu-id="60fd1-110">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="60fd1-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="60fd1-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="60fd1-111">Return code</span></span>                                                                             | <span data-ttu-id="60fd1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="60fd1-112">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="60fd1-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="60fd1-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="60fd1-114">Una llamada interna a **GdiFlush** devolvió un error.</span><span class="sxs-lookup"><span data-stu-id="60fd1-114">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="60fd1-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="60fd1-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="60fd1-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="60fd1-116">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="60fd1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60fd1-117">Remarks</span></span>

<span data-ttu-id="60fd1-118">La paleta proporcionada por la variable miembro [**CBaseWindow:: m \_ hPalette**](cbasewindow-m-hpalette.md) está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="60fd1-118">The palette given by the [**CBaseWindow::m\_hPalette**](cbasewindow-m-hpalette.md) member variable is selected.</span></span> <span data-ttu-id="60fd1-119">El autor de la llamada debe garantizar la validez de **m \_ hPalette**.</span><span class="sxs-lookup"><span data-stu-id="60fd1-119">The caller must ensure the validity of **m\_hPalette**.</span></span>

<span data-ttu-id="60fd1-120">Si el valor de la variable miembro [**CBaseWindow:: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) es **false** (valor predeterminado), este método selecciona la paleta y la realiza.</span><span class="sxs-lookup"><span data-stu-id="60fd1-120">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="60fd1-121">De lo contrario, selecciona la paleta pero no la detecta.</span><span class="sxs-lookup"><span data-stu-id="60fd1-121">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="60fd1-122">El objeto no elimina ninguna de las paletas anteriores que estaba usando.</span><span class="sxs-lookup"><span data-stu-id="60fd1-122">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="60fd1-123">El autor de la llamada es responsable de eliminar las paletas.</span><span class="sxs-lookup"><span data-stu-id="60fd1-123">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="60fd1-124">Cualquier subproceso puede llamar con seguridad a este método, no solo al subproceso que posee la ventana.</span><span class="sxs-lookup"><span data-stu-id="60fd1-124">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="60fd1-125">La ventana envía un mensaje privado a sí mismo, lo que desencadena una llamada al método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="60fd1-125">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="60fd1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60fd1-126">Requirements</span></span>

| <span data-ttu-id="60fd1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="60fd1-127">Requirement</span></span> | <span data-ttu-id="60fd1-128">Value</span><span class="sxs-lookup"><span data-stu-id="60fd1-128">Value</span></span> |
|-|-|
| <span data-ttu-id="60fd1-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60fd1-129">Header</span></span> | <span data-ttu-id="60fd1-130">Winutil. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="60fd1-130">Winutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="60fd1-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60fd1-131">Library</span></span>| <span data-ttu-id="60fd1-132">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="60fd1-132">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="60fd1-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="60fd1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fd1-134">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="60fd1-134">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




