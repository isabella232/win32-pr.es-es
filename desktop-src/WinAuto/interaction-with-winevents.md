---
title: Interacción con WinEvents
description: El tiempo de ejecución de la anotación dinámica no enviará WinEvents; es responsabilidad del anotador enviar los eventos adecuados, cuando sea necesario. Si necesita enviar WinEvents, asegúrese de enviarlos una vez realizada la anotación.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aedd09a22371f91a92eca891c77f6c424583b5
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "105714319"
---
# <a name="interaction-with-winevents"></a><span data-ttu-id="ce243-104">Interacción con WinEvents</span><span class="sxs-lookup"><span data-stu-id="ce243-104">Interaction with WinEvents</span></span>

<span data-ttu-id="ce243-105">El tiempo de ejecución de la anotación dinámica no enviará [WinEvents](winevents-infrastructure.md); es responsabilidad del anotador enviar los eventos adecuados, cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ce243-105">The Dynamic Annotation run time will not send [WinEvents](winevents-infrastructure.md); it is the annotator's responsibility to send appropriate events, when necessary.</span></span> <span data-ttu-id="ce243-106">Si necesita enviar WinEvents, asegúrese de enviarlos una vez realizada la anotación.</span><span class="sxs-lookup"><span data-stu-id="ce243-106">If you need to send WinEvents, be sure to send them after the annotation has taken place.</span></span>

<span data-ttu-id="ce243-107">Por ejemplo, si usa [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para establecer la propiedad [**Name**](name-property.md) de un elemento, envíe un evento [**\_ \_ NameChange (del objeto Event**](event-constants.md) para ese objeto después de que **SetPropValue** devuelva.</span><span class="sxs-lookup"><span data-stu-id="ce243-107">For example, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the [**Name**](name-property.md) property of an element, send an [**EVENT\_OBJECT\_NAMECHANGE**](event-constants.md) event for that object after **SetPropValue** returns.</span></span>

<span data-ttu-id="ce243-108">Sin embargo, si usa [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) para establecer ValueMap para un control deslizante, no es necesario ningún evento porque al establecer ValueMap no se cambia el valor del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="ce243-108">However, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the ValueMap for a slider, no events are required because setting the ValueMap does not change the slider's value.</span></span>

 

 




