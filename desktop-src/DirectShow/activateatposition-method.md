---
description: El método ActivateAtPosition activa el botón de menú en la posición especificada.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Método ActivateAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152605"
---
# <a name="activateatposition-method"></a><span data-ttu-id="8d748-103">Método ActivateAtPosition</span><span class="sxs-lookup"><span data-stu-id="8d748-103">ActivateAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="8d748-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8d748-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8d748-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="8d748-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8d748-106">El método ActivateAtPosition activa el botón de menú en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="8d748-106">The ActivateAtPosition method activates the menu button at the specified position.</span></span>

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="8d748-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d748-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d748-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="8d748-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="8d748-109">Especifica la coordenada x como un entero.</span><span class="sxs-lookup"><span data-stu-id="8d748-109">Specifies x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="8d748-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="8d748-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="8d748-111">Especifica la coordenada y como un entero.</span><span class="sxs-lookup"><span data-stu-id="8d748-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d748-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d748-112">Return Value</span></span>

<span data-ttu-id="8d748-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8d748-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d748-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d748-114">Remarks</span></span>

<span data-ttu-id="8d748-115">Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="8d748-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d748-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d748-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d748-117">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="8d748-117">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="8d748-118">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="8d748-118">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="8d748-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="8d748-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="8d748-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="8d748-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="8d748-121">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="8d748-121">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="8d748-122">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="8d748-122">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



