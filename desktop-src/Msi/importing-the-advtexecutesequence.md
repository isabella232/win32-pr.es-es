---
description: La tabla AdvtExecuteSequence enumera las acciones a las que llama el instalador cuando ejecuta la acción ADVERTISE de nivel superior. Vea Grupo de tablas de procedimientos de instalación, Uso de una tabla de secuencia y Ejemplo detallado de tabla de secuencia.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importación de AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074432"
---
# <a name="importing-the-advtexecutesequence"></a>Importación de AdvtExecuteSequence

La [tabla AdvtExecuteSequence](advtexecutesequence-table.md) enumera las acciones a las que llama el instalador cuando ejecuta la acción [ADVERTISE de nivel superior.](advertise-action.md) Vea [Grupo de tablas de procedimientos de](installation-procedure-tables-group.md)instalación , Uso de una tabla de [secuencia](using-a-sequence-table.md)y Ejemplo detallado de tabla [de secuencias](sequence-table-detailed-example.md).

Si en [](importing-a-blank-database.md) la sección Importación de una base de datos en blanco usó uisample.msi desde el SDK del instalador de Windows, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acciones sugeridas descritas en Uso de una tabla de [secuencias](using-a-sequence-table.md). No es necesario realizar ningún cambio en estas secuencias para crear el Bloc de notas de instalación de ejemplo.

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).

[Tabla AdvtExecuteSequence](advtexecutesequence-table.md)



| Acción                | Condición | Secuencia |
|-----------------------|-----------|----------|
| CostFinalize          |           | 1000     |
| CostInitialize        |           | 800      |
| CreateShortcuts       |           | 4500     |
| InstallFinalize       |           | 6600     |
| InstallInitialize     |           | 1.500     |
| InstallValidate       |           | 1400     |
| PublishComponents     |           | 6200     |
| PublishFeatures       |           | 6300     |
| PublishProduct        |           | 6400     |
| RegisterClassInfo     |           | 4600     |
| RegisterExtensionInfo |           | 4700     |
| RegisterMIMEInfo      |           | 4900     |
| RegisterProgIdInfo    |           | 4800     |



 

El instalador no usa la tabla [AdvtUISequence.](advtuisequence-table.md) Esta tabla no debe existir o dejarse vacía en la base de datos de instalación.

[Continuar](adding-summary-information.md)

 

 



