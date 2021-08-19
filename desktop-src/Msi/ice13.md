---
description: ICE13 valida que los cuadros de diálogo de las tablas de secuencia aparezcan en las tablas AdminUISequence o InstallUISequence. Los diálogos no deben aparecer en las tablas InstallExecuteSequence, AdminExecuteSequence o AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc11f8254c721d404a65e63fc897aa6e55bc61364c768b48f2d5aded4348d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946639"
---
# <a name="ice13"></a>ICE13

ICE13 valida que los cuadros de diálogo de las tablas de secuencia aparezcan en las tablas [AdminUISequence](adminuisequence-table.md)o [InstallUISequence.](installuisequence-table.md) Los diálogos no deben aparecer en las tablas [InstallExecuteSequence,](installexecutesequence-table.md) [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence.](advtexecutesequence-table.md)

## <a name="result"></a>Resultado

ICE13 publica un mensaje de error si aparece un cuadro de diálogo en una tabla de secuencia de ejecución.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, ICE13 publica un mensaje de error que indica que "WelcomeDialog" no se puede enumerar en la tabla "InstallExecuteSequence".

[InstallExecuteSequence Table](installexecutesequence-table.md) (parcial)



| Acción          |
|-----------------|
| InstallFinalize |
| CostFinalize    |
| WelcomeDialog   |



 

[Tabla InstallUISequence](installuisequence-table.md) (parcial)



| Acción         |
|----------------|
| CostFinalize   |
| CostInitialize |
| BrowseDialog   |



 

[Tabla de diálogos](dialog-table.md) (parcial)



| Diálogo        |
|---------------|
| BrowseDialog  |
| WelcomeDialog |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



