---
description: El \_ método put BackgroundPalette establece una marca para obtener la paleta en segundo plano.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Método CBaseControlWindow.put_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660629"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a><span data-ttu-id="3d814-103">CBaseControlWindow. put \_ BackgroundPalette (método)</span><span class="sxs-lookup"><span data-stu-id="3d814-103">CBaseControlWindow.put\_BackgroundPalette method</span></span>

<span data-ttu-id="3d814-104">El `put_BackgroundPalette` método establece una marca para obtener la paleta en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="3d814-104">The `put_BackgroundPalette` method sets a flag to realize the palette in the background.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d814-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d814-105">Syntax</span></span>


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="3d814-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d814-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d814-107">*BackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="3d814-107">*BackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="3d814-108">Marca booleana de Automation (0 está desactivado, 1 en).</span><span class="sxs-lookup"><span data-stu-id="3d814-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d814-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d814-109">Return value</span></span>

<span data-ttu-id="3d814-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3d814-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d814-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d814-111">Remarks</span></span>

<span data-ttu-id="3d814-112">Para reproducir un vídeo dentro de otra aplicación o documento, es posible que la aplicación desee usar su propia paleta.</span><span class="sxs-lookup"><span data-stu-id="3d814-112">To play a video within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="3d814-113">Puede solicitar que el vídeo use la paleta de primer plano actual en lugar de la suya propia como paleta de fondo; para ello, establezca esta marca en 1.</span><span class="sxs-lookup"><span data-stu-id="3d814-113">It can ask that the video use the current foreground palette rather than its own as the background palette by setting this flag to  1.</span></span> <span data-ttu-id="3d814-114">Si se establece en 0, la ventana instalará y obtendrá su propia paleta preferida.</span><span class="sxs-lookup"><span data-stu-id="3d814-114">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="3d814-115">Pedir a la ventana que use una paleta diferente producirá penalizaciones de rendimiento graves.</span><span class="sxs-lookup"><span data-stu-id="3d814-115">Asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d814-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d814-116">Requirements</span></span>



| <span data-ttu-id="3d814-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d814-117">Requirement</span></span> | <span data-ttu-id="3d814-118">Value</span><span class="sxs-lookup"><span data-stu-id="3d814-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d814-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d814-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3d814-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d814-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d814-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d814-121">Library</span></span><br/> | <dl> <span data-ttu-id="3d814-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3d814-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d814-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d814-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d814-124">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="3d814-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




