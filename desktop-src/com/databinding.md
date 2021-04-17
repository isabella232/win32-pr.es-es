---
title: Enlace de datos
description: Enlace de datos
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705039"
---
# <a name="databinding"></a><span data-ttu-id="fa694-103">Enlace de datos</span><span class="sxs-lookup"><span data-stu-id="fa694-103">Databinding</span></span>

<span data-ttu-id="fa694-104">Se ha agregado un nuevo atributo DataBinding para permitir que las propiedades distinga entre la comunicación de los cambios solo cuando el foco sale del control o durante todas las notificaciones de cambio de propiedad.</span><span class="sxs-lookup"><span data-stu-id="fa694-104">A new databinding attribute has been added to allow properties distinguish between communicating changes only when focus leaves the control or during all property change notifications.</span></span>

<span data-ttu-id="fa694-105">El nuevo atributo, conocido como ImmediateBind, permite a los controles diferenciar dos tipos diferentes de propiedades enlazables.</span><span class="sxs-lookup"><span data-stu-id="fa694-105">The new attribute, known as ImmediateBind, enables controls to differentiate two different types of bindable properties.</span></span> <span data-ttu-id="fa694-106">Un tipo de propiedad enlazable debe notificar cada cambio en la base de datos, por ejemplo, con un control de casilla en el que es necesario enviar cada cambio a la base de datos subyacente, aunque el control no haya perdido el foco.</span><span class="sxs-lookup"><span data-stu-id="fa694-106">One type of bindable property needs to notify every change to the database, for example with a check box control where every change needs to be sent through to the underlying database even though the control has not lost the focus.</span></span> <span data-ttu-id="fa694-107">Sin embargo, los controles, como un cuadro de lista, solo quieren que el cambio de una propiedad reciba una notificación a la base de datos cuando el control pierde el foco, ya que es posible que el usuario haya cambiado la selección resaltada con las teclas de dirección antes de encontrar el valor deseado, de modo que la notificación de cambios se envíe a la base de datos cada vez que el usuario</span><span class="sxs-lookup"><span data-stu-id="fa694-107">However controls such as a listbox only wish to have the change of a property notified to the database when the control loses focus, as the user may have changed the highlighted selection with the arrow keys before finding the desired setting, to have the change notification sent to the database every time that the user hit the arrow key would be give unacceptable performance.</span></span> <span data-ttu-id="fa694-108">La nueva propiedad de enlace inmediato permite que las propiedades enlazables individuales de un formulario tengan este comportamiento especificado. cuando se establece este bit, se notificará a todos los cambios.</span><span class="sxs-lookup"><span data-stu-id="fa694-108">The new immediate bind property allows individual bindable properties on a form to have this behavior specified, when this bit is set all changes will be notified.</span></span>

<span data-ttu-id="fa694-109">El nuevo bit ImmediateBind se asigna a los nuevos \_ bits VARFLAG FIMMEDIATEBIND (0x80) y FUNCFLAG \_ FIMMEDIATEBIND (0x80) en las enumeraciones VARFLAGS y FUNCFLAGS de la interfaz [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) , lo que permite inspeccionar los atributos de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="fa694-109">The new ImmediateBind bit maps through to the new VARFLAG\_FIMMEDIATEBIND (0x80) and the FUNCFLAG\_FIMMEDIATEBIND (0x80) bits in the VARFLAGS and FUNCFLAGS enumerations for the [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interface allowing for the properties attributes to be inspected.</span></span>

 

 