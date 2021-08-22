---
description: ICE12 valida las tablas CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence e InstallUISequence de la base de datos Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef427ca1567680aa9a9f2a598f5a94cb8dee545487afcf3eb1fbb8d1f350fd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262265"
---
# <a name="ice12"></a>ICE12

ICE12 consulta las tablas [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence,](adminexecutesequence-table.md) [AdminUISequence,](adminuisequence-table.md) [AdvtExecuteSequence,](advtexecutesequence-table.md) [InstallExecuteSequence](installexecutesequence-table.md)e [InstallUISequence](installuisequence-table.md) para validar lo siguiente:

-   Que la [acción CostFinalize](costfinalize-action.md) se produce en cualquier tabla de secuencia que contenga acciones del tipo Tipo de acción [personalizada 35](custom-action-type-35.md) o Tipo de [acción personalizada 51.](custom-action-type-51.md)
-   Que cada [tipo de acción personalizada 35](custom-action-type-35.md) viene después de la acción [CostFinalize](costfinalize-action.md). en las tablas de secuencia.
-   Que cada tipo de acción personalizada [51](custom-action-type-51.md) que tenga una clave externa a la tabla Directory de la columna Origen de la tabla CustomAction se produce antes que la acción [CostFinalize](costfinalize-action.md) en las tablas de secuencia.

Tenga en cuenta que ICE12 no valida el texto con formato en la columna Destino de la tabla CustomAction.

## <a name="result"></a>Resultado

ICE12 envía un mensaje de error si se produce un error en la validación de las acciones personalizadas que establecen una propiedad de directorio.

## <a name="example"></a>Ejemplo

ICE12 publicaría tres errores para el ejemplo mostrado.

-   Para CA1, la carpeta "MyFolder" no se encuentra en la tabla Directory
-   Para CA2, la secuencia "80" aparece antes que CostFinalize en la tabla InstallExecuteSequence. Debe ir después de ( CF@100 )
-   Para CA3, la secuencia "125" viene después de CostFinalize en la tabla InstallExecuteSequence. Debe ir antes de ( CF@100 )

[Tabla CustomAction](customaction-table.md) (parcial)



| Acción | Tipo | Source        |
|--------|------|---------------|
| CA1    | 35   | MyFolder      |
| CA2    | 35   | WindowsFolder |
| CA3    | 51   | WindowsFolder |



 

[Tabla de directorios](directory-table.md)



| Directorio     | Elemento primario \_ del directorio | DefaultDir    |
|---------------|-------------------|---------------|
| TARGETDIR     |                   | SourceDir     |
| WindowsFolder | TARGETDIR         | WindowsFolder |



 

[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Acción       | Secuencia |
|--------------|----------|
| CostFinalize | 100      |
| CA2          | 80       |
| CA3          | 125      |



 

Para corregir el error de CA1, cambie su entrada en su columna Origen de la tabla CustomAction a una entrada existente en la tabla Directory o agregue MyFolder a la tabla Directory.

Para corregir el error de CA2, cambie su secuencia en la tabla InstallExecuteSequence de forma que llegue después de la acción CostFinalize.

Para corregir el error de CA3, cambie su secuencia en la tabla InstallExecuteSequence de forma que llegue antes de la acción CostFinalize.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



