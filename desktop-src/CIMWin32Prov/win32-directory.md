---
description: El \_ directorio Win32&\# 32; La clase WMI representa una entrada de directorio en un equipo que ejecuta Windows.
ms.assetid: d61cb5ee-8e87-4604-95e6-325c9b543411
ms.tgt_platform: multiple
title: Win32_Directory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory
- Win32_Directory.Caption
- Win32_Directory.Description
- Win32_Directory.InstallDate
- Win32_Directory.Name
- Win32_Directory.Status
- Win32_Directory.AccessMask
- Win32_Directory.Archive
- Win32_Directory.Compressed
- Win32_Directory.CompressionMethod
- Win32_Directory.CreationClassName
- Win32_Directory.CreationDate
- Win32_Directory.CSCreationClassName
- Win32_Directory.CSName
- Win32_Directory.Drive
- Win32_Directory.EightDotThreeFileName
- Win32_Directory.Encrypted
- Win32_Directory.EncryptionMethod
- Win32_Directory.Extension
- Win32_Directory.FileName
- Win32_Directory.FileSize
- Win32_Directory.FileType
- Win32_Directory.FSCreationClassName
- Win32_Directory.FSName
- Win32_Directory.Hidden
- Win32_Directory.InUseCount
- Win32_Directory.LastAccessed
- Win32_Directory.LastModified
- Win32_Directory.Path
- Win32_Directory.Readable
- Win32_Directory.System
- Win32_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6185b9c0d427b7410d36f3fddfaf70c0ed8d364b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275052"
---
# <a name="win32_directory-class"></a><span data-ttu-id="795e4-103">\_Clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="795e4-103">Win32\_Directory class</span></span>

<span data-ttu-id="795e4-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ directorio Win32** representa una entrada de directorio en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="795e4-104">The **Win32\_Directory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a directory entry on a computer system running Windows.</span></span> <span data-ttu-id="795e4-105">Un directorio es un tipo de archivo que agrupa lógicamente los archivos de datos y proporciona información de ruta de acceso para los archivos agrupados.</span><span class="sxs-lookup"><span data-stu-id="795e4-105">A directory is a type of file that logically groups data files and provides path information for the grouped files.</span></span> <span data-ttu-id="795e4-106">Ejemplo: C: \\ temp.</span><span class="sxs-lookup"><span data-stu-id="795e4-106">Example: C:\\TEMP.</span></span> <span data-ttu-id="795e4-107">**Win32 \_ El directorio** no incluye los directorios de las unidades de red.</span><span class="sxs-lookup"><span data-stu-id="795e4-107">**Win32\_Directory** does not include directories of network drives.</span></span>

<span data-ttu-id="795e4-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="795e4-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="795e4-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="795e4-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="795e4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="795e4-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Directory : CIM_Directory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   AccessMask;
  boolean  Archive;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Path;
  boolean  Readable;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="795e4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="795e4-111">Members</span></span>

<span data-ttu-id="795e4-112">La clase de **\_ directorio Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="795e4-112">The **Win32\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="795e4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="795e4-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="795e4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="795e4-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="795e4-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="795e4-115">Methods</span></span>

<span data-ttu-id="795e4-116">La clase de **\_ directorio Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="795e4-116">The **Win32\_Directory** class has these methods.</span></span>



