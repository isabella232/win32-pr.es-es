---
title: Guardar y restaurar conjuntos de variables de estado
description: Puede guardar y restaurar los valores de una colección de variables de estado en una pila de atributos con las funciones glPushAttrib y glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variables de estado de OpenGL
- guardar las variables de estado OpenGL
- restaurar variables de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665687"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a>Guardar y restaurar conjuntos de variables de estado

Puede guardar y restaurar los valores de una colección de variables de estado en una pila de atributos con las funciones [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) . La pila de atributo tiene una profundidad de 16 como mínimo. Para obtener la profundidad real, use la \_ profundidad máxima de la \_ \_ pila Max de GL \_ con [**glGetIntegerv**](glgetintegerv.md). Si se inserta una pila completa o se extrae una vacía, se genera un error.

Por lo general, es más rápido usar **glPushAttrib** y **glPopAttrib** que para obtener y restaurar los valores. Algunos valores se pueden insertar y extraer en el hardware, y guardarlos y restaurarlos puede consumir muchos recursos. Además, si está trabajando en un cliente remoto, todos los datos de atributo se deben transferir a través de la conexión de red y de nuevo a medida que se guardan y restauran. Sin embargo, la implementación de OpenGL mantiene la pila de atributo en el servidor, evitando los retrasos de red innecesarios.

El prototipo de **glPushAttrib** es:

**void** **glPushAttrib**(**GLbitfield** *Mask* );

Al usar [**glPushAttrib**](glpushattrib.md) , se guardan todos los atributos indicados por bits en *Mask* y se insertan en la pila de atributos. Para obtener una lista de los posibles bits de máscara que puede realizar de forma lógica o conjunta para guardar cualquier combinación de atributos, consulte [grupos de atributos](attribute-groups.md). Cada bit corresponde a una colección de variables de estado individuales. Por ejemplo, el \_ bit de iluminación de GL \_ se refiere a todas las variables de estado relacionadas con la iluminación, que incluyen el color del material actual, el ambiente, la luz difusa, el reflejo y la luz emitida; una lista de las luces que están habilitadas y las direcciones de los focos. Cuando se llama a [**glPopAttrib**](glpopattrib.md), se restauran todas las variables. Para averiguar exactamente qué atributos se guardan para los valores de máscara concretos, consulte [variables de estado de OpenGL](opengl-state-variables.md).

 

 




