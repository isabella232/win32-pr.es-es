---
description: La propiedad CurrentButton recupera el número del botón de menú seleccionado.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Propiedad CurrentButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359971"
---
# <a name="currentbutton-property"></a><span data-ttu-id="45a57-103">Propiedad CurrentButton</span><span class="sxs-lookup"><span data-stu-id="45a57-103">CurrentButton Property</span></span>

> [!Note]  
> <span data-ttu-id="45a57-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="45a57-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="45a57-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="45a57-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="45a57-106">La `CurrentButton` propiedad recupera el número del botón de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="45a57-106">The `CurrentButton` property retrieves the number of the selected menu button.</span></span>

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a><span data-ttu-id="45a57-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45a57-107">Return Value</span></span>

<span data-ttu-id="45a57-108">Devuelve un valor entero que representa el botón.</span><span class="sxs-lookup"><span data-stu-id="45a57-108">Returns an integer value representing the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="45a57-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45a57-109">Remarks</span></span>

<span data-ttu-id="45a57-110">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="45a57-110">This property is read-only with no default value.</span></span> <span data-ttu-id="45a57-111">Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="45a57-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="45a57-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="45a57-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a57-113">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="45a57-113">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="45a57-114">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="45a57-114">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="45a57-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="45a57-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="45a57-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="45a57-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="45a57-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="45a57-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="45a57-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="45a57-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



