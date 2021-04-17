---
description: Win32 \_ ShortcutFile&\# 32; La clase WMI representa archivos que son accesos directos a otros archivos, directorios y comandos.
ms.assetid: 15973234-e418-4869-839e-a7c439512e4e
ms.tgt_platform: multiple
title: Win32_ShortcutFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile
- Win32_ShortcutFile.Caption
- Win32_ShortcutFile.Description
- Win32_ShortcutFile.InstallDate
- Win32_ShortcutFile.Status
- Win32_ShortcutFile.AccessMask
- Win32_ShortcutFile.Archive
- Win32_ShortcutFile.Compressed
- Win32_ShortcutFile.CompressionMethod
- Win32_ShortcutFile.CreationClassName
- Win32_ShortcutFile.CreationDate
- Win32_ShortcutFile.CSCreationClassName
- Win32_ShortcutFile.CSName
- Win32_ShortcutFile.Drive
- Win32_ShortcutFile.EightDotThreeFileName
- Win32_ShortcutFile.Encrypted
- Win32_ShortcutFile.EncryptionMethod
- Win32_ShortcutFile.Name
- Win32_ShortcutFile.Extension
- Win32_ShortcutFile.FileName
- Win32_ShortcutFile.FileSize
- Win32_ShortcutFile.FileType
- Win32_ShortcutFile.FSCreationClassName
- Win32_ShortcutFile.FSName
- Win32_ShortcutFile.Hidden
- Win32_ShortcutFile.InUseCount
- Win32_ShortcutFile.LastAccessed
- Win32_ShortcutFile.LastModified
- Win32_ShortcutFile.Path
- Win32_ShortcutFile.Readable
- Win32_ShortcutFile.System
- Win32_ShortcutFile.Writeable
- Win32_ShortcutFile.Manufacturer
- Win32_ShortcutFile.Version
- Win32_ShortcutFile.Target
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b714b4c8119f92931235734664726123744064d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659737"
---
# <a name="win32_shortcutfile-class"></a><span data-ttu-id="43eba-103">\_Clase Win32 ShortcutFile</span><span class="sxs-lookup"><span data-stu-id="43eba-103">Win32\_ShortcutFile class</span></span>

<span data-ttu-id="43eba-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ ShortcutFile de Win32** representa archivos que son accesos directos a otros archivos, directorios y comandos.</span><span class="sxs-lookup"><span data-stu-id="43eba-104">The **Win32\_ShortcutFile** [WMI class](../wmisdk/retrieving-a-class.md) represents files that are shortcuts to other files, directories, and commands.</span></span>

