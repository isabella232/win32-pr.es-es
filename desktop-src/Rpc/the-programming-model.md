---
title: Modelo de programación
description: En los primeros días de la programación informática, cada programa se escribió como un fragmento monolítico grande, relleno de instrucciones goto.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852dfa1dfa007ad28a23679a49f7cf4df15995fded3f222df5cc7fb8f5ad3bfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016845"
---
# <a name="the-programming-model"></a>Modelo de programación

En los primeros días de la programación informática, cada programa se escribió como un fragmento monolítico grande, relleno de **instrucciones goto.** Cada programa tenía que administrar su propia entrada y salida en distintos dispositivos de hardware. A medida que la materia de programación ha madurado, este código monolítico se organizaba en procedimientos, con los procedimientos más usados empaquetados en bibliotecas para su uso compartido y reutilización.

![instrucciones goto monolíticas frente a procedimientos empaquetados en bibliotecas compartidas](images/prog-a06.png)

El lenguaje de programación C admite la programación orientada a procedimientos. En C, el procedimiento principal se relaciona con todos los demás procedimientos como cuadros negros. Por ejemplo, el procedimiento principal no puede averiguar cómo hacen su trabajo los procedimientos A, B y X. El procedimiento principal solo llama a otro procedimiento; no tiene información sobre cómo se implementa ese procedimiento.

![aislamiento de actividades realizadas en procedimientos externos](images/prog-a08.png)

Los lenguajes de programación orientados a procedimientos proporcionan mecanismos sencillos para especificar y escribir procedimientos. Por ejemplo, el prototipo de función de C estándar ANSI es una construcción que se usa para especificar el nombre de un procedimiento, el tipo del resultado que devuelve (si existe) y el número, la secuencia y el tipo de sus parámetros. El uso del prototipo de función es una manera formal de especificar una interfaz entre procedimientos.

Rpc de Microsoft se basa en ese modelo de programación al permitir que los procedimientos, agrupados en interfaces, residan en procesos diferentes a los del autor de la llamada. Rpc de Microsoft también agrega un enfoque más formal a la definición de procedimiento que permite que el autor de la llamada y la rutina llamada adopten un contrato para intercambiar datos de forma remota e invocar la funcionalidad. En el modelo de programación RPC de Microsoft, las llamadas a funciones tradicionales se complementan con dos elementos adicionales.

-   El primer elemento es un archivo .idl/.acf que describe con precisión el intercambio de datos y el mecanismo de paso de parámetros entre el llamador y el procedimiento llamado.
-   El segundo elemento es un conjunto de API en tiempo de ejecución que proporcionan a los desarrolladores un control granular de la llamada a procedimiento remoto, incluidos los aspectos de seguridad, la administración del estado en el servidor, la especificación de qué clientes pueden hablar con el servidor, y así sucesivamente.

 

 




