---
description: ICE13 valida que los cuadros de diálogo de las tablas de secuencia aparecen en las tablas AdminUISequence o InstallUISequence. Los cuadros de diálogo no deben aparecer en las tablas InstallExecuteSequence, AdminExecuteSequence o AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002254"
---
# <a name="ice13"></a>ICE13

ICE13 valida que los cuadros de diálogo de las tablas de secuencia aparecen en las tablas [AdminUISequence](adminuisequence-table.md)o [InstallUISequence](installuisequence-table.md) . Los cuadros de diálogo no deben aparecer en las tablas [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) .

## <a name="result"></a>Resultado

ICE13 envía un mensaje de error si aparece un cuadro de diálogo en una tabla de secuencia de ejecución.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, ICE13 envía un mensaje de error que indica que no se puede enumerar ' WelcomeDialog ' en la tabla ' InstallExecuteSequence '.

[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)



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



 

[Tabla de cuadro de diálogo](dialog-table.md) (parcial)



| Diálogo        |
|---------------|
| BrowseDialog  |
| WelcomeDialog |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



