---
description: Se usa para proteger partes individuales de una aplicación en un entorno bloqueado. Se puede usar con la instalación de archivos, claves del Registro y carpetas creadas.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Tabla LockPermissions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6724f9559f8bf4b5c0aac4581dab6ad7496e2c0e8e023636e621214760c26c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043145"
---
# <a name="lockpermissions-table"></a>Tabla LockPermissions

La tabla LockPermissions se usa para proteger partes individuales de una aplicación en un entorno bloqueado. Se puede usar con la instalación de archivos, claves del Registro y carpetas creadas.

Un paquete destinado a la instalación en Windows Server 2008 R2 o Windows 7 debe usar la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) en lugar de la tabla LockPermissions. Windows Las versiones del instalador anteriores Windows Installer 5.0 omiten la tabla MsiLockPermissionsEx. Windows El instalador 5.0 puede instalar un paquete que contiene la tabla LockPermissions. A partir de Windows Installer 5.0, se produce un error en la instalación de un paquete que contiene la tabla MsiLockPermissionsEx y la tabla LockPermissions y devuelve el mensaje de error 1941 del instalador de Windows.

La tabla LockPermissions tiene las columnas siguientes.



| Columna     | Tipo                               | Clave | Nullable |
|------------|------------------------------------|-----|----------|
| LockObject | [Identificador](identifier.md)       | Y   | N        |
| Tabla      | [Texto](text.md)                   | Y   | N        |
| Domain     | [Formato](formatted.md)         | Y   | Y        |
| Usuario       | [Formato](formatted.md)         | Y   | N        |
| Permiso | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Esta columna y la columna Tabla juntos especifican el archivo, el directorio o la clave del Registro que se va a proteger. La columna LockObject es una clave externa que apunta a la clave principal de la tabla especificada por la columna Table.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Mesa
</dt> <dd>

Esta columna y la columna LockObject especifican el archivo, directorio o clave del Registro que se va a proteger. En la columna Tabla, escriba File, Registry o CreateFolder para especificar un Elemento LockObject que aparece en la tabla de archivos [,](file-table.md)la tabla del [Registro](registry-table.md)o la [tabla CreateFolder](createfolder-table.md).

</dd> <dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Dominio
</dt> <dd>

Columna que identifica el dominio del usuario para el que se van a establecer los permisos. Este es el nombre de una máquina independiente o un nombre de dominio. El tipo de datos de columna es [Formatted](formatted.md)y puede usar la cadena %USERDOMAIN en este campo para obtener el valor de la variable de entorno USERDOMAIN para \[ el dominio \] actual. Para obtener cualquier otro dominio, es necesario usar [Acciones personalizadas](custom-actions.md). Para obtener más información, vea la tabla de acciones personalizadas.

</dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>Usuario
</dt> <dd>

Columna que identifica el nombre localizado del usuario para el que se van a establecer los permisos. Este nombre debe encontrarse en el equipo o dominio. Se produce un error en la instalación si la máquina o el controlador de dominio no reconocen la combinación de dominio y usuario o si no se puede recuperar el identificador de seguridad (SID) del usuario. Se pueden especificar varios usuarios para un único LockObject.

Los nombres de usuario comunes "Todos" y "Administradores" se pueden especificar en inglés y se asignan a SID conocidos. LocalSystem tiene control total en todos los descriptores de seguridad creados a través de la tabla LockPermissions. Puede usar las propiedades [**ComputerName ,**](computername.md) [**LogonUser o**](logonuser.md) [**USERNAME en**](username.md) este campo para obtener el usuario actual. Se requiere una acción personalizada para escribir el nombre localizado de cualquier otro usuario o grupo.

Puede usar varios registros con entradas LockObject y Table idénticas (pero diferentes entradas user) para especificar listas de control de acceso para varios usuarios.

</dd> <dt>

<span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permiso
</dt> <dd>

Columna que identifica la descripción de enteros de los privilegios del sistema. A continuación se proporciona los valores más usados (existe una lista completa en Winnt.h).



| Privilegio                                                              | Descripción                     |
|------------------------------------------------------------------------|---------------------------------|
| GENERIC \_ ALL<br/> 0X10000000<br/> 268435456<br/>     | Acceso de lectura, escritura y ejecución |
| GENERIC \_ EXECUTE<br/> 0X20000000<br/> 536870912<br/> | Ejecución del acceso                  |
| ESCRITURA \_ GENÉRICA<br/> 0X40000000<br/> 1073741824<br/>  | Acceso de escritura                    |



 

No se puede especificar GENERIC \_ READ en la columna Permission . Si intenta hacerlo, se producirá un error. En su lugar, debe especificar un valor como KEY \_ READ o FILE GENERIC \_ \_ READ.

El valor NULL especificado en esta columna está reservado para su uso futuro.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las [acciones InstallFiles,](installfiles-action.md) [WriteRegistryValues](writeregistryvalues-action.md)y [CreateFolders](createfolders-action.md) de las tablas de secuencia [*procesan*](s-gly.md) la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

El permiso solo se puede establecer en la tabla LockPermissions para los usuarios que ya existen en el equipo o dominio. Un intento de establecer permisos para un usuario desconocido provoca un error en la instalación, incluso si esa cuenta de usuario se crea durante la instalación mediante una acción personalizada diferida.

Se recomienda incluir el grupo local del administrador del sistema en todas las listas de control de acceso (ACL). Esto garantiza que el administrador del sistema pueda acceder a los objetos y mantenerlos.

Cada archivo, clave del Registro o directorio que aparece en la tabla LockPermissions recibe un descriptor de seguridad explícito, tanto si reemplaza un objeto existente como si no. El Windows de archivos intenta conservar la seguridad de los objetos que ya existen en el sistema. Si un objeto no aparece en la tabla LockPermissions y reemplaza un objeto existente, el reemplazo obtiene la configuración de seguridad del objeto que reemplaza.

Si un objeto no aparece en la tabla LockPermissions y no reemplaza un objeto existente, no recibe ningún descriptor de seguridad explícito. El acceso al nuevo objeto se basa en los atributos de su objeto primario o contenedor. Si un objeto no aparece en la tabla y reemplaza un objeto por ningún descriptor de seguridad explícito, el acceso al nuevo objeto se basa en los atributos de su objeto primario o contenedor.

El Windows establece la [**propiedad UserSID**](usersid.md) en el identificador de seguridad (SID) o el usuario que ejecuta la instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE55](ice55.md)  
</dl>

 

 




