---
title: Propiedades de anotación que tienen el WinEvents correspondiente
description: Tenga cuidado al invalidar las propiedades que cambian con frecuencia, especialmente las que examinan los clientes como resultado de un WinEvent (como el estado, el valor y, para algunos controles, las propiedades de nombre).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420962"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a><span data-ttu-id="a6444-103">Propiedades de anotación que tienen el WinEvents correspondiente</span><span class="sxs-lookup"><span data-stu-id="a6444-103">Annotation Properties That Have Corresponding WinEvents</span></span>

<span data-ttu-id="a6444-104">Tenga cuidado al invalidar las propiedades que cambian con frecuencia, especialmente las que examinan los clientes como resultado de un WinEvent (como el [**Estado**](state-property.md), el [**valor**](value-property.md)y, para algunos controles, las propiedades de [**nombre**](name-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="a6444-104">Be careful when overriding properties that change frequently, particularly those that are examined by clients as a result of a WinEvent (such as [**State**](state-property.md), [**Value**](value-property.md), and, for some controls, the [**Name**](name-property.md) properties).</span></span>

<span data-ttu-id="a6444-105">En muchos casos, especialmente en el caso de los controles USER y ComCtl, el WinEvent que señala un cambio de propiedad se envía antes de que se notifique al propietario del control (normalmente a través de [WM \_ Notify](../controls/wm-notify.md)).</span><span class="sxs-lookup"><span data-stu-id="a6444-105">In many cases, especially for USER and ComCtl controls, the WinEvent signaling a property change is sent before the owner of the control is notified (typically via [WM\_NOTIFY](../controls/wm-notify.md)).</span></span> <span data-ttu-id="a6444-106">La actualización de la propiedad mediante [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) en el controlador de notificaciones de WM será \_ demasiado tardía; los clientes que usen el enlace en contexto ya tendrán acceso al valor anterior.</span><span class="sxs-lookup"><span data-stu-id="a6444-106">Updating the property using [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) in the WM\_NOTIFY handler will be too late; clients using in-context hooking will already have accessed the old value.</span></span>

<span data-ttu-id="a6444-107">Puede controlar estos tipos de propiedades mediante el uso de objetos de servidor de devolución de llamada (mediante [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); sin embargo, el servidor no puede usar ningún Estado que se actualice en el \_ controlador de notificaciones de WM porque todavía no se ha llamado a ese controlador.</span><span class="sxs-lookup"><span data-stu-id="a6444-107">You can handle these types of properties by using callback server objects (using [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); however, the server cannot use any state that is updated in the WM\_NOTIFY handler because that handler will not yet have been called.</span></span> <span data-ttu-id="a6444-108">Por ejemplo, en lugar de usar una variable de valor actual almacenada en caché que se actualice en el controlador de notificaciones de WM y que no \_ esté actualizada, el objeto de devolución de llamada [**IAccPropServer:: GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) debería enviar un mensaje directamente al control para obtener su verdadero valor actual para generar la propiedad necesaria.</span><span class="sxs-lookup"><span data-stu-id="a6444-108">For example, instead of using a cached current value variable that is updated in the WM\_NOTIFY handler and will be out-of-date, the [**IAccPropServer::GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) callback object should send a message directly to the control to get its true current value to generate the required property.</span></span>

 

 