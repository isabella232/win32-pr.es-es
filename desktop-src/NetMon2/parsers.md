---
description: Un analizador es el Monitor de red que inspecciona los datos en una captura retrasada y pasa información de protocolo específica a la aplicación que llama al analizador. Un analizador es pasivo porque solo funciona cuando Monitor de red o un experto lo llaman.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074106"
---
# <a name="parser"></a>Analizador

Un analizador es el Monitor de red que inspecciona los datos en una captura retrasada y pasa información de protocolo específica [*a*](d.md)la aplicación que llama al analizador. Un analizador es pasivo porque solo funciona cuando Monitor de red o un [*experto*](e.md) lo llaman.

Cada analizador identifica un protocolo y, normalmente, se implementa un analizador dentro de su propio archivo DLL de analizador. Sin embargo, un archivo DLL de analizador puede contener varios analizadores, lo que significa que se puede usar un archivo DLL para detectar más de un protocolo.

Los datos pasados a un analizador [](d.md)se toman de una captura retrasada y se pasan al analizador en función del marco. No se puede analizar una captura en tiempo real.

Para analizar los datos de un marco, el analizador debe reconocer la instancia de protocolo, identificar las propiedades que existen en la instancia de protocolo y adjuntar una definición de propiedad a cada propiedad. Tenga en cuenta que el marco contiene solo un flujo de datos. El marco no contiene datos que indiquen qué protocolos o propiedades de protocolo representan los datos.

En la ilustración siguiente se muestra un marco que contiene una instancia de un protocolo.

![un marco que contiene una instancia de protocolo](images/parser1.png)

Si Monitor de red va a mostrar datos analizados en la interfaz de usuario, el analizador debe dar formato a los datos. Sin embargo, algunos expertos usan la salida del analizador mediante programación y no muestran la salida en la interfaz Monitor de red usuario. Los datos mostrados incluyen los datos definidos por el analizador y los datos de la captura. Por ejemplo, el analizador normalmente proporciona un nombre para una propiedad que se muestra y los datos de la captura asociados a la propiedad .



| Para información acerca de                                         | Vea                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| Qué puntos de entrada se deben implementar dentro del archivo DLL del analizador. | [Arquitectura dll del analizador](parser-dll-architecture.md)                 |
| Cómo implementar funciones de exportación de DLL del analizador.                 | [Escribir un analizador de protocolos](writing-a-protocol-parser.md)             |
| Qué funciones y estructuras usan los analizadores.                   | [Funciones y estructuras del analizador](parser-functions-and-structures.md) |



 

 

 



