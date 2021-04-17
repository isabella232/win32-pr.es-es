---
description: El método SetPalette instala una paleta para la ventana.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Método CBaseWindow. SetPalette (Winutil. h)
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
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660313"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a><span data-ttu-id="17c49-103">Método CBaseWindow. SetPalette (Winutil. h)</span><span class="sxs-lookup"><span data-stu-id="17c49-103">CBaseWindow.SetPalette method (Winutil.h)</span></span>

<span data-ttu-id="17c49-104">El `SetPalette` método instala una paleta para la ventana.</span><span class="sxs-lookup"><span data-stu-id="17c49-104">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17c49-105">Syntax</span></span>


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a><span data-ttu-id="17c49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17c49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c49-107">*hPalette*</span><span class="sxs-lookup"><span data-stu-id="17c49-107">*hPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="17c49-108">Identificador de la nueva paleta.</span><span class="sxs-lookup"><span data-stu-id="17c49-108">Handle to the new palette.</span></span> <span data-ttu-id="17c49-109">No puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="17c49-109">Cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c49-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17c49-110">Return value</span></span>

<span data-ttu-id="17c49-111">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="17c49-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="17c49-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="17c49-112">Return code</span></span>                                                                             | <span data-ttu-id="17c49-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="17c49-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="17c49-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="17c49-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="17c49-115">Una llamada interna a **GdiFlush** devolvió un error.</span><span class="sxs-lookup"><span data-stu-id="17c49-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="17c49-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="17c49-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="17c49-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="17c49-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="17c49-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17c49-118">Remarks</span></span>

<span data-ttu-id="17c49-119">Si el valor de la variable miembro [**CBaseWindow:: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) es **false** (valor predeterminado), este método selecciona la paleta y la realiza.</span><span class="sxs-lookup"><span data-stu-id="17c49-119">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="17c49-120">De lo contrario, selecciona la paleta pero no la detecta.</span><span class="sxs-lookup"><span data-stu-id="17c49-120">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="17c49-121">El objeto no elimina ninguna de las paletas anteriores que estaba usando.</span><span class="sxs-lookup"><span data-stu-id="17c49-121">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="17c49-122">El autor de la llamada es responsable de eliminar las paletas.</span><span class="sxs-lookup"><span data-stu-id="17c49-122">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="17c49-123">Cualquier subproceso puede llamar con seguridad a este método, no solo al subproceso que posee la ventana.</span><span class="sxs-lookup"><span data-stu-id="17c49-123">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="17c49-124">La ventana envía un mensaje privado a sí mismo, lo que desencadena una llamada al método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="17c49-124">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="17c49-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17c49-125">Requirements</span></span>



| <span data-ttu-id="17c49-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c49-126">Requirement</span></span> | <span data-ttu-id="17c49-127">Value</span><span class="sxs-lookup"><span data-stu-id="17c49-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c49-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17c49-128">Header</span></span><br/>  | <dl> <span data-ttu-id="17c49-129"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17c49-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17c49-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17c49-130">Library</span></span><br/> | <dl> <span data-ttu-id="17c49-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="17c49-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17c49-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="17c49-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c49-133">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="17c49-133">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




