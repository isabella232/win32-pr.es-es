---
title: Sobrecarga de IPropertyNotifySink
description: Sobrecarga de IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419033"
---
# <a name="overloading-ipropertynotifysink"></a><span data-ttu-id="db9dc-103">Sobrecarga de IPropertyNotifySink</span><span class="sxs-lookup"><span data-stu-id="db9dc-103">Overloading IPropertyNotifySink</span></span>

<span data-ttu-id="db9dc-104">Muchos contenedores de controles ActiveX implementan una ventana de exploración de propiedades no modal.</span><span class="sxs-lookup"><span data-stu-id="db9dc-104">Many ActiveX control containers implement a modeless property browsing window.</span></span> <span data-ttu-id="db9dc-105">Si las propiedades de un control se modifican a través de las páginas de propiedades del control, las propiedades del control pueden no estar sincronizadas con la vista del contenedor de esas propiedades (el control siempre es correcto, por supuesto).</span><span class="sxs-lookup"><span data-stu-id="db9dc-105">If a control's properties are altered through the control's property pages, then the control's properties can get out of sync with the container's view of those properties (the control is always right, of course).</span></span> <span data-ttu-id="db9dc-106">Para asegurarse de que siempre tiene los valores actuales de las propiedades de un control, un contenedor de controles ActiveX puede sobrecargar la interfaz [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (enlace de datos) y también utilizarla para recibir una notificación de que una propiedad de control ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="db9dc-106">To ensure that it always has the current values for a control's properties, an ActiveX control container can overload the [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) interface (data binding) and also use it to be notified that a control property has changed.</span></span> <span data-ttu-id="db9dc-107">Esta técnica es opcional y no es necesaria para los contenedores de controles ActiveX o los controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="db9dc-107">This technique is optional and is not required of ActiveX control containers or ActiveX controls.</span></span>

<span data-ttu-id="db9dc-108">Tenga en cuenta que un control solo debe usar [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) para el enlace de datos; es libre de usar [**onchange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) para ambos propósitos o para ambos.</span><span class="sxs-lookup"><span data-stu-id="db9dc-108">Note that a control should use [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) only for data binding; it is free to use [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) for either or both purposes.</span></span>

 

 




