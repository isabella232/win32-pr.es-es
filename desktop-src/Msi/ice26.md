---
description: ICE26 valida las tablas de secuencia en una base Windows installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074637"
---
# <a name="ice26"></a>ICE26

ICE26 valida que cada [](s-gly.md) una de las siguientes tablas de secuencia contiene las acciones que requiere la tabla y no contiene ninguna acción no permitido en la tabla:

-   [Tabla AdminUISequence](adminuisequence-table.md)
-   [Tabla AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabla InstallUISequence](installuisequence-table.md)
-   [Tabla InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Resultado

ICE26 envía un mensaje de error si el paquete de instalación tiene una tabla de secuencia que carece de una acción necesaria o que contiene una acción que no está permitido para la tabla.

## <a name="example"></a>Ejemplo



| Error ice26                                                                   | Descripción                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acción: se requiere "Action1" en la tabla InstallExecuteSequence Sequence.   | Falta una acción necesaria en la tabla de secuencia indicada. Vea las template.msi o las tablas de secuencia sugeridas en [Using a Sequence Table](using-a-sequence-table.md). |
| Acción: "Action2" está prohibido en la tabla InstallExecuteSequence Sequence. | Esta acción no puede estar en la tabla de secuencia indicada. Quite esta acción de la tabla de secuencia.                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



