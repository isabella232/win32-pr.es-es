---
description: En la tabla AdminExecuteSequence se enumeran las acciones que ejecuta el instalador cuando llama a la acción de administrador de nivel superior. Vea Grupo de tablas de procedimientos de instalación, uso de una tabla de secuencia y el ejemplo detallado de la tabla de secuencia.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importación de AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810736"
---
# <a name="importing-the-adminexecutesequence"></a>Importación de AdminExecuteSequence

En la [tabla AdminExecuteSequence](adminexecutesequence-table.md) se enumeran las acciones que ejecuta el instalador cuando llama a la [acción de administrador](admin-action.md)de nivel superior. Vea [grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md), [uso de una tabla de secuencia](using-a-sequence-table.md)y el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.

Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acción sugeridas que se describen en [uso de una tabla de secuencia](using-a-sequence-table.md). No es necesario realizar ningún cambio en estas secuencias para crear el paquete de instalación del ejemplo del Bloc de notas.

Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla AdminExecuteSequence.

[Tabla AdminExecuteSequence](adminexecutesequence-table.md)



| Acción              | Condición | Secuencia |
|---------------------|-----------|----------|
| CostFinalize        |           | 1000     |
| CostInitialize      |           | 800      |
| FileCost            |           | 900      |
| InstallAdminPackage |           | 3900     |
| InstallFiles        |           | 4000     |
| InstallFinalize     |           | 6600     |
| InstallInitialize   |           | 1.500     |
| InstallValidate     |           | 1400     |



 

[Continuar](importing-the-adminuisequence.md)

 

 



