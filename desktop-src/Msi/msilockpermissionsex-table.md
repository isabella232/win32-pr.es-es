---
description: La tabla MsiLockPermissionsEx se puede usar para proteger los servicios, los archivos, las claves del Registro y las carpetas creadas.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Tabla MsiLockPermissionsEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266188"
---
# <a name="msilockpermissionsex-table"></a>Tabla MsiLockPermissionsEx

La tabla MsiLockPermissionsEx se puede usar para proteger los servicios, los archivos, las claves del Registro y las carpetas creadas.

Un paquete no debe contener la tabla MsiLockPermissionsEx y [la tabla LockPermissions](lockpermissions-table.md).

**[Windows instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta tabla se recomienda para los paquetes destinados a la instalación con Windows Installer 5.0 o posterior.

La tabla MsiLockPermissionsEx tiene las siguientes columnas.



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

Esta columna y la columna Tabla especifican juntos el archivo, el directorio, la clave del Registro o el servicio que se va a proteger. La columna LockObject es una clave externa que apunta a la clave principal de la tabla especificada por la columna Tabla.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Mesa
</dt> <dd>

Esta columna y la columna LockObject especifican el archivo, el directorio, la clave del Registro o el servicio que se va a proteger. En la columna Tabla, escriba File, Registry, CreateFolder o ServiceInstall para especificar un LockObject enumerado en la tabla [file,](file-table.md) [registry table,](registry-table.md) [createfolder table](createfolder-table.md)o [serviceinstall table](serviceinstall-table.md).

</dd> <dt>

<span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText
</dt> <dd>

Escriba la cadena SDDL para indicar los permisos que se aplicarán al objeto seleccionado. El SDDL debe proporcionarse en formato [de cadena del descriptor de seguridad](../secauthz/security-descriptor-string-format.md).

Esto no admite propiedades privadas o públicas.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Esta columna contiene una expresión condicional que se usa para determinar si se debe aplicar el permiso especificado. Si la condición se evalúa como **FALSE,** no se aplica el permiso. Si la condición se evalúa como **TRUE**, se aplica el permiso.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Consulte [Protección de recursos para](securing-resources-.md)obtener más información sobre la protección de servicios, archivos, claves del Registro y carpetas creadas.

Use la tabla MsiLockPermissionsEx para proteger los objetos de una cuenta de usuario que se crea durante la instalación. La cuenta de usuario ya debe existir cuando la instalación protege el objeto. Cree la cuenta de usuario antes de instalar el archivo, la clave del Registro, la carpeta o el servicio que se va a proteger.

Si un par LockObject y Table de esta tabla tiene más de una expresión condicional que se evalúa como true, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1942.

Si la cadena [FormattedSDDLText](formattedsddltext.md) del campo SDDLText no se puede resolver en una cadena SDDL válida, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1943.

Si el usuario no tiene privilegios suficientes para establecer el descriptor de seguridad especificado por el campo SDDLText en un archivo o carpeta, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1926.

Si el usuario no tiene privilegios suficientes para establecer el descriptor de seguridad especificado por el campo SDDLText en una clave del Registro, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1401.

Si el usuario no tiene privilegios suficientes para establecer el descriptor de seguridad especificado por el campo SDDLText en un servicio, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1944.

## <a name="validation"></a>Validación

<dl>

[ICE104](ice-104.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 
