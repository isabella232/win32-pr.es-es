---
title: Modelos de datos abstractos
description: Cada aplicación y cada sistema operativo tiene un modelo de datos abstracto.
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- abstract data models 64-bit Windows Programming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ad383e52c49997e43aa90301e7e417ef8cfeb089c9f6da151542b193b25071
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121865"
---
# <a name="abstract-data-models"></a>Modelos de datos abstractos

Cada aplicación y cada sistema operativo tiene un modelo de datos abstracto. Muchas aplicaciones no exponen explícitamente este modelo de datos, pero el modelo guía la forma en que se escribe el código de la aplicación. En el modelo de programación de 32 bits (conocido como modelo ILP32), los tipos de datos entero, largo y puntero tienen una longitud de 32 bits. La mayoría de los desarrolladores han usado este modelo sin darse cuenta. Para el historial de la API win32, esta ha sido una suposición válida (aunque no necesariamente segura) que se debe realizar.

En Windows de 64 bits, esta suposición de paridad en tamaños de tipo de datos no es válida. Si todos los tipos de datos tienen una longitud de 64 bits, se desperdiciará espacio, ya que la mayoría de las aplicaciones no necesitan el mayor tamaño. Sin embargo, las aplicaciones necesitan punteros a datos de 64 bits y necesitan la capacidad de tener tipos de datos de 64 bits en casos seleccionados. Estas consideraciones llevaron a la selección de un modelo de datos abstracto denominado LLP64 (o P64). En el modelo de datos LLP64, solo los punteros se expanden a 64 bits; todos los demás tipos de datos básicos (entero y largo) tienen una longitud de 32 bits.

Inicialmente, la mayoría de las aplicaciones que se ejecutan en Windows de 64 bits se habrán portado desde Windows de 32 bits. Es un objetivo que el mismo origen, escrito cuidadosamente, se ejecute tanto en archivos de 32 como en de 64 Windows. La definición del modelo de datos no facilita esta tarea. Sin embargo, asegurarse de que el modelo de datos solo afecta a los tipos de datos de puntero es el primer paso. El segundo paso consiste en definir un conjunto de nuevos tipos de datos que permiten a los desarrolladores ajustar automáticamente el tamaño de sus datos relacionados con el puntero. Esto permite que los datos asociados a punteros cambien de tamaño a medida que el tamaño del puntero cambia de 32 bits a 64 bits. Los tipos de datos básicos tienen una longitud de 32 bits, por lo que no hay ningún cambio en el tamaño de los datos del disco, los datos compartidos a través de una red o los datos compartidos a través de archivos asignados a memoria. Esto libera a los desarrolladores de gran parte del esfuerzo implicado en la porción de código de 32 bits a código de 64 Windows.

Estos nuevos tipos de datos se han agregado a los archivos de encabezado Windows API. Por lo tanto, ahora puede empezar a usar los nuevos tipos. Para obtener más información, vea [Los nuevos tipos de datos](the-new-data-types.md).

 

 




