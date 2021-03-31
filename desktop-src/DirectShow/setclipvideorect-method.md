---
description: El método SetClipVideoRect amplía la presentación de vídeo al subrectángulo especificado.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Método SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805870"
---
# <a name="setclipvideorect-method"></a><span data-ttu-id="07105-103">Método SetClipVideoRect</span><span class="sxs-lookup"><span data-stu-id="07105-103">SetClipVideoRect Method</span></span>

> [!Note]  
> <span data-ttu-id="07105-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="07105-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="07105-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="07105-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="07105-106">El `SetClipVideoRect` método amplía la presentación del vídeo al subrectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="07105-106">The `SetClipVideoRect` method zooms the video display to the specified subrectangle.</span></span>

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a><span data-ttu-id="07105-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07105-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07105-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span><span class="sxs-lookup"><span data-stu-id="07105-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span></span>
</dt> <dd>

<span data-ttu-id="07105-109">Especifica un objeto [DVDRect](dvdrect-object.md) , que contiene el rectángulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="07105-109">Specifies a [DVDRect](dvdrect-object.md) object, which contains the clipping rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07105-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07105-110">Return Value</span></span>

<span data-ttu-id="07105-111">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="07105-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07105-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07105-112">Remarks</span></span>

<span data-ttu-id="07105-113">Cuando se establece un nuevo rectángulo de recorte, el objeto amplía ese área para ajustarse a las dimensiones generales de presentación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="07105-113">When you set a new clipping rectangle, the object enlarges that area to fit within the application's overall display dimensions.</span></span> <span data-ttu-id="07105-114">Esto crea el efecto acercar en un área determinada de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="07105-114">This creates the effect zooming in on a particular area of the screen.</span></span> <span data-ttu-id="07105-115">Para especificar el rectángulo, cree un nuevo objeto [DVDRect](dvdrect-object.md) y rellene sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="07105-115">To specify the rectangle, create a new [DVDRect](dvdrect-object.md) object and fill in its properties.</span></span>

<span data-ttu-id="07105-116">El rectángulo más común para la visualización de vídeo es 720 x 540.</span><span class="sxs-lookup"><span data-stu-id="07105-116">The most common rectangle for video display is 720 x 540.</span></span>

## <a name="see-also"></a><span data-ttu-id="07105-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="07105-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07105-118">**GetClipVideoRect**</span><span class="sxs-lookup"><span data-stu-id="07105-118">**GetClipVideoRect**</span></span>](getclipvideorect-method.md)
</dt> </dl>

 

 



