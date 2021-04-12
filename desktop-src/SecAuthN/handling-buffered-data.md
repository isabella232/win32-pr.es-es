---
description: Varias de las funciones de proveedor de red toman la dirección y el tamaño de un búfer en el que la función coloca una estructura de datos de tamaño variable.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Controlar los datos almacenados en búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278141"
---
# <a name="handling-buffered-data"></a>Controlar los datos almacenados en búfer

Varias de las funciones de proveedor de red toman la dirección y el tamaño de un búfer en el que la función coloca una estructura de datos de tamaño variable.

En cada caso, el mecanismo utilizado es el mismo. El autor de la llamada asigna un búfer y pasa su dirección a la función. También pasa la dirección de un **valor DWORD** que especifica el tamaño del búfer, en bytes.

A continuación, la función copia la gran parte de la estructura de datos solicitada tal y como se puede hacer en el búfer. Si todos los datos caben en el búfer, la función devuelve WN \_ Success. Si los datos no caben en el búfer, los datos se pueden dejar incompletos y la función establece el \_ error de más datos de WN \_ . En cualquier caso, el **valor DWORD** que indica el tamaño del búfer se establece en el número de bytes realmente requerido por la estructura de datos. De este modo, si el búfer pasado es demasiado pequeño y se produjo un error en la función, el llamador puede asignar un nuevo búfer del tamaño requerido y volver a llamar a la función.

Cuando las estructuras de datos devueltas incluyen cadenas de longitud variable, las estructuras de datos individuales normalmente contienen punteros a estas cadenas. Las propias cadenas también se deben colocar en el búfer. Sin embargo, es importante colocarlos al final del búfer. De lo contrario, hará que la indización en la estructura nth sea imposible. En otras palabras, todas las estructuras se colocan de forma contigua al principio del búfer. Los punteros a cadenas o datos de longitud variable deben ser punteros reales, no desplazamientos en el búfer.

Cuando se usa un búfer para pasar y devolver datos que solo se componen de cadenas, el **valor DWORD** que especifica el tamaño del búfer se debe establecer en el número total de caracteres que quepan en estas cadenas, no en el número de bytes.

 

 



