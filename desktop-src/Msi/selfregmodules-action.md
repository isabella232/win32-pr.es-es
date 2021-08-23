---
description: La acción SelfRegModules procesa todos los módulos enumerados en la tabla SelfReg y registra todos los módulos instalados en el sistema. El instalador no registra archivos EXE de forma independiente.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Acción SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf137dc63baa72a3d5b93370e40911af93691eaa911c4081990656c84091870
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630045"
---
# <a name="selfregmodules-action"></a>Acción SelfRegModules

La acción SelfRegModules procesa todos los módulos enumerados en la [tabla SelfReg](selfreg-table.md) y registra todos los módulos instalados en el sistema. El instalador no registra archivos EXE de forma independiente.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de llamar a la acción SelfRegModules. Si se [usa una acción InstallFiles,](installfiles-action.md) debe aparecer antes de la acción SelfRegModules en la secuencia. Dado que la acción SelfRegModules cambia el sistema, SelfRegModules debe ir después de [la acción InstallInitialize](installinitialize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                           |
|-------|------------------------------------------------------|
| \[1\] | Identificador del archivo de módulo registrado.                |
| \[2\] | Identificador de la carpeta que contiene el archivo de módulo registrado. |



 

## <a name="remarks"></a>Comentarios

La acción SelfRegModules intenta llamar a [la función DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) del módulo programado para registrarse. Esta acción se ejecuta con privilegios elevados cuando la instalación se ejecuta con privilegios elevados, como durante una instalación por máquina. Durante una instalación por usuario, el instalador ejecuta esta acción con privilegios de usuario.

Tenga en cuenta que no puede especificar el orden en que el instalador registra los archivos DLL autoregregados mediante la [acción SelfUnRegModules](selfunregmodules-action.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificar el orden de registro propio](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