<span data-ttu-id="43eba-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="43eba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="43eba-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="43eba-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="43eba-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43eba-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE466-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_ShortcutFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
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
  string   Name;
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
  string   Manufacturer;
  string   Version;
  string   Target;
};
```

## <a name="members"></a><span data-ttu-id="43eba-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="43eba-108">Members</span></span>

<span data-ttu-id="43eba-109">La **clase \_ ShortcutFile de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="43eba-109">The **Win32\_ShortcutFile** class has these types of members:</span></span>

-   [<span data-ttu-id="43eba-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="43eba-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="43eba-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43eba-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="43eba-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="43eba-112">Methods</span></span>

<span data-ttu-id="43eba-113">La clase **Win32 \_ ShortcutFile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="43eba-113">The **Win32\_ShortcutFile** class has these methods.</span></span>



| <span data-ttu-id="43eba-114">Método</span><span class="sxs-lookup"><span data-stu-id="43eba-114">Method</span></span>                                                                                                | <span data-ttu-id="43eba-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="43eba-115">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43eba-116">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="43eba-116">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-shortcutfile.md)     | <span data-ttu-id="43eba-117">Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-117">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="43eba-118">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="43eba-118">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-shortcutfile.md) | <span data-ttu-id="43eba-119">Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="43eba-120">**Comprimir**</span><span class="sxs-lookup"><span data-stu-id="43eba-120">**Compress**</span></span>](compress-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="43eba-121">Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-121">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="43eba-122">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="43eba-122">**CompressEx**</span></span>](compressex-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="43eba-123">Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="43eba-124">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="43eba-124">**Copy**</span></span>](copy-method-in-class-win32-shortcutfile.md)                                               | <span data-ttu-id="43eba-125">Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="43eba-125">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="43eba-126">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="43eba-126">**CopyEx**</span></span>](copyex-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="43eba-127">Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="43eba-127">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                |
| [<span data-ttu-id="43eba-128">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="43eba-128">**Delete**</span></span>](delete-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="43eba-129">Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-129">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="43eba-130">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="43eba-130">**DeleteEx**</span></span>](deleteex-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="43eba-131">Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="43eba-132">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="43eba-132">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-shortcutfile.md)           | <span data-ttu-id="43eba-133">Método de clase que determina si el llamador tiene los permisos agregados especificados por el argumento Permission no solo en el objeto File, sino en el recurso compartido en el que reside el archivo o directorio (si está en un recurso compartido).</span><span class="sxs-lookup"><span data-stu-id="43eba-133">Class method that determines whether the caller has the aggregated permissions specified by the Permission argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="43eba-134">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="43eba-134">**Rename**</span></span>](rename-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="43eba-135">Método de clase que cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-135">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="43eba-136">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="43eba-136">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-shortcutfile.md)                             | <span data-ttu-id="43eba-137">Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-137">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="43eba-138">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="43eba-138">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-shortcutfile.md)                         | <span data-ttu-id="43eba-139">Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="43eba-140">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="43eba-140">**Uncompress**</span></span>](uncompress-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="43eba-141">Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-141">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="43eba-142">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="43eba-142">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-shortcutfile.md)                               | <span data-ttu-id="43eba-143">Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="43eba-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43eba-144">Properties</span></span>

<span data-ttu-id="43eba-145">La **clase \_ ShortcutFile de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="43eba-145">The **Win32\_ShortcutFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43eba-146">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="43eba-146">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43eba-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-149">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("derechos de acceso")</span><span class="sxs-lookup"><span data-stu-id="43eba-149">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-150">Máscara de archivos que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-150">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="43eba-151">Para los valores de bit, consulte [**constantes de derechos de acceso a archivos y directorios**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-151">For bit values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="43eba-152">En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-152">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="43eba-153">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-153">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="43eba-154">**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="43eba-154">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="43eba-155">**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="43eba-155">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="43eba-156">**Archivo \_ de ANEXAr \_ datos (archivo) o archivo \_ agregar \_ subdirectorio (directorio)** (4)</span><span class="sxs-lookup"><span data-stu-id="43eba-156">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="43eba-157">**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="43eba-157">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="43eba-158">**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="43eba-158">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="43eba-159">**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="43eba-159">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="43eba-160">**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="43eba-160">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="43eba-161">**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="43eba-161">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="43eba-162">**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="43eba-162">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="43eba-163">**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="43eba-163">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="43eba-164">**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="43eba-164">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="43eba-165">**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="43eba-165">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="43eba-166">**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="43eba-166">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="43eba-167">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="43eba-167">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43eba-168">**Archivar**</span><span class="sxs-lookup"><span data-stu-id="43eba-168">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-169">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="43eba-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-171">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("se debe archivar")</span><span class="sxs-lookup"><span data-stu-id="43eba-171">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-172">Si **es true**, se debe archivar el archivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-172">If **True**, the file should be archived.</span></span>

<span data-ttu-id="43eba-173">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-173">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="43eba-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-177">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="43eba-177">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-178">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-178">A short textual description of the object.</span></span>

<span data-ttu-id="43eba-179">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-180">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="43eba-180">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-181">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="43eba-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-183">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("comprimido")</span><span class="sxs-lookup"><span data-stu-id="43eba-183">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-184">Si es **true**, el archivo se comprime.</span><span class="sxs-lookup"><span data-stu-id="43eba-184">If **True**, the file is compressed.</span></span>

<span data-ttu-id="43eba-185">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-185">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-186">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="43eba-186">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-189">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("método de compresión")</span><span class="sxs-lookup"><span data-stu-id="43eba-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-190">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="43eba-190">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="43eba-191">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="43eba-191">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="43eba-192">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="43eba-192">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="43eba-193">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="43eba-193">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="43eba-194">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-194">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="43eba-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-198">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="43eba-198">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-199">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="43eba-199">Name of the class.</span></span>

<span data-ttu-id="43eba-200">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-200">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-201">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="43eba-201">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-202">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43eba-202">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-204">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("fecha de creación")</span><span class="sxs-lookup"><span data-stu-id="43eba-204">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-205">Fecha y hora de creación del archivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-205">Date and time of the file's creation.</span></span>

<span data-ttu-id="43eba-206">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-206">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-207">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="43eba-207">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-210">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre de clase de sistema de equipo ")</span><span class="sxs-lookup"><span data-stu-id="43eba-210">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-211">Clase del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="43eba-211">Class of the computer system.</span></span>

<span data-ttu-id="43eba-212">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-213">**CSName**</span><span class="sxs-lookup"><span data-stu-id="43eba-213">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-216">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="43eba-216">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-217">Nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="43eba-217">Name of the computer system.</span></span>

<span data-ttu-id="43eba-218">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-219">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="43eba-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-220">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-222">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="43eba-222">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-223">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-223">A textual description of the object.</span></span>

<span data-ttu-id="43eba-224">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-225">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="43eba-225">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-226">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-228">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="43eba-228">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-229">Letra de unidad (incluidos los dos puntos que siguen a la letra de unidad) del archivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-229">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="43eba-230">Ejemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="43eba-230">Example: "c:"</span></span>

<span data-ttu-id="43eba-231">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-232">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="43eba-232">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-233">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-235">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de archivo de ocho puntos tres")</span><span class="sxs-lookup"><span data-stu-id="43eba-235">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-236">Nombre de archivo en formato 8,3.</span><span class="sxs-lookup"><span data-stu-id="43eba-236">File name in 8.3 format.</span></span>

<span data-ttu-id="43eba-237">Ejemplo: "c: \\ programa ~ 1"</span><span class="sxs-lookup"><span data-stu-id="43eba-237">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="43eba-238">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-238">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-239">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="43eba-239">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-240">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="43eba-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-242">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cifrado")</span><span class="sxs-lookup"><span data-stu-id="43eba-242">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-243">Si es **true**, el archivo está cifrado.</span><span class="sxs-lookup"><span data-stu-id="43eba-243">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="43eba-244">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-244">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-245">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="43eba-245">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-248">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("método de cifrado")</span><span class="sxs-lookup"><span data-stu-id="43eba-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-249">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="43eba-249">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="43eba-250">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="43eba-250">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="43eba-251">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="43eba-251">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="43eba-252">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="43eba-252">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="43eba-253">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-254">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="43eba-254">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-257">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("extensión de archivo")</span><span class="sxs-lookup"><span data-stu-id="43eba-257">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-258">Extensión de nombre de archivo sin el punto anterior (punto).</span><span class="sxs-lookup"><span data-stu-id="43eba-258">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="43eba-259">Ejemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="43eba-259">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="43eba-260">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-261">**FileName**</span><span class="sxs-lookup"><span data-stu-id="43eba-261">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-262">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-264">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de archivo")</span><span class="sxs-lookup"><span data-stu-id="43eba-264">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-265">Nombre de archivo sin la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-265">File name without the file name extension.</span></span>

<span data-ttu-id="43eba-266">Ejemplo: "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="43eba-266">Example: "MyDataFile"</span></span>

<span data-ttu-id="43eba-267">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-267">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-268">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="43eba-268">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-269">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="43eba-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-271">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("size"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="43eba-271">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-272">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="43eba-272">Size of the file, in bytes.</span></span>

<span data-ttu-id="43eba-273">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-273">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="43eba-274">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-274">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-275">**FileType**</span><span class="sxs-lookup"><span data-stu-id="43eba-275">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-278">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("tipo de archivo")</span><span class="sxs-lookup"><span data-stu-id="43eba-278">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-279">Descriptor que representa el tipo de archivo indicado por la propiedad de **extensión** .</span><span class="sxs-lookup"><span data-stu-id="43eba-279">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="43eba-280">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-280">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="43eba-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-284">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre de clase del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="43eba-284">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-285">Clase del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="43eba-285">Class of the file system.</span></span>

<span data-ttu-id="43eba-286">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-287">**FSName**</span><span class="sxs-lookup"><span data-stu-id="43eba-287">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-290">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="43eba-290">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-291">Nombre del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="43eba-291">Name of the file system.</span></span>

<span data-ttu-id="43eba-292">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-293">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="43eba-293">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-294">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="43eba-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-296">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="43eba-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-297">Si es **true**, el archivo está oculto.</span><span class="sxs-lookup"><span data-stu-id="43eba-297">If **True**, the file is hidden.</span></span>

<span data-ttu-id="43eba-298">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-299">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="43eba-299">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-300">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43eba-300">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-302">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="43eba-302">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-303">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-303">Indicates when the object was installed.</span></span> <span data-ttu-id="43eba-304">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="43eba-304">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="43eba-305">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-306">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="43eba-306">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-307">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="43eba-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-309">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("recuento de apertura de archivos actuales")</span><span class="sxs-lookup"><span data-stu-id="43eba-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-310">Número de "archivos abiertos" que están activos actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-310">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="43eba-311">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-311">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="43eba-312">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-312">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-313">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="43eba-313">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-314">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43eba-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-316">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("último acceso")</span><span class="sxs-lookup"><span data-stu-id="43eba-316">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-317">Fecha y hora en que se produjo el último acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-317">Date and time the file was last accessed.</span></span>

<span data-ttu-id="43eba-318">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-318">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-319">**Última**</span><span class="sxs-lookup"><span data-stu-id="43eba-319">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-320">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43eba-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-322">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("última modificación")</span><span class="sxs-lookup"><span data-stu-id="43eba-322">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-323">Fecha y hora en que se modificó el archivo por última vez.</span><span class="sxs-lookup"><span data-stu-id="43eba-323">Date and time the file was last modified.</span></span>

<span data-ttu-id="43eba-324">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-324">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-325">**Le**</span><span class="sxs-lookup"><span data-stu-id="43eba-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-328">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("manufacturer")</span><span class="sxs-lookup"><span data-stu-id="43eba-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-329">Cadena del fabricante del recurso de versión (si está presente).</span><span class="sxs-lookup"><span data-stu-id="43eba-329">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="43eba-330">Esta propiedad se hereda del [**\_ archivo**](cim-datafile.md)de propiedades CIM.</span><span class="sxs-lookup"><span data-stu-id="43eba-330">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-331">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="43eba-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-332">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-334">Calificadores: [ **clave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="43eba-334">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="43eba-335">La propiedad Name es una cadena que representa el nombre heredado que actúa como clave de una instancia de archivo lógico dentro de un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="43eba-335">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="43eba-336">Se deben proporcionar los nombres de ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="43eba-336">Full path names should be provided.</span></span>

<span data-ttu-id="43eba-337">Ejemplo: C: \\ Windows \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="43eba-337">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="43eba-338">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-339">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="43eba-339">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-342">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("path")</span><span class="sxs-lookup"><span data-stu-id="43eba-342">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-343">Ruta de acceso del archivo, incluidas las barras diagonales inversas iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="43eba-343">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="43eba-344">Ejemplo: " \\ sistema de Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="43eba-344">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="43eba-345">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-345">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-346">**Puedan**</span><span class="sxs-lookup"><span data-stu-id="43eba-346">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-347">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="43eba-347">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-349">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("legible")</span><span class="sxs-lookup"><span data-stu-id="43eba-349">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-350">Si **es true**, se puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-350">If **True**, the file can be read.</span></span>

<span data-ttu-id="43eba-351">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-352">**Estado**</span><span class="sxs-lookup"><span data-stu-id="43eba-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-355">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="43eba-355">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-356">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="43eba-356">String that indicates the current status of the object.</span></span> <span data-ttu-id="43eba-357">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="43eba-357">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="43eba-358">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="43eba-358">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="43eba-359">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="43eba-359">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="43eba-360">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="43eba-360">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="43eba-361">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="43eba-361">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="43eba-362">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="43eba-362">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="43eba-363">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-363">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="43eba-364">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="43eba-364">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="43eba-365">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="43eba-365">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="43eba-366">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="43eba-366">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="43eba-367">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="43eba-367">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43eba-368">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="43eba-368">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="43eba-369">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="43eba-369">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="43eba-370">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="43eba-370">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="43eba-371">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="43eba-371">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="43eba-372">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="43eba-372">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="43eba-373">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="43eba-373">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="43eba-374">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="43eba-374">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="43eba-375">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="43eba-375">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="43eba-376">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="43eba-376">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43eba-377">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="43eba-377">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-378">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="43eba-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-379">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-380">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("archivo del sistema")</span><span class="sxs-lookup"><span data-stu-id="43eba-380">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-381">Si es **true**, el archivo es un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="43eba-381">If **True**, the file is a system file.</span></span>

<span data-ttu-id="43eba-382">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-383">**Target**</span><span class="sxs-lookup"><span data-stu-id="43eba-383">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-384">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-386">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| \_ beginthreadex")</span><span class="sxs-lookup"><span data-stu-id="43eba-386">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|\_beginthreadex")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-387">Nombre del objeto al que se va a hacer un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="43eba-387">Name of the object that this is a shortcut to.</span></span>

</dd> <dt>

<span data-ttu-id="43eba-388">**Versión**</span><span class="sxs-lookup"><span data-stu-id="43eba-388">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-389">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="43eba-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-391">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("versión")</span><span class="sxs-lookup"><span data-stu-id="43eba-391">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-392">Cadena de versión del recurso de versión (si está presente).</span><span class="sxs-lookup"><span data-stu-id="43eba-392">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="43eba-393">Esta propiedad se hereda del [**\_ archivo**](cim-datafile.md)de propiedades CIM.</span><span class="sxs-lookup"><span data-stu-id="43eba-393">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="43eba-394">**Writeable (Grabable)**</span><span class="sxs-lookup"><span data-stu-id="43eba-394">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43eba-395">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="43eba-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43eba-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43eba-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43eba-397">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("grabable")</span><span class="sxs-lookup"><span data-stu-id="43eba-397">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="43eba-398">Si **es true**, se puede escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-398">If **True**, the file can be written.</span></span>

<span data-ttu-id="43eba-399">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43eba-400">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43eba-400">Remarks</span></span>

<span data-ttu-id="43eba-401">La **clase \_ ShortcutFile de Win32** se deriva [**del \_ archivo de archivos CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-401">The **Win32\_ShortcutFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43eba-402">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43eba-402">Requirements</span></span>



| <span data-ttu-id="43eba-403">Requisito</span><span class="sxs-lookup"><span data-stu-id="43eba-403">Requirement</span></span> | <span data-ttu-id="43eba-404">Value</span><span class="sxs-lookup"><span data-stu-id="43eba-404">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43eba-405">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43eba-405">Minimum supported client</span></span><br/> | <span data-ttu-id="43eba-406">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43eba-406">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43eba-407">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43eba-407">Minimum supported server</span></span><br/> | <span data-ttu-id="43eba-408">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43eba-408">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43eba-409">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="43eba-409">Namespace</span></span><br/>                | <span data-ttu-id="43eba-410">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="43eba-410">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43eba-411">MOF</span><span class="sxs-lookup"><span data-stu-id="43eba-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43eba-412"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43eba-412"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43eba-413">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="43eba-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43eba-414"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43eba-414"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43eba-415">Vea también</span><span class="sxs-lookup"><span data-stu-id="43eba-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43eba-416">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="43eba-416">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="43eba-417">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="43eba-417">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
