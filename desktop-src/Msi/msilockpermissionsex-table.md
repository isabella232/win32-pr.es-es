---
description: La tabla MsiLockPermissionsEx se puede usar para proteger servicios, archivos, claves del registro y carpetas creadas.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Tabla MsiLockPermissionsEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678313"
---
# <a name="msilockpermissionsex-table"></a>Tabla MsiLockPermissionsEx

La tabla MsiLockPermissionsEx se puede usar para proteger servicios, archivos, claves del registro y carpetas creadas.

Un paquete no debe contener la tabla MsiLockPermissionsEx y la [tabla LockPermissions](lockpermissions-table.md).

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Esta tabla se recomienda para los paquetes destinados a su instalación con Windows Installer 5,0 o posterior.

La tabla MsiLockPermissionsEx tiene las columnas siguientes.



| Columna               | Tipo                                       | Clave | Nullable |
|----------------------|--------------------------------------------|-----|----------|
| MsiLockPermissionsEx | [Texto](text.md)                           | Y   | N        |
| LockObject           | [Identificador](identifier.md)               | N   | N        |
| Tabla                | [Texto](text.md)                           | N   | N        |
| SDDLText             | [FormattedSDDLText](formattedsddltext.md) | N   | N        |
| Condición            | [Condition](condition.md)                 | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx
</dt> <dd>

Esta es la clave principal de esta tabla.

</dd> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Esta columna y la columna de la tabla especifican conjuntamente el archivo, el directorio, la clave del registro o el servicio que se va a proteger. La columna LockObject es una clave externa que apunta a la clave principal de la tabla especificada por la columna de la tabla.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro
</dt> <dd>

Esta columna y la columna LockObject especifican el archivo, el directorio, la clave del registro o el servicio que se va a proteger. En la columna de la tabla, escriba File, Registry, CreateFolder o ServiceInstall para especificar un LockObject incluido en la tabla [File](file-table.md), la [tabla del registro](registry-table.md), la [tabla CreateFolder](createfolder-table.md)o la [tabla ServiceInstall](serviceinstall-table.md).

</dd> <dt>

<span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText
</dt> <dd>

Escriba la cadena SDDL para indicar los permisos que se aplicarán al objeto seleccionado. El SDDL se debe proporcionar en [formato de cadena de descriptor de seguridad](../secauthz/security-descriptor-string-format.md).

Esto no es compatible con las propiedades públicas o privadas.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple
</dt> <dd>

Esta columna contiene una expresión condicional que se usa para determinar si se va a aplicar el permiso especificado. Si la condición se evalúa como **false**, no se aplica el permiso. Si la condición se evalúa como **true**, se aplica el permiso.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Consulte [protección de recursos](securing-resources-.md)para obtener más información sobre cómo proteger los servicios, los archivos, las claves del registro y las carpetas creadas.

Use la tabla MsiLockPermissionsEx para proteger los objetos de una cuenta de usuario que se crea durante la instalación. La cuenta de usuario ya debe existir cuando la instalación proteja el objeto. Cree la cuenta de usuario antes de instalar el archivo, la clave del registro, la carpeta o el servicio que se protege.

Si un par de tabla y LockObject de esta tabla tiene más de una expresión condicional que se evalúa como true, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1942.

Si la cadena [FormattedSDDLText](formattedsddltext.md) en el campo SDDLText no se puede resolver en una cadena SDDL válida, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1943.

Si el usuario no tiene privilegios suficientes para establecer el descriptor de seguridad especificado por el campo SDDLText en un archivo o carpeta, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1926.

Si el usuario no tiene privilegios suficientes para establecer el descriptor de seguridad especificado por el campo SDDLText en una clave del registro, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1401.

Si el usuario no tiene privilegios suficientes para establecer el descriptor de seguridad especificado por el campo SDDLText en un servicio, se producirá un error en la instalación y Windows Installer devolverá un mensaje de error 1944.

## <a name="validation"></a>Validación

<dl>

[ICE104](ice-104.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 