| <span data-ttu-id="795e4-117">Método</span><span class="sxs-lookup"><span data-stu-id="795e4-117">Method</span></span>                                                                                             | <span data-ttu-id="795e4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="795e4-118">Description</span></span>                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="795e4-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="795e4-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-directory.md)     | <span data-ttu-id="795e4-120">Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-120">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="795e4-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="795e4-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-directory.md) | <span data-ttu-id="795e4-122">Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-122">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="795e4-123">**Comprimir**</span><span class="sxs-lookup"><span data-stu-id="795e4-123">**Compress**</span></span>](compress-method-in-class-win32-directory.md)                                       | <span data-ttu-id="795e4-124">Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-124">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="795e4-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="795e4-125">**CompressEx**</span></span>](compressex-method-in-class-win32-directory.md)                                   | <span data-ttu-id="795e4-126">Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-126">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="795e4-127">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="795e4-127">**Copy**</span></span>](copy-method-in-class-win32-directory.md)                                               | <span data-ttu-id="795e4-128">Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="795e4-128">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                        |
| [<span data-ttu-id="795e4-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="795e4-129">**CopyEx**</span></span>](copyex-method-in-class-win32-directory.md)                                           | <span data-ttu-id="795e4-130">Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="795e4-130">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                   |
| [<span data-ttu-id="795e4-131">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="795e4-131">**Delete**</span></span>](delete-method-in-class-win32-directory.md)                                           | <span data-ttu-id="795e4-132">Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-132">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="795e4-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="795e4-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-directory.md)                                       | <span data-ttu-id="795e4-134">Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-134">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="795e4-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="795e4-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-directory.md)           | <span data-ttu-id="795e4-136">Método de clase que determina si el llamador tiene los permisos agregados especificados por el argumento *Permissions* no solo en el objeto de archivo, sino en el recurso compartido en el que reside el archivo o directorio (si está en un recurso compartido).</span><span class="sxs-lookup"><span data-stu-id="795e4-136">Class method that determines whether the caller has the aggregated permissions specified by the *Permissions* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="795e4-137">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="795e4-137">**Rename**</span></span>](rename-method-in-class-win32-directory.md)                                           | <span data-ttu-id="795e4-138">Método de clase que cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="795e4-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="795e4-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-directory.md)                             | <span data-ttu-id="795e4-140">Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-140">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="795e4-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="795e4-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-directory.md)                         | <span data-ttu-id="795e4-142">Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="795e4-143">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="795e4-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)                                   | <span data-ttu-id="795e4-144">Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-144">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="795e4-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="795e4-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-directory.md)                               | <span data-ttu-id="795e4-146">Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-146">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="795e4-147">Propiedades</span><span class="sxs-lookup"><span data-stu-id="795e4-147">Properties</span></span>

