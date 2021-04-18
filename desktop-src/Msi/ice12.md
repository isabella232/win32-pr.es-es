---
description: ICE12 valida las tablas CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence y InstallUISequence de la base de datos Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667769"
---
# <a name="ice12"></a>ICE12

ICE12 consulta las tablas [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)y [InstallUISequence](installuisequence-table.md) para validar lo siguiente:

-   Que la [acción CostFinalize](costfinalize-action.md) se produce en cualquier tabla de secuencia que contenga acciones del tipo de [acción personalizada Type 35](custom-action-type-35.md) o el [tipo de acción personalizada 51](custom-action-type-51.md).
-   Que cada [tipo de acción personalizada 35](custom-action-type-35.md) venga después de la [acción CostFinalize](costfinalize-action.md). en las tablas de secuencia.
-   Que cada [acción personalizada tipo 51](custom-action-type-51.md) que tiene una clave externa en la tabla de directorio de la columna de origen de la tabla CustomAction viene antes de la [acción CostFinalize](costfinalize-action.md) en las tablas de secuencia.

Tenga en cuenta que ICE12 no valida el texto con formato de la columna de destino de la tabla CustomAction.

## <a name="result"></a>Resultado

ICE12 envía un mensaje de error si se produce un error en la validación de las acciones personalizadas que establecen una propiedad de directorio.

## <a name="example"></a>Ejemplo

ICE12 publicaría tres errores para el ejemplo mostrado.

-   En el caso de CA1, no se encontró la carpeta ' carpeta ' en la tabla de directorios
-   En el caso de CA2, la secuencia ' 80 ' viene antes de CostFinalize en la tabla InstallExecuteSequence. Debe aparecer después de ( CF@100 )
-   En el caso de CA3, la secuencia ' 125 ' se incluye después de CostFinalize en la tabla InstallExecuteSequence. Debe ser anterior a ( CF@100 )

[Tabla CustomAction](customaction-table.md) (parcial)



| Acción | Tipo | Source        |
|--------|------|---------------|
| CA1    | 35   | MyFolder      |
| CA2    | 35   | WindowsFolder |
| CA3    | 51   | WindowsFolder |



 

[Tabla de directorio](directory-table.md)



| Directorio     | Directorio \_ primario | DefaultDir    |
|---------------|-------------------|---------------|
| TARGETDIR     |                   | SourceDir     |
| WindowsFolder | TARGETDIR         | WindowsFolder |



 

[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Acción       | Secuencia |
|--------------|----------|
| CostFinalize | 100      |
| CA2          | 80       |
| CA3          | 125      |



 

Para corregir el error de CA1, cambie su entrada en la columna de origen de la tabla CustomAction a una entrada existente en la tabla del directorio o agregue mi carpeta a la tabla del directorio.

Para corregir el error de CA2, cambie su secuencia en la tabla InstallExecuteSequence de forma que venga después de la acción CostFinalize.

Para corregir el error de CA3, cambie su secuencia en la tabla InstallExecuteSequence de forma que venga antes de la acción CostFinalize.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



