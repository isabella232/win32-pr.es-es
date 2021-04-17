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
# <a name="lockpermissions-table"></a><span data-ttu-id="c2ef7-104">Tabla LockPermissions</span><span class="sxs-lookup"><span data-stu-id="c2ef7-104">LockPermissions Table</span></span>

<span data-ttu-id="c2ef7-105">La tabla LockPermissions se usa para proteger las partes individuales de una aplicación en un entorno bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-105">The LockPermissions Table is used to secure individual portions of an application in a locked-down environment.</span></span> <span data-ttu-id="c2ef7-106">Se puede usar con la instalación de archivos, claves del registro y carpetas creadas.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-106">It can be used with the installation of files, registry keys, and created folders.</span></span>

<span data-ttu-id="c2ef7-107">Un paquete diseñado para la instalación en Windows Server 2008 R2 o Windows 7 debe usar la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) en lugar de la tabla LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-107">A package intended for installation in Windows Server 2008 R2 or Windows 7 should use the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) rather than the LockPermissions Table.</span></span> <span data-ttu-id="c2ef7-108">Windows Installer versiones anteriores a Windows Installer 5,0 omitirán la tabla MsiLockPermissionsEx.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-108">Windows Installer versions earlier than Windows Installer 5.0 ignore the MsiLockPermissionsEx Table.</span></span> <span data-ttu-id="c2ef7-109">Windows Installer 5,0 puede instalar un paquete que contenga la tabla LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-109">Windows Installer 5.0 can install an package that contains the LockPermissions Table.</span></span> <span data-ttu-id="c2ef7-110">A partir de Windows Installer 5,0, se produce un error en la instalación de un paquete que contiene la tabla MsiLockPermissionsEx y la tabla LockPermissions y se devuelve Windows Installer mensaje de error 1941.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-110">Beginning with Windows Installer 5.0, installation of a package that contains both the MsiLockPermissionsEx Table and the LockPermissions Table fails and returns Windows Installer error message 1941.</span></span>

<span data-ttu-id="c2ef7-111">La tabla LockPermissions tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-111">The LockPermissions Table has the following columns.</span></span>



