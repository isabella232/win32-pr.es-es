---
title: Enlace de datos
description: Enlace de datos
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c2040aa29c83615f42c321483c87be378737dcdef47e43873fbe3b8c0902dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048373"
---
# <a name="databinding"></a>Enlace de datos

Se ha agregado un nuevo atributo de enlace de datos para permitir que las propiedades distinga entre comunicar los cambios solo cuando el foco sale del control o durante todas las notificaciones de cambio de propiedad.

El nuevo atributo, conocido como ImmediateBind, permite a los controles diferenciar dos tipos diferentes de propiedades enlazables. Un tipo de propiedad enlazable debe notificar cada cambio a la base de datos, por ejemplo, con un control de casilla en el que cada cambio debe enviarse a través de la base de datos subyacente aunque el control no haya perdido el foco. Sin embargo, los controles como un cuadro de lista solo desean que se notifique el cambio de una propiedad a la base de datos cuando el control pierde el foco, ya que el usuario puede haber cambiado la selección resaltada con las teclas de dirección antes de encontrar la configuración deseada, para que la notificación de cambio se envíe a la base de datos cada vez que el usuario presione la tecla de dirección daría un rendimiento inaceptable. La nueva propiedad de enlace inmediato permite que se especifique este comportamiento en las propiedades enlazables individuales de un formulario, cuando se establezca este bit, se notificarán todos los cambios.

El nuevo bit ImmediateBind se asigna a través de los nuevos \_ bits VARFLAG FIMMEDIATEBIND (0x80) y FUNCFLAG \_ FIMMEDIATEBIND (0x80) en las enumeraciones VARFLAGS y FUNCFLAGS para la interfaz [ITypeInfo,](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) lo que permite inspeccionar los atributos de propiedades.

 

 