---
description: El \_ método get BackgroundPalette recupera la paleta realizada en la marca de fondo.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Método CBaseControlWindow.get_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660259"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a><span data-ttu-id="75e9d-103">CBaseControlWindow. Get \_ BackgroundPalette (método)</span><span class="sxs-lookup"><span data-stu-id="75e9d-103">CBaseControlWindow.get\_BackgroundPalette method</span></span>

<span data-ttu-id="75e9d-104">El `get_BackgroundPalette` método recupera la paleta realizada en la marca de fondo.</span><span class="sxs-lookup"><span data-stu-id="75e9d-104">The `get_BackgroundPalette` method retrieves the realized palette in the background flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e9d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75e9d-105">Syntax</span></span>


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="75e9d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75e9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75e9d-107">*pBackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="75e9d-107">*pBackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="75e9d-108">Puntero a una marca booleana de Automation (0 es OFF, 1 es ON).</span><span class="sxs-lookup"><span data-stu-id="75e9d-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75e9d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75e9d-109">Return value</span></span>

<span data-ttu-id="75e9d-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75e9d-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75e9d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75e9d-111">Remarks</span></span>

<span data-ttu-id="75e9d-112">Esta función miembro implementa el método [**IVideoWindow:: get \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) .</span><span class="sxs-lookup"><span data-stu-id="75e9d-112">This member function implements the [**IVideoWindow::get\_BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) method.</span></span> <span data-ttu-id="75e9d-113">Si se va a reproducir un vídeo dentro de otra aplicación o documento, es posible que la aplicación desee usar su propia paleta.</span><span class="sxs-lookup"><span data-stu-id="75e9d-113">If a video will be played within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="75e9d-114">Puede solicitar que el vídeo use la paleta de primer plano actual en lugar de la suya propia estableciendo esta marca en 1.</span><span class="sxs-lookup"><span data-stu-id="75e9d-114">It can ask that the video use the current foreground palette rather than its own by setting this flag to  1.</span></span> <span data-ttu-id="75e9d-115">Si se establece en 0, la ventana instalará y obtendrá su propia paleta preferida.</span><span class="sxs-lookup"><span data-stu-id="75e9d-115">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="75e9d-116">Tenga en cuenta que pedir a la ventana que use una paleta diferente producirá penalizaciones de rendimiento graves.</span><span class="sxs-lookup"><span data-stu-id="75e9d-116">Note that asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="75e9d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75e9d-117">Requirements</span></span>



| <span data-ttu-id="75e9d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75e9d-118">Requirement</span></span> | <span data-ttu-id="75e9d-119">Value</span><span class="sxs-lookup"><span data-stu-id="75e9d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e9d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75e9d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="75e9d-121"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75e9d-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="75e9d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75e9d-122">Library</span></span><br/> | <dl> <span data-ttu-id="75e9d-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="75e9d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e9d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="75e9d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e9d-125">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="75e9d-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