| <span data-ttu-id="c2ef7-112">Columna</span><span class="sxs-lookup"><span data-stu-id="c2ef7-112">Column</span></span>     | <span data-ttu-id="c2ef7-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2ef7-113">Type</span></span>                               | <span data-ttu-id="c2ef7-114">Clave</span><span class="sxs-lookup"><span data-stu-id="c2ef7-114">Key</span></span> | <span data-ttu-id="c2ef7-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="c2ef7-115">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="c2ef7-116">LockObject</span><span class="sxs-lookup"><span data-stu-id="c2ef7-116">LockObject</span></span> | [<span data-ttu-id="c2ef7-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="c2ef7-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="c2ef7-118">Y</span><span class="sxs-lookup"><span data-stu-id="c2ef7-118">Y</span></span>   | <span data-ttu-id="c2ef7-119">N</span><span class="sxs-lookup"><span data-stu-id="c2ef7-119">N</span></span>        |
| <span data-ttu-id="c2ef7-120">Tabla</span><span class="sxs-lookup"><span data-stu-id="c2ef7-120">Table</span></span>      | [<span data-ttu-id="c2ef7-121">Texto</span><span class="sxs-lookup"><span data-stu-id="c2ef7-121">Text</span></span>](text.md)                   | <span data-ttu-id="c2ef7-122">Y</span><span class="sxs-lookup"><span data-stu-id="c2ef7-122">Y</span></span>   | <span data-ttu-id="c2ef7-123">N</span><span class="sxs-lookup"><span data-stu-id="c2ef7-123">N</span></span>        |
| <span data-ttu-id="c2ef7-124">Domain</span><span class="sxs-lookup"><span data-stu-id="c2ef7-124">Domain</span></span>     | [<span data-ttu-id="c2ef7-125">Formatea</span><span class="sxs-lookup"><span data-stu-id="c2ef7-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="c2ef7-126">Y</span><span class="sxs-lookup"><span data-stu-id="c2ef7-126">Y</span></span>   | <span data-ttu-id="c2ef7-127">Y</span><span class="sxs-lookup"><span data-stu-id="c2ef7-127">Y</span></span>        |
| <span data-ttu-id="c2ef7-128">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="c2ef7-128">User</span></span>       | [<span data-ttu-id="c2ef7-129">Formatea</span><span class="sxs-lookup"><span data-stu-id="c2ef7-129">Formatted</span></span>](formatted.md)         | <span data-ttu-id="c2ef7-130">Y</span><span class="sxs-lookup"><span data-stu-id="c2ef7-130">Y</span></span>   | <span data-ttu-id="c2ef7-131">N</span><span class="sxs-lookup"><span data-stu-id="c2ef7-131">N</span></span>        |
| <span data-ttu-id="c2ef7-132">Permiso</span><span class="sxs-lookup"><span data-stu-id="c2ef7-132">Permission</span></span> | [<span data-ttu-id="c2ef7-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="c2ef7-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="c2ef7-134">N</span><span class="sxs-lookup"><span data-stu-id="c2ef7-134">N</span></span>   | <span data-ttu-id="c2ef7-135">Y</span><span class="sxs-lookup"><span data-stu-id="c2ef7-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c2ef7-136">Columnas</span><span class="sxs-lookup"><span data-stu-id="c2ef7-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c2ef7-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="c2ef7-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="c2ef7-138">Esta columna y la columna de la tabla especifican conjuntamente el archivo, el directorio o la clave del registro que se va a proteger.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-138">This column and the Table column together specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="c2ef7-139">La columna LockObject es una clave externa que apunta a la clave principal de la tabla especificada por la columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-139">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="c2ef7-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro</span><span class="sxs-lookup"><span data-stu-id="c2ef7-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="c2ef7-141">Esta columna y la columna LockObject especifican el archivo, el directorio o la clave del registro que se va a proteger.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-141">This column and the LockObject column specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="c2ef7-142">En la columna de la tabla, escriba File, Registry o CreateFolder para especificar un LockObject incluido en la tabla de [archivos](file-table.md), en la [tabla del registro](registry-table.md)o en la [tabla CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="c2ef7-142">In the Table column, enter File, Registry, or CreateFolder to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), or [CreateFolder Table](createfolder-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2ef7-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Dominio</span><span class="sxs-lookup"><span data-stu-id="c2ef7-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domain</span></span>
</dt> <dd>

<span data-ttu-id="c2ef7-144">Columna que identifica el dominio del usuario para el que se van a establecer los permisos.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-144">The column that identifies the domain of the user for which permissions are to be set.</span></span> <span data-ttu-id="c2ef7-145">Es el nombre de un equipo independiente o un nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-145">This is the name of a stand-alone machine or a domain name.</span></span> <span data-ttu-id="c2ef7-146">El tipo de datos de la columna está [formateado](formatted.md)y puede usar la cadena \[ % USERDOMAIN \] en este campo para obtener el valor de la variable de entorno USERDOMAIN para el dominio actual.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-146">The column data type is [Formatted](formatted.md), and you may use the string \[%USERDOMAIN\] in this field to get the value of the USERDOMAIN environment variable for the current domain.</span></span> <span data-ttu-id="c2ef7-147">Para obtener cualquier otro dominio, se requiere el uso de [acciones personalizadas](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c2ef7-147">To get any other domain requires using [Custom Actions](custom-actions.md).</span></span> <span data-ttu-id="c2ef7-148">Para obtener más información, vea la tabla de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-148">For more information, see the Custom Action Table.</span></span>

</dd> <dt>

<span data-ttu-id="c2ef7-149"><span id="User"></span><span id="user"></span><span id="USER"></span>Usuario</span><span class="sxs-lookup"><span data-stu-id="c2ef7-149"><span id="User"></span><span id="user"></span><span id="USER"></span>User</span></span>
</dt> <dd>

<span data-ttu-id="c2ef7-150">Columna que identifica el nombre localizado del usuario para el que se van a establecer los permisos.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-150">The column that identifies the localized name of the user for which permissions are to be set.</span></span> <span data-ttu-id="c2ef7-151">Este nombre debe estar ubicado en el equipo o dominio.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-151">This name must be located on the machine or domain.</span></span> <span data-ttu-id="c2ef7-152">Se produce un error en la instalación si el equipo o el controlador de dominio no reconoce el dominio y la combinación de usuarios, o si no se puede recuperar el identificador de seguridad (SID) del usuario.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-152">The installation fails if the machine or domain controller does not recognize the domain and user combination or if the user's security identifier (SID) cannot be retrieved.</span></span> <span data-ttu-id="c2ef7-153">Se pueden especificar varios usuarios para un único LockObject.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-153">Multiple users can be specified for a single LockObject.</span></span>

<span data-ttu-id="c2ef7-154">Los nombres de usuario comunes "todos" y "administradores" se pueden escribir en inglés y se asignan a SID conocidos.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-154">The common user names "Everyone" and "Administrators" may be entered in English and are mapped to well-known SIDs.</span></span> <span data-ttu-id="c2ef7-155">LocalSystem tiene control total en todos los descriptores de seguridad creados a través de la tabla LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-155">LocalSystem is given full control in all security descriptors created through the LockPermissions Table.</span></span> <span data-ttu-id="c2ef7-156">Puede usar la propiedad [**ComputerName**](computername.md), la propiedad [**LogonUser**](logonuser.md) o la [**propiedad username**](username.md) en este campo para obtener el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-156">You can use the [**ComputerName Property**](computername.md), [**LogonUser Property**](logonuser.md) or [**USERNAME Property**](username.md) in this field to get the current user.</span></span> <span data-ttu-id="c2ef7-157">Se requiere una acción personalizada para escribir el nombre localizado de cualquier otro usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-157">A custom action is required to enter the localized name of any other user or group.</span></span>

<span data-ttu-id="c2ef7-158">Puede usar varios registros con las mismas entradas de la tabla y LockObject (pero entradas de usuario diferentes) para especificar listas de control de acceso para varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-158">You can use multiple records with identical LockObject and Table entries (but different User entries) to specify access control lists for multiple users.</span></span>

</dd> <dt>

<span data-ttu-id="c2ef7-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permiso</span><span class="sxs-lookup"><span data-stu-id="c2ef7-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permission</span></span>
</dt> <dd>

<span data-ttu-id="c2ef7-160">Columna que identifica la descripción entera de los privilegios del sistema.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-160">The column that identifies the integer description of system privileges.</span></span> <span data-ttu-id="c2ef7-161">A continuación se proporcionan los valores que se usan con más frecuencia (una lista completa existe en Winnt. h).</span><span class="sxs-lookup"><span data-stu-id="c2ef7-161">The following gives the most commonly used values (a complete list exists in Winnt.h).</span></span>



| <span data-ttu-id="c2ef7-162">Privilegio</span><span class="sxs-lookup"><span data-stu-id="c2ef7-162">Privilege</span></span>                                                              | <span data-ttu-id="c2ef7-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2ef7-163">Description</span></span>                     |
|------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="c2ef7-164">todos GENÉRICOs \_</span><span class="sxs-lookup"><span data-stu-id="c2ef7-164">GENERIC\_ALL</span></span><br/> <span data-ttu-id="c2ef7-165">0X10000000</span><span class="sxs-lookup"><span data-stu-id="c2ef7-165">0X10000000</span></span><br/> <span data-ttu-id="c2ef7-166">268435456</span><span class="sxs-lookup"><span data-stu-id="c2ef7-166">268435456</span></span><br/>     | <span data-ttu-id="c2ef7-167">Lectura, escritura y ejecución de acceso</span><span class="sxs-lookup"><span data-stu-id="c2ef7-167">Read, write, and execute access</span></span> |
| <span data-ttu-id="c2ef7-168">\_ejecución genérica</span><span class="sxs-lookup"><span data-stu-id="c2ef7-168">GENERIC\_EXECUTE</span></span><br/> <span data-ttu-id="c2ef7-169">0X20000000</span><span class="sxs-lookup"><span data-stu-id="c2ef7-169">0X20000000</span></span><br/> <span data-ttu-id="c2ef7-170">536870912</span><span class="sxs-lookup"><span data-stu-id="c2ef7-170">536870912</span></span><br/> | <span data-ttu-id="c2ef7-171">Ejecutar acceso</span><span class="sxs-lookup"><span data-stu-id="c2ef7-171">Execute access</span></span>                  |
| <span data-ttu-id="c2ef7-172">\_escritura genérica</span><span class="sxs-lookup"><span data-stu-id="c2ef7-172">GENERIC\_WRITE</span></span><br/> <span data-ttu-id="c2ef7-173">0X40000000</span><span class="sxs-lookup"><span data-stu-id="c2ef7-173">0X40000000</span></span><br/> <span data-ttu-id="c2ef7-174">1073741824</span><span class="sxs-lookup"><span data-stu-id="c2ef7-174">1073741824</span></span><br/>  | <span data-ttu-id="c2ef7-175">Acceso de escritura</span><span class="sxs-lookup"><span data-stu-id="c2ef7-175">Write access</span></span>                    |



 

<span data-ttu-id="c2ef7-176">No se puede especificar una \_ lectura genérica en la columna Permission.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-176">You cannot specify GENERIC\_READ in the Permission column.</span></span> <span data-ttu-id="c2ef7-177">Si intenta hacerlo, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-177">Attempting to do so will fail.</span></span> <span data-ttu-id="c2ef7-178">En su lugar, debe especificar un valor como lectura de clave \_ o archivo \_ genérico de \_ lectura.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-178">Instead, you must specify a value such as KEY\_READ or FILE\_GENERIC\_READ.</span></span>

<span data-ttu-id="c2ef7-179">El valor NULL especificado en esta columna está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-179">Null entered in this column is reserved for future use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2ef7-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2ef7-180">Remarks</span></span>

<span data-ttu-id="c2ef7-181">Las acciones [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md)y [CreateFolders](createfolders-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-181">The [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md), and [CreateFolders](createfolders-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="c2ef7-182">Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="c2ef7-182">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="c2ef7-183">El permiso solo se puede establecer en la tabla LockPermissions para los usuarios que ya existen en el equipo o dominio.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-183">Permission can only be set in the LockPermissions Table for users that already exist on the computer or domain.</span></span> <span data-ttu-id="c2ef7-184">Un intento de establecer permisos para un usuario desconocido produce un error en la instalación, incluso si esa cuenta de usuario se crea durante la instalación mediante una acción personalizada diferida.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-184">An attempt to set permissions for an unknown user causes the installation to fail, even if that user account is created during the installation by a deferred custom action.</span></span>

<span data-ttu-id="c2ef7-185">Se recomienda incluir el grupo local del administrador del sistema en todas las listas de control de acceso (ACL).</span><span class="sxs-lookup"><span data-stu-id="c2ef7-185">It is recommended that the system administrator's local group be included in all access control lists (ACL).</span></span> <span data-ttu-id="c2ef7-186">Esto garantiza que el administrador del sistema pueda tener acceso a los objetos y mantenerlos.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-186">This ensures that the system administrator can access and maintain objects.</span></span>

<span data-ttu-id="c2ef7-187">Todos los archivos, claves del registro o directorios que se enumeran en la tabla LockPermissions reciben un descriptor de seguridad explícito, tanto si reemplaza un objeto existente como si no.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-187">Every file, registry key, or directory that is listed in the LockPermissions Table receives an explicit security descriptor, whether it replaces an existing object or not.</span></span> <span data-ttu-id="c2ef7-188">El Windows Installer intenta preservar la seguridad de los objetos que ya existen en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-188">The Windows Installer attempts to preserve the security on objects that already exist on the system.</span></span> <span data-ttu-id="c2ef7-189">Si un objeto no aparece en la tabla LockPermissions y reemplaza un objeto existente, el reemplazo obtiene la configuración de seguridad del objeto que reemplaza.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-189">If an object is not listed in the LockPermissions Table, and replaces an existing object, the replacement gets the security settings of the object that it replaces.</span></span>

<span data-ttu-id="c2ef7-190">Si un objeto no aparece en la tabla LockPermissions y no reemplaza un objeto existente, no recibe ningún descriptor de seguridad explícito.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-190">If an object is not listed in the LockPermissions Table, and does not replace an existing object, it receives no explicit security descriptor.</span></span> <span data-ttu-id="c2ef7-191">El acceso al nuevo objeto se basa en los atributos de su objeto primario o contenedor.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-191">The access to the new object is based on the attributes of its parent or container object.</span></span> <span data-ttu-id="c2ef7-192">Si un objeto no aparece en la tabla y reemplaza un objeto sin un descriptor de seguridad explícito, el acceso al nuevo objeto se basa en los atributos de su objeto primario o contenedor.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-192">If an object is not listed in the table, and replaces an object with no explicit security descriptor, the access to the new object is based on the attributes of its parent or container object.</span></span>

<span data-ttu-id="c2ef7-193">El Windows Installer establece la propiedad [**UserSID**](usersid.md) en el identificador de seguridad (SID) o el usuario que ejecuta la instalación.</span><span class="sxs-lookup"><span data-stu-id="c2ef7-193">The Windows Installer sets the [**UserSID**](usersid.md) property to the security identifier (SID) or the user running the installation.</span></span>

## <a name="validation"></a><span data-ttu-id="c2ef7-194">Validación</span><span class="sxs-lookup"><span data-stu-id="c2ef7-194">Validation</span></span>

<dl>

[<span data-ttu-id="c2ef7-195">ICE03</span><span class="sxs-lookup"><span data-stu-id="c2ef7-195">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c2ef7-196">ICE06</span><span class="sxs-lookup"><span data-stu-id="c2ef7-196">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c2ef7-197">ICE46</span><span class="sxs-lookup"><span data-stu-id="c2ef7-197">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="c2ef7-198">ICE55</span><span class="sxs-lookup"><span data-stu-id="c2ef7-198">ICE55</span></span>](ice55.md)  
</dl>

 

 




