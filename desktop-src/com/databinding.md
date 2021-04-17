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
# <a name="databinding"></a>Enlace de datos

Se ha agregado un nuevo atributo DataBinding para permitir que las propiedades distinga entre la comunicación de los cambios solo cuando el foco sale del control o durante todas las notificaciones de cambio de propiedad.

El nuevo atributo, conocido como ImmediateBind, permite a los controles diferenciar dos tipos diferentes de propiedades enlazables. Un tipo de propiedad enlazable debe notificar cada cambio en la base de datos, por ejemplo, con un control de casilla en el que es necesario enviar cada cambio a la base de datos subyacente, aunque el control no haya perdido el foco. Sin embargo, los controles, como un cuadro de lista, solo quieren que el cambio de una propiedad reciba una notificación a la base de datos cuando el control pierde el foco, ya que es posible que el usuario haya cambiado la selección resaltada con las teclas de dirección antes de encontrar el valor deseado, de modo que la notificación de cambios se envíe a la base de datos cada vez que el usuario La nueva propiedad de enlace inmediato permite que las propiedades enlazables individuales de un formulario tengan este comportamiento especificado. cuando se establece este bit, se notificará a todos los cambios.

El nuevo bit ImmediateBind se asigna a los nuevos \_ bits VARFLAG FIMMEDIATEBIND (0x80) y FUNCFLAG \_ FIMMEDIATEBIND (0x80) en las enumeraciones VARFLAGS y FUNCFLAGS de la interfaz [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) , lo que permite inspeccionar los atributos de las propiedades.

 

 