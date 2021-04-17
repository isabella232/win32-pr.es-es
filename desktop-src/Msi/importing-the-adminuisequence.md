---
description: En la tabla AdminUISequence se enumeran las acciones que el instalador llama cuando ejecuta la acción de administrador de nivel superior y el nivel de interfaz de usuario interna se establece en interfaz de usuario completa o en interfaz de usuario reducida.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importación de AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652855"
---
# <a name="importing-the-adminuisequence"></a>Importación de AdminUISequence

En la [tabla AdminUISequence](adminuisequence-table.md) se enumeran las acciones que el instalador llama cuando ejecuta la [acción de administrador](admin-action.md) de nivel superior y el nivel de interfaz de usuario interna se establece en interfaz de usuario completa o en interfaz de usuario reducida. El instalador omite las acciones de esta tabla si el nivel de la interfaz de usuario se establece en la interfaz de usuario básica o en ninguna interfaz de usuario. Vea [los niveles](user-interface-levels.md)de interfaz [de usuario y](user-interface.md) interfaz de usuario. Vea [grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md), [uso de una tabla de secuencia](using-a-sequence-table.md)y el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.

Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acción sugeridas que se describen en [uso de una tabla de secuencia](using-a-sequence-table.md). No es necesario realizar ningún cambio en estas secuencias para instalar el ejemplo de Bloc de notas.

Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla AdminExecuteSequence.

[Tabla AdminUISequence](adminuisequence-table.md)



| Acción          | Condición | Secuencia |
|-----------------|-----------|----------|
| AdminWelcomeDlg |           | 1230     |
| CostFinalize    |           | 1000     |
| CostInitialize  |           | 800      |
| ExecuteAction   |           | 1300     |
| ExitDlg         |           | -1       |
| FatalErrorDlg   |           | -3       |
| FileCost        |           | 900      |
| PrepareDlg      |           | 140      |
| ProgressDlg     |           | 1280     |
| UserExitDlg     |           | -2       |



 

[Continuar](importing-the-advtexecutesequence.md)

 

 



