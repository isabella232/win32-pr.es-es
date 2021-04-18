---
title: Modelos de datos abstractos
description: Cada aplicación y cada sistema operativo tiene un modelo de datos abstracto.
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- modelos de datos abstractos de la programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bfb116d5afccba1b1ce3438f8b7135d01bc1b7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704715"
---
# <a name="abstract-data-models"></a>Modelos de datos abstractos

Cada aplicación y cada sistema operativo tiene un modelo de datos abstracto. Muchas aplicaciones no exponen explícitamente este modelo de datos, pero el modelo guía el modo en que se escribe el código de la aplicación. En el modelo de programación de 32 bits (conocido como modelo ILP32), los tipos de datos Integer, Long y Pointer tienen una longitud de 32 bits. La mayoría de los desarrolladores han usado este modelo sin darse cuenta. Para el historial de la API de Win32, se trata de una suposición válida (aunque no necesariamente segura).

En 64-bitWindows, esta suposición de la paridad en tamaños de tipo de datos no es válida. Hacer que todos los tipos de datos 64 bits de longitud pierda espacio, ya que la mayoría de las aplicaciones no necesitan el mayor tamaño. Sin embargo, las aplicaciones necesitan punteros a datos de 64 bits y necesitan la capacidad de tener tipos de datos de 64 bits en casos seleccionados. Estas consideraciones se llevaron a la selección de un modelo de datos abstracto denominado LLP64 (o P64). En el modelo de datos LLP64, solo los punteros se expanden hasta 64 bits; todos los demás tipos de datos básicos (entero y largo) siguen siendo 32 bits de longitud.

Inicialmente, la mayoría de las aplicaciones que se ejecutan en Windows de 64 bits se transportan desde Windows de 32 bits. Es un objetivo que el mismo origen, escrito cuidadosamente, se debe ejecutar en Windows de 32 y 64 bits. La definición del modelo de datos no facilita esta tarea. Sin embargo, asegurarse de que el modelo de datos solo afecta a los tipos de datos de puntero es el primer paso. El segundo paso es definir un conjunto de nuevos tipos de datos que permiten a los desarrolladores ajustar automáticamente el tamaño de los datos relacionados con los punteros. Esto permite que los datos asociados a punteros cambien de tamaño a medida que cambia el tamaño del puntero de 32 bits a 64 bits. Los tipos de datos básicos siguen siendo 32 bits de longitud, por lo que no hay ningún cambio en el tamaño de los datos del disco, los datos compartidos a través de una red o los datos compartidos mediante archivos asignados a memoria. Esto libera a los desarrolladores de gran parte del esfuerzo que supone trasladar el código de 32 bits a Windows de 64 bits.

Estos nuevos tipos de datos se han agregado a los archivos de encabezado de la API de Windows. Por lo tanto, puede empezar a usar los nuevos tipos ahora. Para obtener más información, vea [los nuevos tipos de datos](the-new-data-types.md).

 

 




