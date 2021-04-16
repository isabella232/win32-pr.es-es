---
description: El método SelectAndActivateButton selecciona y activa el botón especificado.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Método SelectAndActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686302"
---
# <a name="selectandactivatebutton-method"></a><span data-ttu-id="6a435-103">Método SelectAndActivateButton</span><span class="sxs-lookup"><span data-stu-id="6a435-103">SelectAndActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="6a435-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6a435-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6a435-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="6a435-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6a435-106">El `SelectAndActivateButton` método selecciona y activa el botón especificado.</span><span class="sxs-lookup"><span data-stu-id="6a435-106">The `SelectAndActivateButton` method selects and activates the specified button.</span></span>

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a><span data-ttu-id="6a435-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a435-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a435-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="6a435-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="6a435-109">Especifica el botón como un entero.</span><span class="sxs-lookup"><span data-stu-id="6a435-109">Specifies the button as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a435-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a435-110">Return Value</span></span>

<span data-ttu-id="6a435-111">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6a435-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a435-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a435-112">Remarks</span></span>

<span data-ttu-id="6a435-113">Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="6a435-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="6a435-114">Este método resalta el botón especificado y lo activa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6a435-114">This method highlights the specified button and activate it automatically.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a435-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a435-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a435-116">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="6a435-116">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="6a435-117">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="6a435-117">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="6a435-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="6a435-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="6a435-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="6a435-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="6a435-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="6a435-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="6a435-121">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="6a435-121">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



