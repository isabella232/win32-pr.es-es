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
# <a name="msilockpermissionsex-table"></a><span data-ttu-id="553aa-103">Tabla MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="553aa-103">MsiLockPermissionsEx Table</span></span>

<span data-ttu-id="553aa-104">La tabla MsiLockPermissionsEx se puede usar para proteger servicios, archivos, claves del registro y carpetas creadas.</span><span class="sxs-lookup"><span data-stu-id="553aa-104">The MsiLockPermissionsEx Table can be used to secure services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="553aa-105">Un paquete no debe contener la tabla MsiLockPermissionsEx y la [tabla LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="553aa-105">A package should not contain both the MsiLockPermissionsEx Table and the [LockPermissions Table](lockpermissions-table.md).</span></span>

<span data-ttu-id="553aa-106">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="553aa-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="553aa-107">Esta tabla se recomienda para los paquetes destinados a su instalación con Windows Installer 5,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="553aa-107">This table is recommended for packages intended for installation with Windows Installer 5.0 or later.</span></span>

<span data-ttu-id="553aa-108">La tabla MsiLockPermissionsEx tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="553aa-108">The MsiLockPermissionsEx Table has the following columns.</span></span>



| <span data-ttu-id="553aa-109">Columna</span><span class="sxs-lookup"><span data-stu-id="553aa-109">Column</span></span>               | <span data-ttu-id="553aa-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="553aa-110">Type</span></span>                                       | <span data-ttu-id="553aa-111">Clave</span><span class="sxs-lookup"><span data-stu-id="553aa-111">Key</span></span> | <span data-ttu-id="553aa-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="553aa-112">Nullable</span></span> |
|----------------------|--------------------------------------------|-----|----------|
| <span data-ttu-id="553aa-113">MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="553aa-113">MsiLockPermissionsEx</span></span> | [<span data-ttu-id="553aa-114">Texto</span><span class="sxs-lookup"><span data-stu-id="553aa-114">Text</span></span>](text.md)                           | <span data-ttu-id="553aa-115">Y</span><span class="sxs-lookup"><span data-stu-id="553aa-115">Y</span></span>   | <span data-ttu-id="553aa-116">N</span><span class="sxs-lookup"><span data-stu-id="553aa-116">N</span></span>        |
| <span data-ttu-id="553aa-117">LockObject</span><span class="sxs-lookup"><span data-stu-id="553aa-117">LockObject</span></span>           | [<span data-ttu-id="553aa-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="553aa-118">Identifier</span></span>](identifier.md)               | <span data-ttu-id="553aa-119">N</span><span class="sxs-lookup"><span data-stu-id="553aa-119">N</span></span>   | <span data-ttu-id="553aa-120">N</span><span class="sxs-lookup"><span data-stu-id="553aa-120">N</span></span>        |
| <span data-ttu-id="553aa-121">Tabla</span><span class="sxs-lookup"><span data-stu-id="553aa-121">Table</span></span>                | [<span data-ttu-id="553aa-122">Texto</span><span class="sxs-lookup"><span data-stu-id="553aa-122">Text</span></span>](text.md)                           | <span data-ttu-id="553aa-123">N</span><span class="sxs-lookup"><span data-stu-id="553aa-123">N</span></span>   | <span data-ttu-id="553aa-124">N</span><span class="sxs-lookup"><span data-stu-id="553aa-124">N</span></span>        |
| <span data-ttu-id="553aa-125">SDDLText</span><span class="sxs-lookup"><span data-stu-id="553aa-125">SDDLText</span></span>             | [<span data-ttu-id="553aa-126">FormattedSDDLText</span><span class="sxs-lookup"><span data-stu-id="553aa-126">FormattedSDDLText</span></span>](formattedsddltext.md) | <span data-ttu-id="553aa-127">N</span><span class="sxs-lookup"><span data-stu-id="553aa-127">N</span></span>   | <span data-ttu-id="553aa-128">N</span><span class="sxs-lookup"><span data-stu-id="553aa-128">N</span></span>        |
| <span data-ttu-id="553aa-129">Condición</span><span class="sxs-lookup"><span data-stu-id="553aa-129">Condition</span></span>            | [<span data-ttu-id="553aa-130">Condition</span><span class="sxs-lookup"><span data-stu-id="553aa-130">Condition</span></span>](condition.md)                 | <span data-ttu-id="553aa-131">N</span><span class="sxs-lookup"><span data-stu-id="553aa-131">N</span></span>   | <span data-ttu-id="553aa-132">Y</span><span class="sxs-lookup"><span data-stu-id="553aa-132">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="553aa-133">Columnas</span><span class="sxs-lookup"><span data-stu-id="553aa-133">Columns</span></span>

<dl> <dt>

<span data-ttu-id="553aa-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="553aa-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span></span>
</dt> <dd>

<span data-ttu-id="553aa-135">Esta es la clave principal de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="553aa-135">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="553aa-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="553aa-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="553aa-137">Esta columna y la columna de la tabla especifican conjuntamente el archivo, el directorio, la clave del registro o el servicio que se va a proteger.</span><span class="sxs-lookup"><span data-stu-id="553aa-137">This column and the Table column together specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="553aa-138">La columna LockObject es una clave externa que apunta a la clave principal de la tabla especificada por la columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="553aa-138">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="553aa-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro</span><span class="sxs-lookup"><span data-stu-id="553aa-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="553aa-140">Esta columna y la columna LockObject especifican el archivo, el directorio, la clave del registro o el servicio que se va a proteger.</span><span class="sxs-lookup"><span data-stu-id="553aa-140">This column and the LockObject column specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="553aa-141">En la columna de la tabla, escriba File, Registry, CreateFolder o ServiceInstall para especificar un LockObject incluido en la tabla [File](file-table.md), la [tabla del registro](registry-table.md), la [tabla CreateFolder](createfolder-table.md)o la [tabla ServiceInstall](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="553aa-141">In the Table column, enter File, Registry, CreateFolder, or ServiceInstall to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), [CreateFolder Table](createfolder-table.md), or [ServiceInstall Table](serviceinstall-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="553aa-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span><span class="sxs-lookup"><span data-stu-id="553aa-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span></span>
</dt> <dd>

<span data-ttu-id="553aa-143">Escriba la cadena SDDL para indicar los permisos que se aplicarán al objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="553aa-143">Enter the SDDL string to indicate permissions to apply to selected object.</span></span> <span data-ttu-id="553aa-144">El SDDL se debe proporcionar en [formato de cadena de descriptor de seguridad](../secauthz/security-descriptor-string-format.md).</span><span class="sxs-lookup"><span data-stu-id="553aa-144">The SDDL must be provided in [Security Descriptor String Format](../secauthz/security-descriptor-string-format.md).</span></span>

<span data-ttu-id="553aa-145">Esto no es compatible con las propiedades públicas o privadas.</span><span class="sxs-lookup"><span data-stu-id="553aa-145">This does not support private or public properties.</span></span>

</dd> <dt>

<span data-ttu-id="553aa-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="553aa-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="553aa-147">Esta columna contiene una expresión condicional que se usa para determinar si se va a aplicar el permiso especificado.</span><span class="sxs-lookup"><span data-stu-id="553aa-147">This column contains a conditional expression used to determine whether to apply the specified permission.</span></span> <span data-ttu-id="553aa-148">Si la condición se evalúa como **false**, no se aplica el permiso.</span><span class="sxs-lookup"><span data-stu-id="553aa-148">If the condition evaluates to **FALSE**, the permission is not applied.</span></span> <span data-ttu-id="553aa-149">Si la condición se evalúa como **true**, se aplica el permiso.</span><span class="sxs-lookup"><span data-stu-id="553aa-149">If the condition evaluates to **TRUE**, the permission is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="553aa-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="553aa-150">Remarks</span></span>

<span data-ttu-id="553aa-151">Consulte [protección de recursos](securing-resources-.md)para obtener más información sobre cómo proteger los servicios, los archivos, las claves del registro y las carpetas creadas.</span><span class="sxs-lookup"><span data-stu-id="553aa-151">See [Securing Resources](securing-resources-.md)for more information about securing services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="553aa-152">Use la tabla MsiLockPermissionsEx para proteger los objetos de una cuenta de usuario que se crea durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="553aa-152">Use the MsiLockPermissionsEx Table to secure objects for a user account that is being created during the installation.</span></span> <span data-ttu-id="553aa-153">La cuenta de usuario ya debe existir cuando la instalación proteja el objeto.</span><span class="sxs-lookup"><span data-stu-id="553aa-153">The user account must already exist when the installation secures the object.</span></span> <span data-ttu-id="553aa-154">Cree la cuenta de usuario antes de instalar el archivo, la clave del registro, la carpeta o el servicio que se protege.</span><span class="sxs-lookup"><span data-stu-id="553aa-154">Create the user account before installing the file, registry key, folder or service being secured.</span></span>

<span data-ttu-id="553aa-155">Si un par de tabla y LockObject de esta tabla tiene más de una expresión condicional que se evalúa como true, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1942.</span><span class="sxs-lookup"><span data-stu-id="553aa-155">If a LockObject and Table pair in this table has more than one conditional expression that evaluates to true, the installation fails and Windows Installer returns an error message 1942.</span></span>

<span data-ttu-id="553aa-156">Si la cadena [FormattedSDDLText](formattedsddltext.md) en el campo SDDLText no se puede resolver en una cadena SDDL válida, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1943.</span><span class="sxs-lookup"><span data-stu-id="553aa-156">If the [FormattedSDDLText](formattedsddltext.md) string in the SDDLText field cannot be resolved into a valid SDDL string, the installation fails and Windows Installer returns an error message 1943.</span></span>

<span data-ttu-id="553aa-157">Si el usuario no tiene privilegios suficientes para establecer el descriptor de seguridad especificado por el campo SDDLText en un archivo o carpeta, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1926.</span><span class="sxs-lookup"><span data-stu-id="553aa-157">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a file or folder, the installation fails and Windows Installer returns an error message 1926.</span></span>

<span data-ttu-id="553aa-158">Si el usuario no tiene privilegios suficientes para establecer el descriptor de seguridad especificado por el campo SDDLText en una clave del registro, se produce un error en la instalación y Windows Installer devuelve un mensaje de error 1401.</span><span class="sxs-lookup"><span data-stu-id="553aa-158">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a registry key, the installation fails and Windows Installer returns an error message 1401.</span></span>

<span data-ttu-id="553aa-159">Si el usuario no tiene privilegios suficientes para establecer el descriptor de seguridad especificado por el campo SDDLText en un servicio, se producirá un error en la instalación y Windows Installer devolverá un mensaje de error 1944.</span><span class="sxs-lookup"><span data-stu-id="553aa-159">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a service, the installation fails and Windows Installer returns an error message 1944.</span></span>

## <a name="validation"></a><span data-ttu-id="553aa-160">Validación</span><span class="sxs-lookup"><span data-stu-id="553aa-160">Validation</span></span>

<dl>

[<span data-ttu-id="553aa-161">ICE104</span><span class="sxs-lookup"><span data-stu-id="553aa-161">ICE104</span></span>](ice-104.md)  
[<span data-ttu-id="553aa-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="553aa-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="553aa-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="553aa-163">ICE06</span></span>](ice06.md)  
</dl>

 

 
