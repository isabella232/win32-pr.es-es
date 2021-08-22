---
description: ICE26 valida las tablas de secuencia en una base de Windows installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf63e0efeec79de35122f7a210c32746af9de50f27ac3e47ad1f88984a6ec77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528865"
---
# <a name="ice26"></a>ICE26

ICE26 valida que cada [](s-gly.md) una de las siguientes tablas de secuencia contiene las acciones que requiere la tabla y no contiene ninguna acción no permitido en la tabla:

-   [Tabla AdminUISequence](adminuisequence-table.md)
-   [Tabla AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabla InstallUISequence](installuisequence-table.md)
-   [Tabla InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Resultado

ICE26 publica un mensaje de error si el paquete de instalación tiene una tabla de secuencias que carece de una acción necesaria o que contiene una acción que no se puede realizar para la tabla.

## <a name="example"></a>Ejemplo



| Error de ICE26                                                                   | Descripción                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acción: se requiere "Action1" en la tabla InstallExecuteSequence Sequence.   | Falta una acción necesaria en la tabla de secuencia indicada. Vea las template.msi o las tablas de secuencia sugeridas en [Uso de una tabla de secuencia](using-a-sequence-table.md). |
| Acción: "Action2" está prohibido en la tabla InstallExecuteSequence Sequence. | Esta acción no puede estar en la tabla de secuencia indicada. Quite esta acción de la tabla de secuencia.                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