<span data-ttu-id="795e4-148">La clase de **\_ directorio Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="795e4-148">The **Win32\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="795e4-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="795e4-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="795e4-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-152">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("derechos de acceso")</span><span class="sxs-lookup"><span data-stu-id="795e4-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-153">Máscara de máscara que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el directorio.</span><span class="sxs-lookup"><span data-stu-id="795e4-153">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="795e4-154">Para los valores de bit, consulte [**constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="795e4-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="795e4-155">En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="795e4-156">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="795e4-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="795e4-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-158">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-158">Grants the right to read data from the file.</span></span> <span data-ttu-id="795e4-159">Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="795e4-159">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="795e4-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="795e4-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-161">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-161">Grants the right to write data to the file.</span></span> <span data-ttu-id="795e4-162">Para un directorio, este valor concede el derecho a crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="795e4-162">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="795e4-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Archivo \_ de ANEXAr \_ datos (archivo) o \_ \_ subdirectorio de adición de archivo** (4)</span><span class="sxs-lookup"><span data-stu-id="795e4-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-164">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-164">Grants the right to append data to the file.</span></span> <span data-ttu-id="795e4-165">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="795e4-165">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="795e4-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="795e4-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-167">Concede el derecho para leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="795e4-167">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="795e4-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="795e4-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-169">Concede el derecho para escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="795e4-169">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="795e4-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="795e4-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-171">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-171">Grants the right to execute a file.</span></span> <span data-ttu-id="795e4-172">Para un directorio, se puede atravesar el directorio.</span><span class="sxs-lookup"><span data-stu-id="795e4-172">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="795e4-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="795e4-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-174">Concede el derecho para eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="795e4-174">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="795e4-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="795e4-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-176">Concede el derecho a leer los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-176">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="795e4-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="795e4-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-178">Concede el derecho para cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-178">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="795e4-179"><span id="DELETE"></span><span id="delete"></span>**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="795e4-179"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-180">Concede acceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="795e4-180">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="795e4-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="795e4-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-182">Concede acceso de lectura al descriptor de seguridad y al propietario.</span><span class="sxs-lookup"><span data-stu-id="795e4-182">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="795e4-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="795e4-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-184">Concede acceso de escritura a la ACL discrecional.</span><span class="sxs-lookup"><span data-stu-id="795e4-184">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="795e4-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="795e4-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-186">Asigna el propietario de la escritura.</span><span class="sxs-lookup"><span data-stu-id="795e4-186">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="795e4-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="795e4-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-188">Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="795e4-188">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span data-ttu-id="795e4-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Acceso a \_ \_Seguridad del sistema** (18809343)</span><span class="sxs-lookup"><span data-stu-id="795e4-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**ACCESS\_SYSTEM\_SECURITY** (18809343)</span></span>


</dt> <dd>

<span data-ttu-id="795e4-190">Controla la capacidad de obtener o establecer la SACL en el descriptor de seguridad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-190">Controls the ability to get or set the SACL in an object's security descriptor.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="795e4-191">**Archivar**</span><span class="sxs-lookup"><span data-stu-id="795e4-191">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-192">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="795e4-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-194">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("se debe archivar")</span><span class="sxs-lookup"><span data-stu-id="795e4-194">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-195">Indica si se ha establecido el bit de archivo en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="795e4-195">Indicates whether the archive bit on the folder has been set.</span></span> <span data-ttu-id="795e4-196">Los programas de copia de seguridad utilizan el bit de archivo para identificar los archivos de los que se debe hacer una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="795e4-196">The archive bit is used by backup programs to identify files that should be backed up.</span></span> <span data-ttu-id="795e4-197">Si **es true**, se debe archivar el archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-197">If **True**, the file should be archived.</span></span>

<span data-ttu-id="795e4-198">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-198">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-199">**Caption**</span><span class="sxs-lookup"><span data-stu-id="795e4-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-202">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="795e4-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-203">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-203">A short textual description of the object.</span></span>

<span data-ttu-id="795e4-204">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-205">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="795e4-205">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-206">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="795e4-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-208">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("comprimido")</span><span class="sxs-lookup"><span data-stu-id="795e4-208">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-209">Indica si la carpeta se ha comprimido o no.</span><span class="sxs-lookup"><span data-stu-id="795e4-209">Indicates whether or not the folder has been compressed.</span></span> <span data-ttu-id="795e4-210">WMI reconoce las carpetas comprimidas mediante WMI o mediante la interfaz gráfica de usuario; sin embargo, no reconoce. Archivos ZIP como comprimidos.</span><span class="sxs-lookup"><span data-stu-id="795e4-210">WMI recognizes folders compressed using WMI itself or using the graphical user interface; it does not, however, recognize .ZIP files as being compressed.</span></span> <span data-ttu-id="795e4-211">Si es **true**, el archivo se comprime.</span><span class="sxs-lookup"><span data-stu-id="795e4-211">If **True**, the file is compressed.</span></span>

<span data-ttu-id="795e4-212">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-213">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="795e4-213">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-216">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compresión")</span><span class="sxs-lookup"><span data-stu-id="795e4-216">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-217">Algoritmo o herramienta (normalmente un método) que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="795e4-217">Algorithm or tool (usually a method) used to compress the logical file.</span></span> <span data-ttu-id="795e4-218">Si no es posible (o no desea) describir el esquema de compresión (quizás porque no se conoce), use las siguientes palabras: "Unknown" para indicar que no se conoce si el archivo lógico está comprimido; "Compressed" para representar que el archivo está comprimido, pero su esquema de compresión no se conoce o no se revela; y "no comprimido" para representar que el archivo lógico no está comprimido.</span><span class="sxs-lookup"><span data-stu-id="795e4-218">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed; "Compressed" to represent that the file is compressed, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="795e4-219">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-220">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="795e4-220">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-223">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="795e4-223">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-224">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="795e4-224">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="795e4-225">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="795e4-225">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="795e4-226">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-226">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-227">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="795e4-227">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-228">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="795e4-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-230">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fecha de creación")</span><span class="sxs-lookup"><span data-stu-id="795e4-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-231">Fecha en que se creó el objeto de sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="795e4-231">Date that the file system object was created.</span></span> <span data-ttu-id="795e4-232">Para obtener más información sobre cómo trabajar con formatos de fecha y hora de WMI, vea [tareas de WMI: fechas y horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="795e4-232">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="795e4-233">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-234">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="795e4-234">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-237">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase de sistema de equipo ")</span><span class="sxs-lookup"><span data-stu-id="795e4-237">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-238">Nombre de la clase de creación del sistema de ámbito del equipo.</span><span class="sxs-lookup"><span data-stu-id="795e4-238">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="795e4-239">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-239">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-240">**CSName**</span><span class="sxs-lookup"><span data-stu-id="795e4-240">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-243">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="795e4-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-244">Nombre del equipo en el que se almacena el objeto de sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="795e4-244">Name of the computer where the file system object is stored.</span></span>

