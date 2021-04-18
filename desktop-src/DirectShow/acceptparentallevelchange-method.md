---
description: El método AcceptParentalLevelChange acepta o rechaza el nuevo nivel de administración parental temporal.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Método AcceptParentalLevelChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686416"
---
# <a name="acceptparentallevelchange-method"></a><span data-ttu-id="69446-103">Método AcceptParentalLevelChange</span><span class="sxs-lookup"><span data-stu-id="69446-103">AcceptParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="69446-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="69446-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="69446-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="69446-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="69446-106">El método AcceptParentalLevelChange acepta o rechaza el nuevo nivel de administración parental temporal.</span><span class="sxs-lookup"><span data-stu-id="69446-106">The AcceptParentalLevelChange method accepts or rejects the new temporary parental management level.</span></span>

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a><span data-ttu-id="69446-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69446-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69446-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span><span class="sxs-lookup"><span data-stu-id="69446-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span></span>
</dt> <dd>

<span data-ttu-id="69446-109">Especifica el nuevo nivel parental como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="69446-109">Specifies the new parental level as a Boolean value.</span></span>



| <span data-ttu-id="69446-110">Value</span><span class="sxs-lookup"><span data-stu-id="69446-110">Value</span></span> | <span data-ttu-id="69446-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="69446-111">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="69446-112">true</span><span class="sxs-lookup"><span data-stu-id="69446-112">true</span></span>  | <span data-ttu-id="69446-113">Acepte el nuevo nivel de administración parental.</span><span class="sxs-lookup"><span data-stu-id="69446-113">Accept the new parental management level.</span></span> |
| <span data-ttu-id="69446-114">false</span><span class="sxs-lookup"><span data-stu-id="69446-114">false</span></span> | <span data-ttu-id="69446-115">Rechace el nuevo nivel de administración parental.</span><span class="sxs-lookup"><span data-stu-id="69446-115">Reject the new parental management level.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69446-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69446-116">Return Value</span></span>

<span data-ttu-id="69446-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="69446-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69446-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69446-118">Remarks</span></span>

<span data-ttu-id="69446-119">Llame a este método en respuesta a una \_ notificación de evento de cambio de nivel parental de DVD de EC \_ \_ \_ para especificar si el navegador de DVD debe reproducir el contenido con el nuevo nivel parental, o bien bifurcar a donde el disco especifique si se rechaza el nuevo nivel.</span><span class="sxs-lookup"><span data-stu-id="69446-119">Call this method in response to an EC\_DVD\_PARENTAL\_LEVEL\_CHANGE event notification to specify whether the DVD Navigator should play the content with the new parental level, or branch to where the disc specifies if the new level is rejected.</span></span>

## <a name="see-also"></a><span data-ttu-id="69446-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="69446-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69446-121">Aplicar niveles de administración parental</span><span class="sxs-lookup"><span data-stu-id="69446-121">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
</dt> <dt>

[<span data-ttu-id="69446-122">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="69446-122">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="69446-123">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="69446-123">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="69446-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="69446-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="69446-125">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="69446-125">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="69446-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="69446-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="69446-127">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="69446-127">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



