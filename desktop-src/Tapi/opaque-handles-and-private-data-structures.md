---
description: Los identificadores opacos se usan en TSPI para hacer referencia a las estructuras de datos que representan las líneas, los teléfonos y los aspectos de la llamada.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Controladores opacos y estructuras de datos privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001317"
---
# <a name="opaque-handles-and-private-data-structures"></a>Controladores opacos y estructuras de datos privadas

Los identificadores opacos se usan en TSPI para hacer referencia a las estructuras de datos que representan las líneas, los teléfonos y los aspectos de la llamada. Aparecen como parámetros de la mayoría de las funciones y devoluciones de llamada. Hay pocas funciones que hacen referencia al dispositivo con un identificador de dispositivo en lugar de un identificador opaco. En tal caso, la referencia es al propio dispositivo en lugar de a una estructura de datos. Las funciones que funcionan de esta manera son normalmente las llamadas a los tiempos de inicialización tempranas antes de que se creen las estructuras de datos y se intercambien los identificadores opacos.

El proveedor de servicios debe decidir cómo interpretar estos identificadores. Un proveedor de servicios suele usar el puntero a su estructura de datos o al índice en una matriz de estructuras de datos como su identificador opaco. La única restricción es que el proveedor de servicios no puede usar el valor 0 como [HDRVLINE](hdrvline.md), HDRVCALL o [HDRVPHONE](hdrvphone.md). El valor 0 o **null** para un identificador tiene un significado especial en algunas operaciones.

 

 



