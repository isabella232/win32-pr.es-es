---
description: Un analizador es el Monitor de red componente que inspecciona los datos en una captura diferida y pasa información de protocolo específica a la aplicación que llama al analizador. Un analizador es pasivo porque solo funciona cuando Monitor de red o un experto lo llama.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907661"
---
# <a name="parser"></a>Analizador

Un analizador es el Monitor de red componente que inspecciona los datos en una [*captura diferida*](d.md)y pasa información de protocolo específica a la aplicación que llama al analizador. Un analizador es pasivo porque solo funciona cuando Monitor de red o un [*experto*](e.md) lo llama.

Cada analizador identifica un protocolo y, normalmente, se implementa un analizador dentro de su propio archivo DLL de analizador. Sin embargo, un archivo DLL de analizador puede contener varios analizadores, lo que significa que se puede usar una DLL para detectar más de un protocolo.

Los datos que se pasan a un analizador se toman de una [*captura diferida*](d.md)y se pasan al analizador fotograma a fotograma. No se puede analizar una captura en tiempo real.

Para analizar los datos de un marco, el analizador debe reconocer la instancia del Protocolo, identificar las propiedades que existen en la instancia del protocolo y adjuntar una definición de propiedad a cada propiedad. Tenga en cuenta que el marco solo contiene un flujo de datos. El marco no contiene datos que indiquen qué protocolos o propiedades de protocolo representan los datos.

En la ilustración siguiente se muestra un marco que contiene una instancia de un protocolo.

![marco que contiene una instancia de protocolo](images/parser1.png)

Si Monitor de red va a mostrar los datos analizados en la interfaz de usuario, el analizador debe dar formato a los datos. Sin embargo, algunos expertos usan el resultado del analizador mediante programación y no muestran el resultado en la interfaz de usuario de Monitor de red. Los datos mostrados incluyen tanto los datos definidos por el analizador como los datos de la captura. Por ejemplo, el analizador suele proporcionar un nombre para una propiedad que se muestra, y los datos de la captura que están asociados a la propiedad.



| Para información acerca de                                         | Vea                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| Qué puntos de entrada se deben implementar en el archivo DLL del analizador. | [Arquitectura de DLL de analizador](parser-dll-architecture.md)                 |
| Cómo implementar funciones de exportación de DLL de analizador.                 | [Escritura de un analizador de protocolos](writing-a-protocol-parser.md)             |
| Qué funciones y estructuras usan los analizadores.                   | [Funciones y estructuras del analizador](parser-functions-and-structures.md) |



 

 

 