<span data-ttu-id="795e4-245">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-245">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-246">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="795e4-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-249">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="795e4-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-250">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-250">A textual description of the object.</span></span>

<span data-ttu-id="795e4-251">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-252">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="795e4-252">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-253">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-255">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="795e4-255">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-256">Letra de unidad de la unidad (incluidos los dos puntos) donde se almacena el objeto de sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="795e4-256">Drive letter of the drive (including colon) where the file system object is stored.</span></span>

<span data-ttu-id="795e4-257">Ejemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="795e4-257">Example: "c:"</span></span>

<span data-ttu-id="795e4-258">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-258">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-259">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="795e4-259">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-260">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-262">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo de ocho puntos tres")</span><span class="sxs-lookup"><span data-stu-id="795e4-262">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-263">Nombre compatible con MS-DOS para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="795e4-263">MS-DOS -compatible name for the folder.</span></span>

<span data-ttu-id="795e4-264">Ejemplo: "c: \\ programa ~ 1"</span><span class="sxs-lookup"><span data-stu-id="795e4-264">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="795e4-265">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-266">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="795e4-266">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-267">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="795e4-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-269">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("cifrado")</span><span class="sxs-lookup"><span data-stu-id="795e4-269">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-270">Indica si la carpeta está cifrada o no.</span><span class="sxs-lookup"><span data-stu-id="795e4-270">Indicates whether or not the folder has been encrypted.</span></span> <span data-ttu-id="795e4-271">Si es **true**, la carpeta está cifrada.</span><span class="sxs-lookup"><span data-stu-id="795e4-271">If **True**, the folder is encrypted.</span></span>

<span data-ttu-id="795e4-272">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-273">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="795e4-273">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-276">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de cifrado")</span><span class="sxs-lookup"><span data-stu-id="795e4-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-277">Algoritmo o herramienta que se usa para cifrar el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="795e4-277">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="795e4-278">Si no es posible (o no desea) describir el esquema de cifrado (quizás por motivos de seguridad), use las siguientes palabras: "Unknown" para representar que no se conoce si el archivo lógico está cifrado; "Cifrado" para representar que el archivo está cifrado, pero el esquema de cifrado no es conocido o no se ha divulgado. y "no cifrado" para representar que el archivo lógico no está cifrado.</span><span class="sxs-lookup"><span data-stu-id="795e4-278">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted; "Encrypted" to represent that the file is encrypted, but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="795e4-279">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-280">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="795e4-280">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-281">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-283">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensión de archivo")</span><span class="sxs-lookup"><span data-stu-id="795e4-283">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-284">Extensión de nombre de archivo del objeto del sistema de archivos, sin incluir el punto (.) que separa la extensión del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-284">File name extension for the file system object, not including the dot (.) that separates the extension from the file name.</span></span>

<span data-ttu-id="795e4-285">Ejemplos: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="795e4-285">Examples: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="795e4-286">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-287">**FileName**</span><span class="sxs-lookup"><span data-stu-id="795e4-287">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-290">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo")</span><span class="sxs-lookup"><span data-stu-id="795e4-290">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-291">Nombre de archivo (sin el punto o la extensión) del archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-291">File name (without the dot or extension) of the file.</span></span>

<span data-ttu-id="795e4-292">Ejemplo: "Autoexec"</span><span class="sxs-lookup"><span data-stu-id="795e4-292">Example: "autoexec"</span></span>

<span data-ttu-id="795e4-293">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-293">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-294">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="795e4-294">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-295">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="795e4-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-297">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="795e4-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-298">Tamaño del objeto del sistema de archivos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="795e4-298">Size of the file system object, in bytes.</span></span> <span data-ttu-id="795e4-299">Aunque las carpetas poseen una propiedad de **archivo** , siempre se devuelve el valor 0.</span><span class="sxs-lookup"><span data-stu-id="795e4-299">Although folders possess a **FileSize** property, the value 0 is always returned.</span></span> <span data-ttu-id="795e4-300">Para determinar el tamaño de una carpeta, use FileSystemObject o agregue el tamaño de todos los archivos almacenados en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="795e4-300">To determine the size of a folder, use the FileSystemObject or add up the size of all the files stored in the folder.</span></span>

