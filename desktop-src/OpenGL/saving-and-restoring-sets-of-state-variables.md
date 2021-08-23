---
title: Guardar y restaurar conjuntos de variables de estado
description: Puede guardar y restaurar los valores de una colección de variables de estado en una pila de atributos con las funciones glPushAttrib y glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variables de estado OpenGL
- guardar variables de estado OpenGL
- restaurar variables de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197a05d80e72479aecdade3323899464bf0b1f4afa2d9f2a8a1a1add6e56db78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553815"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a>Guardar y restaurar conjuntos de variables de estado

Puede guardar y restaurar los valores de una colección de variables de estado en una pila de atributos con las funciones [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib.**](glpopattrib.md) La pila de atributos tiene una profundidad de al menos 16. Para obtener la profundidad real, use GL \_ MAX \_ ATTRIB \_ STACK DEPTH con \_ [**glGetIntegerv**](glgetintegerv.md). Insertar una pila completa o sacar una vacía genera un error.

Por lo general, es más rápido usar **glPushAttrib** y **glPopAttrib** que obtener y restaurar los valores usted mismo. Algunos valores se pueden insertar y sacar en el hardware, y guardarlos y restaurarlos puede hacer un uso intensivo de recursos. Además, si está trabajando en un cliente remoto, todos los datos de atributo se deben transferir a través de la conexión de red y volver a hacerlo a medida que se guardan y restauran. Sin embargo, la implementación de OpenGL mantiene la pila de atributos en el servidor, lo que evita retrasos de red innecesarios.

El prototipo **de glPushAttrib** es:

**void** **glPushAttrib**(**GLbitfield** *mask* );

El [**uso de glPushAttrib**](glpushattrib.md) guarda todos los atributos indicados por los bits en *máscara* al insertarlos en la pila de atributos. Para obtener una lista de los posibles bits de máscara que puede combinar de forma lógica o conjunta para guardar cualquier combinación de atributos, vea [Grupos de atributos](attribute-groups.md). Cada bit corresponde a una colección de variables de estado individuales. Por ejemplo, GL LIGHTING BIT hace referencia a todas las variables de estado relacionadas con la iluminación, que incluyen el color del material actual; la luz ambiente, difusa, especular y emitida; una lista de las luces habilitadas y las direcciones de los \_ \_ focos. Cuando se llama [**a glPopAttrib,**](glpopattrib.md)se restauran todas esas variables. Para averiguar exactamente qué atributos se guardan para valores de máscara determinados, vea [Variables de estado OpenGL](opengl-state-variables.md).

 

 




