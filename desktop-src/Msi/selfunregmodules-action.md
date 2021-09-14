---
description: La acción SelfUnregModules anula el registro de todos los módulos enumerados en la tabla SelfReg que están programados para desinstalarse. El instalador no se registra de forma .EXE archivos.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Acción SelfUnregModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260980"
---
# <a name="selfunregmodules-action"></a>Acción SelfUnregModules

La acción SelfUnregModules anula el registro de todos los módulos enumerados en la [tabla SelfReg](selfreg-table.md) que están programados para desinstalarse. El instalador no se registra de forma .EXE archivos.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La [acción InstallValidate](installvalidate-action.md) debe aparecer antes de la acción SelfUnregModules de la secuencia. Si se usa una acción [SelfRegModules,](selfregmodules-action.md) debe aparecer después de la acción SelfUnregModules en la secuencia. Si se [usa una acción RemoveFiles,](removefiles-action.md) debe aparecer después de la acción SelfUnregModules en la secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                             |
|-------|--------------------------------------------------------|
| \[1\] | Identificador del archivo de módulo no registrado.                |
| \[2\] | Identificador de la carpeta que contiene el archivo de módulo no registrado. |



 

## <a name="remarks"></a>Observaciones

La acción SelfUnregModules intenta llamar a la función [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) del módulo que se va a anular el registro. Esta acción se ejecuta con privilegios elevados cuando la instalación se ejecuta con privilegios elevados, como durante una instalación por máquina. Durante una instalación por usuario, el instalador ejecuta esta acción con privilegios de usuario.

Tenga en cuenta que no puede especificar el orden en el que el instalador anula el registro de los archivos DLL de registro automático mediante la acción SelfUnRegModules.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificar el orden de registro propio](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
