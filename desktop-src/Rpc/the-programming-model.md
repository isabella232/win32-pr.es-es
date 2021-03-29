---
title: Modelo de programación
description: En los primeros días de programación de equipos, cada programa se escribió como un fragmento monolítico grande, rellenado con instrucciones Goto.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776429"
---
# <a name="the-programming-model"></a>Modelo de programación

En los primeros días de programación de equipos, cada programa se escribió como un fragmento monolítico grande, rellenado con instrucciones **goto** . Cada programa tenía que administrar su propia entrada y salida en distintos dispositivos de hardware. A medida que la disciplina de programación ha evolucionado, este código monolítico se organizó en procedimientos, con los procedimientos más usados empaquetados en bibliotecas para compartir y reutilizar.

![instrucciones Goto monolíticas frente a procedimientos empaquetados en bibliotecas compartidas](images/prog-a06.png)

El lenguaje de programación C admite la programación orientada a procedimientos. En C, el procedimiento principal se relaciona con todos los demás procedimientos como cuadros negros. Por ejemplo, el procedimiento Main no puede averiguar cómo los procedimientos A, B y X realizan su trabajo. El procedimiento Main solo llama a otro procedimiento; no tiene información sobre cómo se implementa el procedimiento.

![aislamiento de actividades realizadas en procedimientos externos](images/prog-a08.png)

Los lenguajes de programación orientados a procedimientos proporcionan mecanismos sencillos para especificar y escribir procedimientos. Por ejemplo, el prototipo de función estándar de C de ANSI es una construcción que se usa para especificar el nombre de un procedimiento, el tipo del resultado que devuelve (si existe) y el número, la secuencia y el tipo de sus parámetros. El uso del prototipo de función es una manera formal de especificar una interfaz entre los procedimientos.

Microsoft RPC se basa en ese modelo de programación, ya que permite que los procedimientos, agrupados en interfaces, residan en procesos diferentes a los del llamador. Microsoft RPC también agrega un enfoque más formal a la definición de procedimiento que permite que el llamador y la rutina llamada adopten un contrato para intercambiar datos de forma remota e invocar la funcionalidad. En el modelo de programación RPC de Microsoft, las llamadas de función tradicionales se complementan con dos elementos adicionales.

-   El primer elemento es un archivo. idl/. ACF que describe con precisión el intercambio de datos y el mecanismo de paso de parámetros entre el llamador y el procedimiento llamado.
-   El segundo elemento es un conjunto de API en tiempo de ejecución que proporcionan a los desarrolladores un control granular de la llamada a procedimiento remoto, incluidos los aspectos de seguridad, la administración del estado en el servidor, la especificación de qué clientes pueden comunicarse con el servidor, etc.

 

 