<span data-ttu-id="795e4-301">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="795e4-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="795e4-302">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-303">**FileType**</span><span class="sxs-lookup"><span data-stu-id="795e4-303">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-306">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de archivo")</span><span class="sxs-lookup"><span data-stu-id="795e4-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-307">Tipo de archivo (indicado por la propiedad de **extensión** ).</span><span class="sxs-lookup"><span data-stu-id="795e4-307">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="795e4-308">Por ejemplo, es probable que un archivo. mdb tenga el tipo de archivo aplicación de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="795e4-308">For example, an .mdb file is likely to have the file type Microsoft Access Application.</span></span> <span data-ttu-id="795e4-309">Es probable que un archivo. asp tenga el tipo de archivo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="795e4-309">An .asp file likely has the file type HTML Document.</span></span> <span data-ttu-id="795e4-310">Las carpetas se suelen presentar simplemente como carpeta.</span><span class="sxs-lookup"><span data-stu-id="795e4-310">Folders are typically reported simply as Folder.</span></span>

<span data-ttu-id="795e4-311">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-311">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-312">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="795e4-312">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-315">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="795e4-315">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-316">Clase del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="795e4-316">Class of the file system.</span></span>

<span data-ttu-id="795e4-317">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-317">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-318">**FSName**</span><span class="sxs-lookup"><span data-stu-id="795e4-318">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-321">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="795e4-321">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-322">Tipo de sistema de archivos (NTFS, FAT, FAT32) instalado en la unidad donde se encuentra el archivo o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="795e4-322">Type of file system (NTFS, FAT, FAT32) installed on the drive where the file or folder is located.</span></span>

<span data-ttu-id="795e4-323">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-324">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="795e4-324">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-325">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="795e4-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-327">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="795e4-327">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-328">Indica si el objeto del sistema de archivos está oculto.</span><span class="sxs-lookup"><span data-stu-id="795e4-328">Indicates whether the file system object is hidden.</span></span> <span data-ttu-id="795e4-329">Si es **true**, el archivo está oculto.</span><span class="sxs-lookup"><span data-stu-id="795e4-329">If **True**, the file is hidden.</span></span>

<span data-ttu-id="795e4-330">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-331">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="795e4-331">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-332">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="795e4-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-334">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="795e4-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-335">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-335">Indicates when the object was installed.</span></span> <span data-ttu-id="795e4-336">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="795e4-336">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="795e4-337">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-338">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="795e4-338">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-339">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="795e4-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-341">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("recuento de apertura de archivos actuales")</span><span class="sxs-lookup"><span data-stu-id="795e4-341">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-342">Número de "archivos abiertos" que están activos actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-342">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="795e4-343">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-343">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="795e4-344">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="795e4-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-345">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="795e4-345">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-346">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="795e4-346">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-348">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acceso")</span><span class="sxs-lookup"><span data-stu-id="795e4-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-349">Fecha en que se produjo el último acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-349">Date the file was last accessed.</span></span> <span data-ttu-id="795e4-350">Para obtener más información sobre cómo trabajar con formatos de fecha y hora de WMI, vea [tareas de WMI: fechas y horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="795e4-350">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="795e4-351">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-352">**Última**</span><span class="sxs-lookup"><span data-stu-id="795e4-352">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-353">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="795e4-353">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-355">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificación")</span><span class="sxs-lookup"><span data-stu-id="795e4-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-356">Fecha en que se modificó el archivo por última vez.</span><span class="sxs-lookup"><span data-stu-id="795e4-356">Date the file was last modified.</span></span> <span data-ttu-id="795e4-357">Para obtener más información sobre cómo trabajar con formatos de fecha y hora de WMI, vea [tareas de WMI: fechas y horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="795e4-357">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="795e4-358">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-358">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-359">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="795e4-359">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-362">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="795e4-362">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="795e4-363">La propiedad Name es una cadena que representa el nombre heredado que actúa como clave de una instancia de archivo lógico dentro de un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="795e4-363">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="795e4-364">Se deben proporcionar los nombres de ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="795e4-364">Full path names should be provided.</span></span> <span data-ttu-id="795e4-365">Ejemplo: C: \\ Windows \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="795e4-365">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="795e4-366">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-366">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-367">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="795e4-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-368">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-370">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="795e4-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-371">Ruta de acceso del archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-371">Path for the file.</span></span> <span data-ttu-id="795e4-372">La ruta de acceso incluye las barras diagonales inversas iniciales y finales, pero no la letra de unidad o el nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="795e4-372">The path includes the leading and trailing backslashes, but not the drive letter or the folder name.</span></span>

<span data-ttu-id="795e4-373">En la carpeta c: \\ Windows \\ system32 \\ WBEM, la ruta de acceso es \\ Windows \\ system32 \\ .</span><span class="sxs-lookup"><span data-stu-id="795e4-373">For the folder c:\\windows\\system32\\wbem, the path is \\windows\\system32\\.</span></span> <span data-ttu-id="795e4-374">Para la carpeta c: \\ scripts, la ruta de acceso es \\ .</span><span class="sxs-lookup"><span data-stu-id="795e4-374">For the folder c:\\scripts, the path is \\.</span></span>

<span data-ttu-id="795e4-375">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-375">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-376">**Puedan**</span><span class="sxs-lookup"><span data-stu-id="795e4-376">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-377">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="795e4-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-379">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legible")</span><span class="sxs-lookup"><span data-stu-id="795e4-379">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-380">Indica si se pueden leer los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="795e4-380">Indicates whether you can read items in the folder.</span></span> <span data-ttu-id="795e4-381">Si **es true**, se puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-381">If **True**, the file can be read.</span></span>

