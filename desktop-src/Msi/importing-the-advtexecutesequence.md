---
description: En la tabla AdvtExecuteSequence se enumeran las acciones que llama el instalador cuando ejecuta la acción ANUNCIAnte de nivel superior. Vea Grupo de tablas de procedimientos de instalación, uso de una tabla de secuencia y el ejemplo detallado de la tabla de secuencia.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importación de AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815446"
---
# <a name="importing-the-advtexecutesequence"></a>Importación de AdvtExecuteSequence

En la [tabla AdvtExecuteSequence](advtexecutesequence-table.md) se enumeran las acciones que llama el instalador cuando ejecuta la [acción anunciante](advertise-action.md)de nivel superior. Vea [grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md), [uso de una tabla de secuencia](using-a-sequence-table.md)y el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.

Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acción sugeridas que se describen en [uso de una tabla de secuencia](using-a-sequence-table.md). No es necesario realizar ningún cambio en estas secuencias para crear el paquete de instalación del ejemplo del Bloc de notas.

Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).

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



 

El instalador no utiliza la [tabla AdvtUISequence](advtuisequence-table.md) . Esta tabla no debe existir o dejarse vacía en la base de datos de instalación.

[Continuar](adding-summary-information.md)

 

 



