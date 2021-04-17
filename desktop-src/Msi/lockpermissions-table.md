---
description: Se usa para proteger las partes individuales de una aplicación en un entorno bloqueado. Se puede usar con la instalación de archivos, claves del registro y carpetas creadas.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Tabla LockPermissions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687444"
---
# <a name="lockpermissions-table"></a>Tabla LockPermissions

La tabla LockPermissions se usa para proteger las partes individuales de una aplicación en un entorno bloqueado. Se puede usar con la instalación de archivos, claves del registro y carpetas creadas.

Un paquete diseñado para la instalación en Windows Server 2008 R2 o Windows 7 debe usar la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) en lugar de la tabla LockPermissions. Windows Installer versiones anteriores a Windows Installer 5,0 omitirán la tabla MsiLockPermissionsEx. Windows Installer 5,0 puede instalar un paquete que contenga la tabla LockPermissions. A partir de Windows Installer 5,0, se produce un error en la instalación de un paquete que contiene la tabla MsiLockPermissionsEx y la tabla LockPermissions y se devuelve Windows Installer mensaje de error 1941.

La tabla LockPermissions tiene las columnas siguientes.



| Columna     | Tipo                               | Clave | Nullable |
|------------|------------------------------------|-----|----------|
| LockObject | [Identificador](identifier.md)       | Y   | N        |
| Tabla      | [Texto](text.md)                   | Y   | N        |
| Domain     | [Formatea](formatted.md)         | Y   | Y        |
| User (Usuario)       | [Formatea](formatted.md)         | Y   | N        |
| Permiso | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Esta columna y la columna de la tabla especifican conjuntamente el archivo, el directorio o la clave del registro que se va a proteger. La columna LockObject es una clave externa que apunta a la clave principal de la tabla especificada por la columna de la tabla.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro
</dt> <dd>

Esta columna y la columna LockObject especifican el archivo, el directorio o la clave del registro que se va a proteger. En la columna de la tabla, escriba File, Registry o CreateFolder para especificar un LockObject incluido en la tabla de [archivos](file-table.md), en la [tabla del registro](registry-table.md)o en la [tabla CreateFolder](createfolder-table.md).

</dd> <dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Dominio
</dt> <dd>

Columna que identifica el dominio del usuario para el que se van a establecer los permisos. Es el nombre de un equipo independiente o un nombre de dominio. El tipo de datos de la columna está [formateado](formatted.md)y puede usar la cadena \[ % USERDOMAIN \] en este campo para obtener el valor de la variable de entorno USERDOMAIN para el dominio actual. Para obtener cualquier otro dominio, se requiere el uso de [acciones personalizadas](custom-actions.md). Para obtener más información, vea la tabla de acciones personalizadas.

</dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>Usuario
</dt> <dd>

Columna que identifica el nombre localizado del usuario para el que se van a establecer los permisos. Este nombre debe estar ubicado en el equipo o dominio. Se produce un error en la instalación si el equipo o el controlador de dominio no reconoce el dominio y la combinación de usuarios, o si no se puede recuperar el identificador de seguridad (SID) del usuario. Se pueden especificar varios usuarios para un único LockObject.

Los nombres de usuario comunes "todos" y "administradores" se pueden escribir en inglés y se asignan a SID conocidos. LocalSystem tiene control total en todos los descriptores de seguridad creados a través de la tabla LockPermissions. Puede usar la propiedad [**ComputerName**](computername.md), la propiedad [**LogonUser**](logonuser.md) o la [**propiedad username**](username.md) en este campo para obtener el usuario actual. Se requiere una acción personalizada para escribir el nombre localizado de cualquier otro usuario o grupo.

Puede usar varios registros con las mismas entradas de la tabla y LockObject (pero entradas de usuario diferentes) para especificar listas de control de acceso para varios usuarios.

</dd> <dt>

<span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permiso
</dt> <dd>

Columna que identifica la descripción entera de los privilegios del sistema. A continuación se proporcionan los valores que se usan con más frecuencia (una lista completa existe en Winnt. h).



| Privilegio                                                              | Descripción                     |
|------------------------------------------------------------------------|---------------------------------|
| todos GENÉRICOs \_<br/> 0X10000000<br/> 268435456<br/>     | Lectura, escritura y ejecución de acceso |
| \_ejecución genérica<br/> 0X20000000<br/> 536870912<br/> | Ejecutar acceso                  |
| \_escritura genérica<br/> 0X40000000<br/> 1073741824<br/>  | Acceso de escritura                    |



 

No se puede especificar una \_ lectura genérica en la columna Permission. Si intenta hacerlo, se producirá un error. En su lugar, debe especificar un valor como lectura de clave \_ o archivo \_ genérico de \_ lectura.

El valor NULL especificado en esta columna está reservado para uso futuro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las acciones [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md)y [CreateFolders](createfolders-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

El permiso solo se puede establecer en la tabla LockPermissions para los usuarios que ya existen en el equipo o dominio. Un intento de establecer permisos para un usuario desconocido produce un error en la instalación, incluso si esa cuenta de usuario se crea durante la instalación mediante una acción personalizada diferida.

Se recomienda incluir el grupo local del administrador del sistema en todas las listas de control de acceso (ACL). Esto garantiza que el administrador del sistema pueda tener acceso a los objetos y mantenerlos.

Todos los archivos, claves del registro o directorios que se enumeran en la tabla LockPermissions reciben un descriptor de seguridad explícito, tanto si reemplaza un objeto existente como si no. El Windows Installer intenta preservar la seguridad de los objetos que ya existen en el sistema. Si un objeto no aparece en la tabla LockPermissions y reemplaza un objeto existente, el reemplazo obtiene la configuración de seguridad del objeto que reemplaza.

Si un objeto no aparece en la tabla LockPermissions y no reemplaza un objeto existente, no recibe ningún descriptor de seguridad explícito. El acceso al nuevo objeto se basa en los atributos de su objeto primario o contenedor. Si un objeto no aparece en la tabla y reemplaza un objeto sin un descriptor de seguridad explícito, el acceso al nuevo objeto se basa en los atributos de su objeto primario o contenedor.

El Windows Installer establece la propiedad [**UserSID**](usersid.md) en el identificador de seguridad (SID) o el usuario que ejecuta la instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE55](ice55.md)  
</dl>

 

 




