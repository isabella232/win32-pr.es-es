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
# <a name="overloading-ipropertynotifysink"></a>Sobrecarga de IPropertyNotifySink

Muchos contenedores de controles ActiveX implementan una ventana de exploración de propiedades no modal. Si las propiedades de un control se modifican a través de las páginas de propiedades del control, las propiedades del control pueden no estar sincronizadas con la vista del contenedor de esas propiedades (el control siempre es correcto, por supuesto). Para asegurarse de que siempre tiene los valores actuales de las propiedades de un control, un contenedor de controles ActiveX puede sobrecargar la interfaz [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (enlace de datos) y también utilizarla para recibir una notificación de que una propiedad de control ha cambiado. Esta técnica es opcional y no es necesaria para los contenedores de controles ActiveX o los controles ActiveX.

Tenga en cuenta que un control solo debe usar [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) para el enlace de datos; es libre de usar [**onchange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) para ambos propósitos o para ambos.

 

 




