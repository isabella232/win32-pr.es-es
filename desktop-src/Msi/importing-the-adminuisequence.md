---
description: En la tabla AdminUISequence se enumeran las acciones a las que llama el instalador cuando ejecuta la acción admin de nivel superior y el nivel de interfaz de usuario interno se establece en interfaz de usuario completa o interfaz de usuario reducida.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importación de AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074434"
---
# <a name="importing-the-adminuisequence"></a>Importación de AdminUISequence

En la [tabla AdminUISequence](adminuisequence-table.md) se enumeran las acciones a las que llama el instalador cuando ejecuta la acción [admin](admin-action.md) de nivel superior y el nivel de interfaz de usuario interno se establece en interfaz de usuario completa o interfaz de usuario reducida. El instalador omite las acciones de esta tabla si el nivel de interfaz de usuario está establecido en interfaz de usuario básica o sin interfaz de usuario. Vea [Interfaz de usuario](user-interface.md) y [Interfaz de usuario niveles](user-interface-levels.md). Vea [Grupo de tablas de procedimientos de](installation-procedure-tables-group.md)instalación , Uso de una tabla de [secuencia](using-a-sequence-table.md)y Ejemplo detallado de tabla [de secuencia.](sequence-table-detailed-example.md)

Si en [](importing-a-blank-database.md) la sección Importación de una base de datos en blanco usó uisample.msi desde el SDK del instalador de Windows, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acciones sugeridas descritas en Uso de una tabla de [secuencia](using-a-sequence-table.md). No es necesario realizar ningún cambio en estas secuencias para instalar el Bloc de notas ejemplo.

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla AdminExecuteSequence.

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

 

 



