---
description: El método ActivateButton activa el botón de menú seleccionado.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: Método ActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a463a3aad1ee0dcabc0e5daaa4a4969efa37aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686383"
---
# <a name="activatebutton-method"></a><span data-ttu-id="e87c3-103">Método ActivateButton</span><span class="sxs-lookup"><span data-stu-id="e87c3-103">ActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="e87c3-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e87c3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e87c3-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="e87c3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e87c3-106">El método ActivateButton activa el botón de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e87c3-106">The ActivateButton method activates the selected menu button.</span></span>

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a><span data-ttu-id="e87c3-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e87c3-107">Return Value</span></span>

<span data-ttu-id="e87c3-108">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e87c3-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e87c3-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e87c3-109">Remarks</span></span>

<span data-ttu-id="e87c3-110">Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="e87c3-110">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="e87c3-111">Use este método para activar un botón que se ha seleccionado a través del método [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md)o [**SelectRightButton**](selectrightbutton-method.md) .</span><span class="sxs-lookup"><span data-stu-id="e87c3-111">Use this method to activate a button that has been selected through the [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), or [**SelectRightButton**](selectrightbutton-method.md) method.</span></span>

 

 



