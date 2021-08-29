---
description: Varias de las funciones del proveedor de red toman la dirección y el tamaño de un búfer en el que la función coloca una estructura de datos de tamaño variable.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Control de datos almacenados en búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01cac833b0c7b76bf09a6735d719a001c8393383f1dd031ff741900a1c9dcf2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623105"
---
# <a name="handling-buffered-data"></a>Control de datos almacenados en búfer

Varias de las funciones del proveedor de red toman la dirección y el tamaño de un búfer en el que la función coloca una estructura de datos de tamaño variable.

En cada caso, el mecanismo utilizado es el mismo. El autor de la llamada asigna un búfer y pasa su dirección a la función . También pasa la dirección de un **DWORD** que especifica el tamaño del búfer, en bytes.

A continuación, la función copia tanto como sea posible en el búfer de la estructura de datos solicitada. Si todos los datos caben en el búfer, la función devuelve WN \_ SUCCESS. Si los datos no caben en el búfer, los datos pueden quedar incompletos y la función establece el \_ error WN MORE \_ DATA. En cualquier caso, **DWORD** que indica el tamaño del búfer se establece en el número de bytes realmente requeridos por la estructura de datos. De este modo, si el búfer pasado era demasiado pequeño y la función no se pudo realizar, el autor de la llamada puede asignar un nuevo búfer del tamaño necesario y volver a llamar a la función.

Cuando las estructuras de datos devueltas incluyen cadenas de longitud variable, las estructuras de datos individuales normalmente contienen punteros a estas cadenas. Las propias cadenas también deben colocarse dentro del búfer. Sin embargo, es importante colocarlos al final del búfer. De lo contrario, harán imposible la indexación a la enésima estructura. En otras palabras, todas las estructuras se encuentran de forma contigua al principio del búfer. Los punteros a cadenas o datos de longitud variable deben ser punteros reales, no desplazamientos en el búfer.

Cuando se usa un búfer para pasar y devolver datos que constan solo de cadenas, el **DWORD** que especifica el tamaño del búfer debe establecerse en el número total de caracteres que caben en estas cadenas, no en el número de bytes.

 

 



