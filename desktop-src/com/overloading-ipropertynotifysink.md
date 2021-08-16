---
title: Sobrecarga de IPropertyNotifySink
description: Sobrecarga de IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4faca0027144498138e1a60bf3df9a29b618aeb7eb09198ff97a3dd7616be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310028"
---
# <a name="overloading-ipropertynotifysink"></a>Sobrecarga de IPropertyNotifySink

Muchos ActiveX contenedores de control implementan una ventana de exploración de propiedades modeless. Si las propiedades de un control se modifican a través de las páginas de propiedades del control, las propiedades del control pueden no estar sincronizadas con la vista del contenedor de esas propiedades (el control siempre es correcto, por supuesto). Para asegurarse de que siempre tiene los valores actuales de las propiedades de un control, un contenedor de controles de ActiveX puede sobrecargar la interfaz [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (enlace de datos) y también usarla para recibir notificaciones de que una propiedad de control ha cambiado. Esta técnica es opcional y no es necesaria para ActiveX contenedores de control ni ActiveX controles.

Tenga en cuenta que un control solo [**debe usar OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) para el enlace de datos; Es gratuito usar [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) para uno o ambos propósitos.

 

 