<span data-ttu-id="795e4-382">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-383">**Estado**</span><span class="sxs-lookup"><span data-stu-id="795e4-383">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-384">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="795e4-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-386">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="795e4-386">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-387">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="795e4-387">String that indicates the current status of the object.</span></span>

<span data-ttu-id="795e4-388">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="795e4-389">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="795e4-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="795e4-390">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="795e4-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="795e4-391">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="795e4-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="795e4-392">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="795e4-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="795e4-393">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="795e4-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="795e4-394">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="795e4-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="795e4-395">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="795e4-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="795e4-396">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="795e4-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="795e4-397">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="795e4-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="795e4-398">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="795e4-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="795e4-399">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="795e4-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="795e4-400">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="795e4-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="795e4-401">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="795e4-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="795e4-402">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="795e4-402">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-403">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="795e4-403">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-405">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("archivo del sistema")</span><span class="sxs-lookup"><span data-stu-id="795e4-405">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-406">Indica si el objeto es un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="795e4-406">Indicates whether the object is a system file.</span></span> <span data-ttu-id="795e4-407">Si es **true**, el archivo es un archivo del sistema</span><span class="sxs-lookup"><span data-stu-id="795e4-407">If **True**, the file is a system file</span></span>

<span data-ttu-id="795e4-408">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-408">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="795e4-409">**Writeable (Grabable)**</span><span class="sxs-lookup"><span data-stu-id="795e4-409">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-410">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="795e4-410">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="795e4-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-412">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("grabable")</span><span class="sxs-lookup"><span data-stu-id="795e4-412">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-413">Si **es true**, se puede escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="795e4-413">If **True**, the file can be written.</span></span>

<span data-ttu-id="795e4-414">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-414">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="795e4-415">Observaciones</span><span class="sxs-lookup"><span data-stu-id="795e4-415">Remarks</span></span>

