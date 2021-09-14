---
description: En la tabla AdminExecuteSequence se enumeran las acciones que el instalador ejecuta cuando llama a la acción admin de nivel superior. Vea Grupo de tablas de procedimientos de instalación, Uso de una tabla de secuencia y Ejemplo detallado de tabla de secuencia.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importación de AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074438"
---
# <a name="importing-the-adminexecutesequence"></a>Importación de AdminExecuteSequence

En [la tabla AdminExecuteSequence](adminexecutesequence-table.md) se enumeran las acciones que el instalador ejecuta cuando llama a la acción [admin de nivel superior.](admin-action.md) Vea [Grupo de tablas de procedimientos de](installation-procedure-tables-group.md)instalación , Uso de una tabla de [secuencia](using-a-sequence-table.md)y Ejemplo detallado de tabla [de secuencias](sequence-table-detailed-example.md).

Si en [](importing-a-blank-database.md) la sección Importación de una base de datos en blanco usó uisample.msi desde el SDK del instalador de Windows, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acciones sugeridas descritas en Uso de una tabla de [secuencia.](using-a-sequence-table.md) No es necesario realizar ningún cambio en estas secuencias para crear el Bloc de notas de instalación de ejemplo.

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla AdminExecuteSequence.

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

 

 



