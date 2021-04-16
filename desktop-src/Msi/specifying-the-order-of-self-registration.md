---
description: Tenga en cuenta que no puede especificar el orden en el que el instalador registra o anula el registro de los archivos dll de registro automático mediante las acciones SelfRegModules y SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Especificar el orden de registro automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497788"
---
# <a name="specifying-the-order-of-self-registration"></a>Especificar el orden de registro automático

Tenga en cuenta que no puede especificar el orden en el que el instalador registra o anula el registro de los archivos dll de registro automático mediante las acciones [SelfRegModules](selfregmodules-action.md) y [SelfUnRegModules](selfunregmodules-action.md) . Estas acciones registran todos los módulos que se enumeran en la [tabla SelfReg](selfreg-table.md). El instalador no registra automáticamente los archivos. exe.

Para especificar el orden en el que el instalador registra o anula el registro de módulos, debe usar dos [acciones personalizadas](custom-actions.md) para cada módulo. Una acción personalizada para DllRegisterServer y otro para DllUnregisterServer. Estas acciones personalizadas se deben crear en la [tabla InstallExecuteSequence](installexecutesequence-table.md) en el punto de la secuencia en el que se va a registrar o anular el registro del archivo dll.

En el ejemplo siguiente se muestra cómo crear la base de datos para programar el registro automático de un archivo DLL en un punto determinado de la secuencia de acciones.

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | FileName  | Secuencia |
|-------|-------------|-----------|----------|
| MYDLL | myComponent | Mydll.dll | 13       |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente   | ComponentId | Directorio\_ | Rutas |
|-------------|-------------|-------------|---------|
| myComponent | {*un GUID*}  | myFolder    | MYDLL   |



 

[Tabla de directorio](directory-table.md)



| Directorio | Directorio \_ primario | DefaultDir          |
|-----------|-------------------|---------------------|
| TARGETDIR |                   | SourceDir           |
| myFolder  | TARGETDIR         | carpeta \| mi carpeta |



 

[Tabla CustomAction](customaction-table.md)



| Acción     | Tipo | Source   | Destino                                     |
|------------|------|----------|--------------------------------------------|
| mydllREG   | 3170 | myFolder | " \[ Carpetadelsistema \] msiexec"/y " \[ \# MYDLL \] " |
| mydllUNREG | 3170 | myFolder | " \[ Carpetadelsistema \] msiexec"/z " \[ \# MYDLL \] " |



 

[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Acción           | Condición         | Secuencia |
|------------------|-------------------|----------|
| SelfUnregModules |                   | 2200     |
| mydllUNREG       | $myComponent = 2    | 2201     |
| RemoveFiles      |                   | 3500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllREG         | $myComponent>2 | 6501     |



 

 

 