<span data-ttu-id="795e4-416">La clase de **\_ directorio Win32** se deriva [**del \_ directorio CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="795e4-416">The **Win32\_Directory** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

<span data-ttu-id="795e4-417">**Información general**</span><span class="sxs-lookup"><span data-stu-id="795e4-417">**Overview**</span></span>

<span data-ttu-id="795e4-418">Las carpetas son objetos del sistema de archivos diseñados para contener otros objetos del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="795e4-418">Folders are file system objects designed to contain other file system objects.</span></span> <span data-ttu-id="795e4-419">Sin embargo, esto no significa que todas las carpetas sean iguales.</span><span class="sxs-lookup"><span data-stu-id="795e4-419">This does not mean that all folders are alike, however.</span></span> <span data-ttu-id="795e4-420">En su lugar, las carpetas pueden variar considerablemente.</span><span class="sxs-lookup"><span data-stu-id="795e4-420">Instead, folders can vary considerably.</span></span> <span data-ttu-id="795e4-421">Algunas carpetas son carpetas del sistema operativo, que por lo general no deben modificarse mediante un script.</span><span class="sxs-lookup"><span data-stu-id="795e4-421">Some folders are operating system folders, which generally should not be modified by a script.</span></span> <span data-ttu-id="795e4-422">Algunas carpetas son de solo lectura, lo que significa que los usuarios pueden tener acceso al contenido de la carpeta pero no pueden agregar, eliminar o modificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="795e4-422">Some folders are read-only, which means that users can access the contents of that folder but cannot add to, delete from, or modify those contents.</span></span> <span data-ttu-id="795e4-423">Algunas carpetas están comprimidas para un almacenamiento óptimo, mientras que otras están ocultas y no son visibles para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="795e4-423">Some folders are compressed for optimal storage, while others are hidden and not visible to users.</span></span>

<span data-ttu-id="795e4-424">WMI utiliza la clase de **\_ directorio Win32** para administrar carpetas.</span><span class="sxs-lookup"><span data-stu-id="795e4-424">WMI uses the **Win32\_Directory** class to manage folders.</span></span> <span data-ttu-id="795e4-425">De forma significativa, las propiedades y los métodos disponibles en esta clase son idénticos a las propiedades y los métodos disponibles en la clase de [**\_ archivo de archivos CIM**](cim-datafile.md) , la clase que se usa para administrar archivos.</span><span class="sxs-lookup"><span data-stu-id="795e4-425">Significantly, the properties and methods available in this class are identical to the properties and methods available in the [**CIM\_DataFile**](cim-datafile.md) class, the class used to manage files.</span></span> <span data-ttu-id="795e4-426">Esto significa que, una vez que haya aprendido a administrar carpetas mediante WMI, sin ningún trabajo adicional, también sabrá cómo administrar archivos.</span><span class="sxs-lookup"><span data-stu-id="795e4-426">This means that after you have learned how to manage folders using WMI, you will, without any extra work, also know how to manage files.</span></span>

<span data-ttu-id="795e4-427">La clase de Asociación de [**\_ subdirectorios de Win32**](win32-subdirectory.md) también se utiliza para administrar archivos y carpetas.</span><span class="sxs-lookup"><span data-stu-id="795e4-427">The [**Win32\_Subdirectory**](win32-subdirectory.md) association class is also used to manage files and folders.</span></span> <span data-ttu-id="795e4-428">La clase de **\_ subdirectorio Win32** relaciona una carpeta y sus subcarpetas inmediatas.</span><span class="sxs-lookup"><span data-stu-id="795e4-428">The **Win32\_Subdirectory** class relates a folder and its immediate subfolders.</span></span> <span data-ttu-id="795e4-429">Por ejemplo, en la estructura de carpetas C: \\ scripts \\ registros, logs es una subcarpeta de scripts y scripts es una subcarpeta de la carpeta raíz C: \\ .</span><span class="sxs-lookup"><span data-stu-id="795e4-429">For example, in the folder structure C:\\Scripts\\Logs, Logs is a subfolder of Scripts, and Scripts is a subfolder of the root folder C:\\.</span></span> <span data-ttu-id="795e4-430">Sin embargo, los registros no se consideran una subcarpeta de C: \\ .</span><span class="sxs-lookup"><span data-stu-id="795e4-430">However, Logs is not considered a subfolder of C:\\.</span></span>

<span data-ttu-id="795e4-431">Puede recuperar las propiedades de cualquier carpeta en el sistema de archivos mediante la clase de **\_ directorio Win32** .</span><span class="sxs-lookup"><span data-stu-id="795e4-431">You can retrieve the properties of any folder in the file system using the **Win32\_Directory** class.</span></span> <span data-ttu-id="795e4-432">Las propiedades disponibles mediante esta clase se muestran en la tabla 11,1.</span><span class="sxs-lookup"><span data-stu-id="795e4-432">The properties available using this class are shown in Table 11.1.</span></span> <span data-ttu-id="795e4-433">Para recuperar las propiedades de una sola carpeta, construya una consulta WQL (lenguaje de consulta de Windows) para la clase de **\_ directorio Win32** , asegurándose de incluir el nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="795e4-433">To retrieve the properties for a single folder, construct a Windows Query Language (WQL) query for the **Win32\_Directory** class, making sure that you include the name of the folder.</span></span> <span data-ttu-id="795e4-434">Por ejemplo, esta consulta se enlaza a la carpeta D: \\ Archive:</span><span class="sxs-lookup"><span data-stu-id="795e4-434">For example, this query binds to the folder D:\\Archive:</span></span>

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

<span data-ttu-id="795e4-435">Al especificar un nombre de archivo o carpeta en una consulta WQL, asegúrese de usar dos barras diagonales inversas ( \\ \\ ) para separar los componentes de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="795e4-435">When specifying a file or folder name in a WQL query, be sure you use two backslashes (\\\\) to separate path components.</span></span>

<span data-ttu-id="795e4-436">Si desea limitar la recuperación de datos a una sola unidad de disco, incluya una cláusula WHERE que especifique la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="795e4-436">If you want to limit data retrieval to a single disk drive, include a Where clause specifying the drive letter.</span></span> <span data-ttu-id="795e4-437">Por ejemplo, esta consulta devuelve una lista de todas las carpetas de la unidad C:</span><span class="sxs-lookup"><span data-stu-id="795e4-437">For example, this query returns a list of all the folders on drive C:</span></span>

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

<span data-ttu-id="795e4-438">Si tiene que enumerar todas las carpetas de un equipo, tenga en cuenta que esta consulta puede tardar mucho tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="795e4-438">If you need to enumerate all the folders on a computer, be aware that this query can take an extended time to complete.</span></span>

## <a name="examples"></a><span data-ttu-id="795e4-439">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="795e4-439">Examples</span></span>

<span data-ttu-id="795e4-440">En el siguiente ejemplo de VBScript se recuperan las propiedades de la carpeta C: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="795e4-440">The following VBScript sample retrieves properties for the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 Wscript.Echo "Archive: " & objFolder.Archive
 Wscript.Echo "Caption: " & objFolder.Caption
 Wscript.Echo "Compressed: " & objFolder.Compressed
 Wscript.Echo "Compression method: " & objFolder.CompressionMethod
 Wscript.Echo "Creation date: " & objFolder.CreationDate
 Wscript.Echo "Encrypted: " & objFolder.Encrypted
 Wscript.Echo "Encryption method: " & objFolder.EncryptionMethod
 Wscript.Echo "Hidden: " & objFolder.Hidden
 Wscript.Echo "In use count: " & objFolder.InUseCount
 Wscript.Echo "Last accessed: " & objFolder.LastAccessed
 Wscript.Echo "Last modified: " & objFolder.LastModified
 Wscript.Echo "Name: " & objFolder.Name
 Wscript.Echo "Path: " & objFolder.Path
 Wscript.Echo "Readable: " & objFolder.Readable
 Wscript.Echo "System: " & objFolder.System
 Wscript.Echo "Writeable: " & objFolder.Writeable
Next
```



<span data-ttu-id="795e4-441">El siguiente ejemplo de VBScript devuelve una lista de todas las carpetas ocultas de un equipo.</span><span class="sxs-lookup"><span data-stu-id="795e4-441">The following VBScript sample returns a list of all the hidden folders on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="795e4-442">Requisitos</span><span class="sxs-lookup"><span data-stu-id="795e4-442">Requirements</span></span>



| <span data-ttu-id="795e4-443">Requisito</span><span class="sxs-lookup"><span data-stu-id="795e4-443">Requirement</span></span> | <span data-ttu-id="795e4-444">Value</span><span class="sxs-lookup"><span data-stu-id="795e4-444">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="795e4-445">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="795e4-445">Minimum supported client</span></span><br/> | <span data-ttu-id="795e4-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="795e4-446">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="795e4-447">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="795e4-447">Minimum supported server</span></span><br/> | <span data-ttu-id="795e4-448">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="795e4-448">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="795e4-449">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="795e4-449">Namespace</span></span><br/>                | <span data-ttu-id="795e4-450">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="795e4-450">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="795e4-451">MOF</span><span class="sxs-lookup"><span data-stu-id="795e4-451">MOF</span></span><br/>                      | <dl> <span data-ttu-id="795e4-452"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="795e4-452"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="795e4-453">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="795e4-453">DLL</span></span><br/>                      | <dl> <span data-ttu-id="795e4-454"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="795e4-454"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="795e4-455">Vea también</span><span class="sxs-lookup"><span data-stu-id="795e4-455">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795e4-456">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="795e4-456">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dt>

<span data-ttu-id="795e4-457">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="795e4-457">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

