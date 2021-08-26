---
description: Tenga en cuenta que no puede especificar el orden en el que el instalador registra o anula el registro de los archivos DLL de registro automático mediante las acciones SelfRegModules y SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Especificar el orden de registro propio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb26fbebad3167fbea95679a1ea7a29c28946ae6fa2dd2b014be6ade986e28f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039685"
---
# <a name="specifying-the-order-of-self-registration"></a>Especificar el orden de registro propio

Tenga en cuenta que no puede especificar el orden en el que el instalador registra o anula el registro de los archivos DLL de registro automático mediante las acciones [SelfRegModules](selfregmodules-action.md) y [SelfUnRegModules.](selfunregmodules-action.md) Estas acciones registran todos los módulos enumerados en la [tabla SelfReg](selfreg-table.md). El instalador no se registra de forma .exe archivos.

Para especificar el orden en que el instalador registra o anula el registro de los módulos, debe usar dos [acciones](custom-actions.md) personalizadas para cada módulo. Una acción personalizada para DllRegisterServer y una segunda para DllUnregisterServer. A continuación, estas acciones personalizadas deben crearse en la tabla [InstallExecuteSequence](installexecutesequence-table.md) en el punto de la secuencia donde quiera que el archivo DLL se registre o se anulará el registro.

En el ejemplo siguiente se muestra cómo crear la base de datos para programar el registro propio de un archivo DLL en un punto determinado de la secuencia de acciones.

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | FileName  | Secuencia |
|-------|-------------|-----------|----------|
| Mydll | myComponent | Mydll.dll | 13       |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente   | Componentid | Directorio\_ | KeyPath |
|-------------|-------------|-------------|---------|
| myComponent | {*a GUID*}  | myFolder    | Mydll   |



 

[Tabla de directorios](directory-table.md)



| Directorio | Elemento \_ primario del directorio | DefaultDir          |
|-----------|-------------------|---------------------|
| TARGETDIR |                   | SourceDir           |
| myFolder  | TARGETDIR         | myFolder \| My Folder |



 

[Tabla CustomAction](customaction-table.md)



| Acción     | Tipo | Source   | Destino                                     |
|------------|------|----------|--------------------------------------------|
| mydllREG   | 3170 | myFolder | " \[ SystemFolder \] msiexec" /y " \[ \# mydll \] " |
| mydllUNREG | 3170 | myFolder | " \[ SystemFolder \] msiexec" /z " \[ \# mydll \] " |



 

[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Acción           | Condición         | Secuencia |
|------------------|-------------------|----------|
| SelfUnregModules |                   | 2200     |
| mydllUNREG       | $myComponent=2    | 2201     |
| RemoveFiles      |                   | 3500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllREG         | $myComponent>2 | 6501     |



 

 

 



