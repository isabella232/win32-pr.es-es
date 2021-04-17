---
description: 'La sintaxis del evento SetProperty es diferente de la de otros ControlEvents en lugar del nombre del evento que coloca la propiedad entre corchetes: nombre de \[ la \_ propiedad \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: SetProperty ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678146"
---
# <a name="setproperty-controlevent"></a>SetProperty ControlEvent,

La sintaxis del evento SetProperty es diferente de la de otros ControlEvents en lugar del nombre del evento que coloca la propiedad entre corchetes: nombre de \[ la \_ propiedad \] . El argumento es el nuevo valor de la propiedad. Para anular la propiedad, el argumento debe ser {} . Esto es necesario porque el argumento es una clave principal de la tabla y, por tanto, no puede ser null. Se dará formato al argumento mediante el método FormatText, por lo que el argumento puede contener cualquier expresión que pueda controlar el método FormatText. Los valores de propiedad se evalúan en el momento de ControlEvent,.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md), un [control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Nuevo valor de la propiedad. {} para null.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo vinculado a este evento para que cambie una propiedad cuando se inserte el botón.

 

 



