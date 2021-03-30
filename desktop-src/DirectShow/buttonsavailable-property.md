---
description: La propiedad ButtonsAvailable recupera el número total de botones del menú actual.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Propiedad ButtonsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423019"
---
# <a name="buttonsavailable-property"></a><span data-ttu-id="dee3e-103">Propiedad ButtonsAvailable</span><span class="sxs-lookup"><span data-stu-id="dee3e-103">ButtonsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="dee3e-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dee3e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dee3e-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="dee3e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dee3e-106">La `ButtonsAvailable` propiedad recupera el número total de botones del menú actual.</span><span class="sxs-lookup"><span data-stu-id="dee3e-106">The `ButtonsAvailable` property retrieves the total number of buttons on the current menu.</span></span>

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a><span data-ttu-id="dee3e-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dee3e-107">Return Value</span></span>

<span data-ttu-id="dee3e-108">Devuelve un valor entero que representa el número de botones.</span><span class="sxs-lookup"><span data-stu-id="dee3e-108">Returns an integer value representing the number of buttons.</span></span>

## <a name="remarks"></a><span data-ttu-id="dee3e-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dee3e-109">Remarks</span></span>

<span data-ttu-id="dee3e-110">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dee3e-110">This property is read-only with no default value.</span></span> <span data-ttu-id="dee3e-111">Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="dee3e-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="dee3e-112">Llame a este método para recuperar el límite superior para el intervalo de números de botón válidos.</span><span class="sxs-lookup"><span data-stu-id="dee3e-112">Call this method to retrieve the upper limit for the range of valid button numbers.</span></span>

## <a name="see-also"></a><span data-ttu-id="dee3e-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="dee3e-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee3e-114">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="dee3e-114">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="dee3e-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="dee3e-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="dee3e-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="dee3e-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="dee3e-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="dee3e-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="dee3e-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="dee3e-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



