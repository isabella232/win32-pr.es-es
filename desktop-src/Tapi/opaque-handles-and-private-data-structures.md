---
description: Los identificadores opacos se usan en TSPI para hacer referencia a las estructuras de datos que representan líneas, teléfonos y apariencias de llamadas.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Manipuladores opacos y estructuras de datos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa8d7cb4e4a3bd6e8e6cb4b12c3d74dbd712757640d215a231a939568cfe1d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118862730"
---
# <a name="opaque-handles-and-private-data-structures"></a>Manipuladores opacos y estructuras de datos privados

Los identificadores opacos se usan en TSPI para hacer referencia a las estructuras de datos que representan líneas, teléfonos y apariencias de llamadas. Estos aparecen como parámetros para la mayoría de las funciones y devoluciones de llamada. Hay algunas funciones que hacen referencia al dispositivo mediante un identificador de dispositivo en lugar de un identificador opaco. En tal caso, la referencia es al propio dispositivo en lugar de a una estructura de datos. Las funciones que funcionan de este modo suelen ser las llamadas en los primeros momentos de inicialización antes de crear estructuras de datos y se intercambian identificadores opacos.

El proveedor de servicios debe decidir cómo interpretar estos identificadores. Normalmente, un proveedor de servicios usa el puntero a su estructura de datos o al índice en una matriz de estructuras de datos como su identificador opaco. La única restricción es que el proveedor de servicios no puede usar el valor 0 como [HDRVLINE,](hdrvline.md)HDRVCALL o [HDRVPHONE](hdrvphone.md). El valor 0 o **NULL para** un identificador tiene un significado especial en algunas operaciones.

 

 



