---
description: Tenga en cuenta que no puede especificar el orden en que el instalador registra o anula el registro de los archivos DLL autoregistros mediante las acciones SelfRegModules y SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Especificar el orden de registro propio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473926"
---
# <a name="specifying-the-order-of-self-registration"></a>Especificar el orden de registro propio

Tenga en cuenta que no puede especificar el orden en que el instalador registra o anula el registro de los archivos DLL autoregistros mediante las acciones [SelfRegModules](selfregmodules-action.md) y [SelfUnRegModules.](selfunregmodules-action.md) Estas acciones registran todos los módulos enumerados en la [tabla SelfReg](selfreg-table.md). El instalador no registra de forma .exe archivos.

Para especificar el orden en que el instalador registra o anula el registro de módulos, debe usar dos [acciones personalizadas](custom-actions.md) para cada módulo. Una acción personalizada para DllRegisterServer y una segunda para DllUnregisterServer. A continuación, estas acciones personalizadas deben crearse en la tabla [InstallExecuteSequence](installexecutesequence-table.md) en el punto de la secuencia dondequiera que el archivo DLL se registre o se anulará el registro.

En el ejemplo siguiente se muestra cómo crear la base de datos para programar el registro de un archivo DLL en un punto determinado de la secuencia de acciones.

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | FileName  | Secuencia |
|-------|-------------|-----------|----------|
| Mydll | myComponent | Mydll.dll | 13       |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente   | Componentid | Directorio\_ | KeyPath |
|-------------|-------------|-------------|---------|
| myComponent | {*un GUID*}  | myFolder    | Mydll   |



 

[Tabla de directorios](directory-table.md)



| Directorio | Elemento primario \_ del directorio | DefaultDir          |
|-----------|-------------------|---------------------|
| TARGETDIR |                   | SourceDir           |
| myFolder  | TARGETDIR         | myFolder \| My Folder |



 

[CustomAction (tabla)](customaction-table.md)



| Acción     | Tipo | Source   | Destino                                     |
|------------|------|----------|--------------------------------------------|
| mydllREG   | 3170 | myFolder | " \[ SystemFolder \] msiexec" /y " \[ \# mydll \] " |
| mydllUNREG | 3170 | myFolder | " \[ SystemFolder \] msiexec" /z " \[ \# mydll \] " |



 

[InstallExecuteSequence Table](installexecutesequence-table.md) (parcial)



| Acción           | Condición         | Secuencia |
|------------------|-------------------|----------|
| SelfUnregModules |                   | 2200     |
| mydllUNREG       | $myComponent=2    | 2201     |
| RemoveFiles      |                   | 3500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllREG         | $myComponent>2 | 6501     |



 

 

 



