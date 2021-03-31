---
description: El método SelectAtPosition selecciona el botón de menú en las coordenadas especificadas del puntero del mouse.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Método SelectAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805839"
---
# <a name="selectatposition-method"></a><span data-ttu-id="f439b-103">Método SelectAtPosition</span><span class="sxs-lookup"><span data-stu-id="f439b-103">SelectAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="f439b-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f439b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f439b-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="f439b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f439b-106">El `SelectAtPosition` método selecciona el botón de menú en las coordenadas especificadas del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="f439b-106">The `SelectAtPosition` method selects the menu button at the specified mouse pointer coordinates.</span></span>

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="f439b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f439b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f439b-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="f439b-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="f439b-109">Especifica la coordenada x como un entero.</span><span class="sxs-lookup"><span data-stu-id="f439b-109">Specifies the x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="f439b-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="f439b-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="f439b-111">Especifica la coordenada y como un entero.</span><span class="sxs-lookup"><span data-stu-id="f439b-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f439b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f439b-112">Return Value</span></span>

<span data-ttu-id="f439b-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f439b-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f439b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f439b-114">Remarks</span></span>

<span data-ttu-id="f439b-115">Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="f439b-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="f439b-116">Al seleccionar solo se resalta el botón.</span><span class="sxs-lookup"><span data-stu-id="f439b-116">Selecting merely highlights the button.</span></span> <span data-ttu-id="f439b-117">Para enviar el comando asociado a un botón que se ha seleccionado, llame a [**ActivateButton**](activatebutton-method.md).</span><span class="sxs-lookup"><span data-stu-id="f439b-117">To send the command associated with a button that has been selected, call [**ActivateButton**](activatebutton-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f439b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f439b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f439b-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="f439b-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="f439b-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="f439b-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="f439b-121">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="f439b-121">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="f439b-122">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="f439b-122">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="f439b-123">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="f439b-123">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> </dl>

 

 



