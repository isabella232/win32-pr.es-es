---
description: El método GetButtonAtPosition recupera el número del botón en las coordenadas especificadas sin seleccionarlo o activarlo.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Método GetButtonAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152008"
---
# <a name="getbuttonatposition-method"></a><span data-ttu-id="bb726-103">Método GetButtonAtPosition</span><span class="sxs-lookup"><span data-stu-id="bb726-103">GetButtonAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="bb726-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb726-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bb726-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="bb726-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bb726-106">El `GetButtonAtPosition` método recupera el número del botón en las coordenadas especificadas sin seleccionarlo o activarlo.</span><span class="sxs-lookup"><span data-stu-id="bb726-106">The `GetButtonAtPosition` method retrieves the number of the button at the specified coordinates without selecting or activating it.</span></span>

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="bb726-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb726-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb726-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="bb726-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="bb726-109">Especifica la coordenada x del puntero del mouse como un entero.</span><span class="sxs-lookup"><span data-stu-id="bb726-109">Specifies the x-coordinate of the mouse pointer as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="bb726-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="bb726-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="bb726-111">Especifica la coordenada y del puntero del mouse como un entero.</span><span class="sxs-lookup"><span data-stu-id="bb726-111">Specifies the y-coordinate of the mouse pointer as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb726-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb726-112">Return Value</span></span>

<span data-ttu-id="bb726-113">Devuelve un valor entero que especifica el botón, si existe, en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="bb726-113">Returns an integer value specifying the button, if any, at the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb726-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb726-114">Remarks</span></span>

<span data-ttu-id="bb726-115">Este método devuelve cero si no hay ningún botón presente en las coordenadas especificadas.</span><span class="sxs-lookup"><span data-stu-id="bb726-115">This method returns zero if no button is present at the given coordinates.</span></span> <span data-ttu-id="bb726-116">Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="bb726-116">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb726-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb726-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb726-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="bb726-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="bb726-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="bb726-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="bb726-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="bb726-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="bb726-121">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="bb726-121">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="bb726-122">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="bb726-122">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="bb726-123">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="bb726-123">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



