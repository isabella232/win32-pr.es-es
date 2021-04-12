---
description: El método GetButtonRect recupera el rectángulo para el botón especificado, en coordenadas de ventana.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Método GetButtonRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152007"
---
# <a name="getbuttonrect-method"></a><span data-ttu-id="07f03-103">Método GetButtonRect</span><span class="sxs-lookup"><span data-stu-id="07f03-103">GetButtonRect Method</span></span>

> [!Note]  
> <span data-ttu-id="07f03-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="07f03-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="07f03-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="07f03-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="07f03-106">El `GetButtonRect` método recupera el rectángulo para el botón especificado, en coordenadas de ventana.</span><span class="sxs-lookup"><span data-stu-id="07f03-106">The `GetButtonRect` method retrieves the rectangle for the specified button, in window coordinates.</span></span>

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a><span data-ttu-id="07f03-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07f03-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07f03-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="07f03-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="07f03-109">Especifica el número de botón como un entero.</span><span class="sxs-lookup"><span data-stu-id="07f03-109">Specifies the button number as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07f03-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07f03-110">Return Value</span></span>

<span data-ttu-id="07f03-111">Devuelve un objeto [DVDRect](dvdrect-object.md) que define el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="07f03-111">Returns a [DVDRect](dvdrect-object.md) object that defines the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="07f03-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07f03-112">Remarks</span></span>

<span data-ttu-id="07f03-113">Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="07f03-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="07f03-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="07f03-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f03-115">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="07f03-115">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="07f03-116">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="07f03-116">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="07f03-117">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="07f03-117">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="07f03-118">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="07f03-118">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="07f03-119">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="07f03-119">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



