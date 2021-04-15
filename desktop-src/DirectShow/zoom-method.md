---
description: El método de zoom amplía el vídeo mostrado hacia arriba o hacia afuera, centrado en un conjunto determinado de coordenadas de pantalla.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497981"
---
# <a name="zoom-method"></a><span data-ttu-id="54ebb-103">Zoom (método)</span><span class="sxs-lookup"><span data-stu-id="54ebb-103">Zoom Method</span></span>

> [!Note]  
> <span data-ttu-id="54ebb-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="54ebb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="54ebb-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="54ebb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="54ebb-106">El `Zoom` método amplía el vídeo mostrado hacia arriba o hacia afuera, centrado en un conjunto determinado de coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="54ebb-106">The `Zoom` method zooms the video display in or out, centered on a given set of screen coordinates.</span></span>

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a><span data-ttu-id="54ebb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54ebb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54ebb-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span><span class="sxs-lookup"><span data-stu-id="54ebb-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span></span>
</dt> <dd>

<span data-ttu-id="54ebb-109">Especifica la coordenada x en el centro del área de zoom rectangular como un entero.</span><span class="sxs-lookup"><span data-stu-id="54ebb-109">Specifies the x-coordinate at the center of the rectangular zoom area as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="54ebb-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span><span class="sxs-lookup"><span data-stu-id="54ebb-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span></span>
</dt> <dd>

<span data-ttu-id="54ebb-111">Especifica la coordenada y en el centro del rectángulo que se va a ampliar como un entero.</span><span class="sxs-lookup"><span data-stu-id="54ebb-111">Specifies the y-coordinate at the center of the rectangle to be zoomed as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="54ebb-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span><span class="sxs-lookup"><span data-stu-id="54ebb-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span></span>
</dt> <dd>

<span data-ttu-id="54ebb-113">Especifica el factor de ampliación que se aplica al valor de zoom actual como un entero.</span><span class="sxs-lookup"><span data-stu-id="54ebb-113">Specifies the magnification factor applied to the current zoom value as an Integer.</span></span> <span data-ttu-id="54ebb-114">El valor máximo total depende de lo que admita la superposición de hardware; suele ser un factor de 32 a 64 veces el tamaño original.</span><span class="sxs-lookup"><span data-stu-id="54ebb-114">The total maximum value depends on what the hardware overlay can support; this is typically a factor of 32 to 64 times the original size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54ebb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54ebb-115">Return Value</span></span>

<span data-ttu-id="54ebb-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="54ebb-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54ebb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54ebb-117">Remarks</span></span>

<span data-ttu-id="54ebb-118">La nueva relación de zoom permanece en vigor hasta que se restaura al tamaño original o se cambia de nuevo.</span><span class="sxs-lookup"><span data-stu-id="54ebb-118">The new zoom ratio stays in effect until it is restored to the original size or changed again.</span></span> <span data-ttu-id="54ebb-119">En otras palabras, dos llamadas a este método que especifican un *iZoomRatio* de dos darán lugar a una relación de zoom cuatro veces mayor que el tamaño del vídeo original.</span><span class="sxs-lookup"><span data-stu-id="54ebb-119">In other words, two calls to this method specifying an *iZoomRatio* of two will result in a zoom ratio four times larger than the original video size.</span></span> <span data-ttu-id="54ebb-120">Si el usuario intenta hacer zoom más allá de lo que el hardware puede admitir, este método se realizará correctamente, pero no hará nada.</span><span class="sxs-lookup"><span data-stu-id="54ebb-120">If the user tries to zoom beyond what the hardware can support, this method will succeed but do nothing.</span></span>

<span data-ttu-id="54ebb-121">El método [**SetClipVideoRect**](setclipvideorect-method.md) es otra manera de hacer zoom; la única diferencia entre los dos métodos es la forma en que se especifica el rectángulo de zoom.</span><span class="sxs-lookup"><span data-stu-id="54ebb-121">The [**SetClipVideoRect**](setclipvideorect-method.md) method is another way to zoom in; the only difference between the two methods is the way in which the zoom rectangle is specified.</span></span>

 

 



