---
description: El archivo de \_ paginación de Win32&\# 32; La clase WMI representa el archivo usado para controlar el intercambio de archivos de memoria virtual en un sistema Win32. Esta clase está en desuso.
ms.assetid: 5599d09d-a2fd-4217-8560-5fd56f09d47b
ms.tgt_platform: multiple
title: Win32_PageFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile
- Win32_PageFile.Caption
- Win32_PageFile.Description
- Win32_PageFile.InstallDate
- Win32_PageFile.Archive
- Win32_PageFile.Compressed
- Win32_PageFile.CompressionMethod
- Win32_PageFile.CreationClassName
- Win32_PageFile.CreationDate
- Win32_PageFile.CSCreationClassName
- Win32_PageFile.CSName
- Win32_PageFile.Drive
- Win32_PageFile.EightDotThreeFileName
- Win32_PageFile.Encrypted
- Win32_PageFile.EncryptionMethod
- Win32_PageFile.Extension
- Win32_PageFile.FileName
- Win32_PageFile.FileSize
- Win32_PageFile.FileType
- Win32_PageFile.FSCreationClassName
- Win32_PageFile.FSName
- Win32_PageFile.Hidden
- Win32_PageFile.InUseCount
- Win32_PageFile.LastAccessed
- Win32_PageFile.LastModified
- Win32_PageFile.Path
- Win32_PageFile.Readable
- Win32_PageFile.System
- Win32_PageFile.Writeable
- Win32_PageFile.AccessMask
- Win32_PageFile.Manufacturer
- Win32_PageFile.Status
- Win32_PageFile.Version
- Win32_PageFile.FreeSpace
- Win32_PageFile.InitialSize
- Win32_PageFile.MaximumSize
- Win32_PageFile.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb63c4242ae8fa3cca5133a25d2742d07210ca1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659697"
---
# <a name="win32_pagefile-class"></a><span data-ttu-id="14fca-104">Clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="14fca-104">Win32\_PageFile class</span></span>

<span data-ttu-id="14fca-105">La [clase WMI](../wmisdk/retrieving-a-class.md) de archivo de **\_ paginación de Win32** representa el archivo usado para controlar el intercambio de archivos de memoria virtual en un sistema Win32.</span><span class="sxs-lookup"><span data-stu-id="14fca-105">The **Win32\_PageFile** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="14fca-106">Esta clase está en desuso.</span><span class="sxs-lookup"><span data-stu-id="14fca-106">This class has been deprecated.</span></span>

<span data-ttu-id="14fca-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="14fca-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="14fca-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="14fca-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="14fca-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14fca-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{8502C4C6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
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
  uint32   AccessMask;
  string   Manufacturer;
  string   Status;
  string   Version;
  uint32   FreeSpace;
  uint32   InitialSize;
  uint32   MaximumSize;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="14fca-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="14fca-110">Members</span></span>

<span data-ttu-id="14fca-111">La clase de archivo de **\_ paginación Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="14fca-111">The **Win32\_PageFile** class has these types of members:</span></span>

-   [<span data-ttu-id="14fca-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="14fca-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="14fca-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14fca-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="14fca-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="14fca-114">Methods</span></span>

<span data-ttu-id="14fca-115">La clase de archivo de **\_ paginación Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="14fca-115">The **Win32\_PageFile** class has these methods.</span></span>



| <span data-ttu-id="14fca-116">Método</span><span class="sxs-lookup"><span data-stu-id="14fca-116">Method</span></span>                                                                                            | <span data-ttu-id="14fca-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="14fca-117">Description</span></span>                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14fca-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="14fca-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-pagefile.md)     | <span data-ttu-id="14fca-119">Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="14fca-120">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="14fca-120">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | <span data-ttu-id="14fca-121">Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-121">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="14fca-122">**Comprimir**</span><span class="sxs-lookup"><span data-stu-id="14fca-122">**Compress**</span></span>](compress-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="14fca-123">Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="14fca-124">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="14fca-124">**CompressEx**</span></span>](compressex-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="14fca-125">Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-125">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="14fca-126">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="14fca-126">**Copy**</span></span>](copy-method-in-class-win32-pagefile.md)                                               | <span data-ttu-id="14fca-127">Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="14fca-127">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                       |
| [<span data-ttu-id="14fca-128">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="14fca-128">**CopyEx**</span></span>](copyex-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="14fca-129">Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName.</span><span class="sxs-lookup"><span data-stu-id="14fca-129">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                                    |
| [<span data-ttu-id="14fca-130">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="14fca-130">**Delete**</span></span>](delete-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="14fca-131">Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="14fca-132">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="14fca-132">**DeleteEx**</span></span>](deleteex-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="14fca-133">Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-133">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="14fca-134">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="14fca-134">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-pagefile.md)           | <span data-ttu-id="14fca-135">Método de clase que determina si el llamador tiene los permisos agregados especificados por el argumento *Permission* no solo en el objeto File, sino en el recurso compartido en el que reside el archivo o directorio (si está en un recurso compartido).</span><span class="sxs-lookup"><span data-stu-id="14fca-135">Class method that determines whether the caller has the aggregated permissions specified by the *Permission* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="14fca-136">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="14fca-136">**Rename**</span></span>](rename-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="14fca-137">Método de clase que cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-137">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="14fca-138">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="14fca-138">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-pagefile.md)                             | <span data-ttu-id="14fca-139">Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="14fca-140">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="14fca-140">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-pagefile.md)                         | <span data-ttu-id="14fca-141">Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-141">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="14fca-142">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="14fca-142">**Uncompress**</span></span>](uncompress-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="14fca-143">Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="14fca-144">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="14fca-144">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-pagefile.md)                               | <span data-ttu-id="14fca-145">Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-145">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="14fca-146">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14fca-146">Properties</span></span>

<span data-ttu-id="14fca-147">La clase de archivo de **\_ paginación Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="14fca-147">The **Win32\_PageFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14fca-148">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="14fca-148">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14fca-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-151">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("derechos de acceso")</span><span class="sxs-lookup"><span data-stu-id="14fca-151">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-152">Máscara de archivos que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="14fca-152">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="14fca-153">Para ver los valores, consulte [**constantes de derechos de acceso a archivos y directorios**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-153">For values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

<span data-ttu-id="14fca-154">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-154">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="14fca-155">**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="14fca-155">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="14fca-156">**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="14fca-156">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="14fca-157">**Archivo \_ de ANEXAr \_ datos (archivo) o archivo \_ agregar \_ subdirectorio (directorio)** (4)</span><span class="sxs-lookup"><span data-stu-id="14fca-157">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="14fca-158">**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="14fca-158">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="14fca-159">**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="14fca-159">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="14fca-160">**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="14fca-160">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="14fca-161">**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="14fca-161">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="14fca-162">**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="14fca-162">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="14fca-163">**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="14fca-163">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="14fca-164">**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="14fca-164">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="14fca-165">**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="14fca-165">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="14fca-166">**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="14fca-166">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="14fca-167">**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="14fca-167">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="14fca-168">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="14fca-168">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14fca-169">**Archivar**</span><span class="sxs-lookup"><span data-stu-id="14fca-169">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-170">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14fca-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-172">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("se debe archivar")</span><span class="sxs-lookup"><span data-stu-id="14fca-172">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-173">Si **es true**, se debe archivar el archivo.</span><span class="sxs-lookup"><span data-stu-id="14fca-173">If **True**, the file should be archived.</span></span>

<span data-ttu-id="14fca-174">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-174">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="14fca-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-178">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="14fca-178">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-179">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-179">A short textual description of the object.</span></span>

<span data-ttu-id="14fca-180">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-181">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="14fca-181">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-182">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14fca-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-184">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("comprimido")</span><span class="sxs-lookup"><span data-stu-id="14fca-184">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-185">Si es **true**, el archivo se comprime.</span><span class="sxs-lookup"><span data-stu-id="14fca-185">If **True**, the file is compressed.</span></span>

<span data-ttu-id="14fca-186">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-186">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-187">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="14fca-187">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-190">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("método de compresión")</span><span class="sxs-lookup"><span data-stu-id="14fca-190">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-191">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="14fca-191">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="14fca-192">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="14fca-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="14fca-193">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="14fca-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="14fca-194">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="14fca-194">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="14fca-195">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="14fca-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-199">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="14fca-199">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-200">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="14fca-200">Name of the class.</span></span>

<span data-ttu-id="14fca-201">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-202">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="14fca-202">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-203">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="14fca-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-205">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("fecha de creación")</span><span class="sxs-lookup"><span data-stu-id="14fca-205">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-206">Fecha y hora de creación del archivo.</span><span class="sxs-lookup"><span data-stu-id="14fca-206">Date and time of the file's creation.</span></span>

<span data-ttu-id="14fca-207">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-207">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-208">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="14fca-208">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-211">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre de clase de sistema de equipo ")</span><span class="sxs-lookup"><span data-stu-id="14fca-211">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-212">Clase del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="14fca-212">Class of the computer system.</span></span>

<span data-ttu-id="14fca-213">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-213">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-214">**CSName**</span><span class="sxs-lookup"><span data-stu-id="14fca-214">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-217">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="14fca-217">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-218">Nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="14fca-218">Name of the computer system.</span></span>

<span data-ttu-id="14fca-219">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-220">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="14fca-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-223">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="14fca-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-224">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-224">A textual description of the object.</span></span>

<span data-ttu-id="14fca-225">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-226">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="14fca-226">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-229">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="14fca-229">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-230">Letra de unidad (incluidos los dos puntos que siguen a la letra de unidad) del archivo.</span><span class="sxs-lookup"><span data-stu-id="14fca-230">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="14fca-231">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="14fca-232">Ejemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="14fca-232">Example: "c:"</span></span>

<span data-ttu-id="14fca-233">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-234">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="14fca-234">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-237">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de archivo de ocho puntos tres")</span><span class="sxs-lookup"><span data-stu-id="14fca-237">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-238">Nombre de archivo compatible con DOS.</span><span class="sxs-lookup"><span data-stu-id="14fca-238">DOS-compatible file name.</span></span>

<span data-ttu-id="14fca-239">Ejemplo: "c: \\ programa ~ 1"</span><span class="sxs-lookup"><span data-stu-id="14fca-239">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="14fca-240">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-240">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-241">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="14fca-241">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-242">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14fca-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-244">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cifrado")</span><span class="sxs-lookup"><span data-stu-id="14fca-244">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-245">Si es **true**, el archivo está cifrado.</span><span class="sxs-lookup"><span data-stu-id="14fca-245">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="14fca-246">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-247">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="14fca-247">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-250">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("método de cifrado")</span><span class="sxs-lookup"><span data-stu-id="14fca-250">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-251">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="14fca-251">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="14fca-252">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="14fca-252">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="14fca-253">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="14fca-253">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="14fca-254">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="14fca-254">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="14fca-255">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-256">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="14fca-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-259">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("extensión de archivo")</span><span class="sxs-lookup"><span data-stu-id="14fca-259">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-260">Extensión de nombre de archivo sin el punto anterior (punto).</span><span class="sxs-lookup"><span data-stu-id="14fca-260">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="14fca-261">Ejemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="14fca-261">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="14fca-262">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="14fca-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-266">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de archivo")</span><span class="sxs-lookup"><span data-stu-id="14fca-266">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-267">Nombre de archivo sin la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="14fca-267">File name without the file name extension.</span></span> <span data-ttu-id="14fca-268">Ejemplo: "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="14fca-268">Example: "MyDataFile"</span></span>

<span data-ttu-id="14fca-269">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="14fca-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-271">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="14fca-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-273">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("size"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="14fca-273">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-274">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="14fca-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="14fca-275">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="14fca-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="14fca-276">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-276">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="14fca-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-280">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("tipo de archivo")</span><span class="sxs-lookup"><span data-stu-id="14fca-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-281">Descriptor que representa el tipo de archivo indicado por la propiedad de **extensión** .</span><span class="sxs-lookup"><span data-stu-id="14fca-281">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="14fca-282">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-283">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="14fca-283">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-284">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14fca-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-286">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estructuras de administración de memoria inesperados win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwAvailPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="14fca-286">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwAvailPageFile"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-287">Espacio disponible en el archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="14fca-287">Space available in the paging file.</span></span> <span data-ttu-id="14fca-288">El sistema operativo puede aumentar el archivo de paginación según sea necesario, hasta el límite impuesto por el usuario.</span><span class="sxs-lookup"><span data-stu-id="14fca-288">The operating system can enlarge the paging file as necessary, up to the limit imposed by the user.</span></span> <span data-ttu-id="14fca-289">Esta propiedad muestra la diferencia entre el tamaño de la memoria asignada actual y el tamaño actual del archivo de paginación; no muestra el mayor tamaño posible del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="14fca-289">This property shows the difference between the size of current committed memory and the current size of the paging file; it does not show the largest possible size of the paging file.</span></span>

</dd> <dt>

<span data-ttu-id="14fca-290">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="14fca-290">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-291">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-293">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre de clase del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="14fca-293">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-294">Clase del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="14fca-294">Class of the file system.</span></span>

<span data-ttu-id="14fca-295">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-295">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-296">**FSName**</span><span class="sxs-lookup"><span data-stu-id="14fca-296">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-299">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="14fca-299">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-300">Nombre del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="14fca-300">Name of the file system.</span></span>

<span data-ttu-id="14fca-301">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-302">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="14fca-302">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-303">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14fca-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-305">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="14fca-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-306">Si es **true**, el archivo está oculto.</span><span class="sxs-lookup"><span data-stu-id="14fca-306">If **True**, the file is hidden.</span></span>

<span data-ttu-id="14fca-307">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-307">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-308">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="14fca-308">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-309">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14fca-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-311">Calificadores: [**desusado**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Administración \| de memoria PagingFiles"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="14fca-311">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-312">Tamaño inicial del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="14fca-312">Initial size of the page file.</span></span>

</dd> <dt>

<span data-ttu-id="14fca-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="14fca-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-314">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="14fca-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-316">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="14fca-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-317">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-317">Indicates when the object was installed.</span></span> <span data-ttu-id="14fca-318">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="14fca-318">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="14fca-319">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-320">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="14fca-320">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-321">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="14fca-321">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-323">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("recuento de apertura de archivos actuales")</span><span class="sxs-lookup"><span data-stu-id="14fca-323">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-324">Número de "archivos abiertos" que están activos actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="14fca-324">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="14fca-325">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="14fca-325">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="14fca-326">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-326">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-327">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="14fca-327">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-328">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="14fca-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-330">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("último acceso")</span><span class="sxs-lookup"><span data-stu-id="14fca-330">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-331">Fecha y hora en que se produjo el último acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="14fca-331">Date and time the file was last accessed.</span></span>

<span data-ttu-id="14fca-332">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-332">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-333">**Última**</span><span class="sxs-lookup"><span data-stu-id="14fca-333">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-334">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="14fca-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-336">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("última modificación")</span><span class="sxs-lookup"><span data-stu-id="14fca-336">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-337">Fecha y hora en que se modificó el archivo por última vez.</span><span class="sxs-lookup"><span data-stu-id="14fca-337">Date and time the file was last modified.</span></span>

<span data-ttu-id="14fca-338">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-339">**Le**</span><span class="sxs-lookup"><span data-stu-id="14fca-339">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-342">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("manufacturer")</span><span class="sxs-lookup"><span data-stu-id="14fca-342">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-343">Cadena del fabricante del recurso de versión (si está presente).</span><span class="sxs-lookup"><span data-stu-id="14fca-343">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="14fca-344">Esta propiedad se hereda del [**\_ archivo**](cim-datafile.md)de propiedades CIM.</span><span class="sxs-lookup"><span data-stu-id="14fca-344">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-345">**Tamañomáximo**</span><span class="sxs-lookup"><span data-stu-id="14fca-345">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-346">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14fca-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-348">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estructuras de administración de memoria inesperados win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="14fca-348">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-349">Tamaño máximo del archivo de paginación establecido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="14fca-349">Maximum size of the page file as set by the user.</span></span> <span data-ttu-id="14fca-350">El sistema operativo no permitirá que el archivo de paginación supere este límite.</span><span class="sxs-lookup"><span data-stu-id="14fca-350">The operating system will not allow the page file to exceed this limit.</span></span>

</dd> <dt>

<span data-ttu-id="14fca-351">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="14fca-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-354">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemPageFileInformation \| PageFileName")</span><span class="sxs-lookup"><span data-stu-id="14fca-354">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemPageFileInformation\|PageFileName")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-355">Nombre del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="14fca-355">Name of the page file.</span></span>

<span data-ttu-id="14fca-356">Ejemplo: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="14fca-356">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="14fca-357">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="14fca-357">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-360">Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("path")</span><span class="sxs-lookup"><span data-stu-id="14fca-360">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-361">Ruta de acceso del archivo, incluidas las barras diagonales inversas iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="14fca-361">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="14fca-362">Ejemplo: " \\ sistema de Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="14fca-362">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="14fca-363">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-363">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-364">**Puedan**</span><span class="sxs-lookup"><span data-stu-id="14fca-364">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-365">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14fca-365">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-367">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("legible")</span><span class="sxs-lookup"><span data-stu-id="14fca-367">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-368">Si **es true**, se puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="14fca-368">If **True**, the file can be read.</span></span>

<span data-ttu-id="14fca-369">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-369">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-370">**Estado**</span><span class="sxs-lookup"><span data-stu-id="14fca-370">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-371">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-373">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="14fca-373">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-374">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="14fca-374">String that indicates the current status of the object.</span></span>

<span data-ttu-id="14fca-375">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="14fca-376">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="14fca-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="14fca-377">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="14fca-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="14fca-378">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="14fca-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="14fca-379">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="14fca-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14fca-380">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="14fca-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="14fca-381">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="14fca-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="14fca-382">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="14fca-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="14fca-383">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="14fca-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="14fca-384">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="14fca-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="14fca-385">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="14fca-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="14fca-386">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="14fca-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="14fca-387">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="14fca-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="14fca-388">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="14fca-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14fca-389">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="14fca-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-390">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14fca-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-392">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("archivo del sistema")</span><span class="sxs-lookup"><span data-stu-id="14fca-392">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-393">Si es **true**, el archivo es un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="14fca-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="14fca-394">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-395">**Versión**</span><span class="sxs-lookup"><span data-stu-id="14fca-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-396">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14fca-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-398">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("versión")</span><span class="sxs-lookup"><span data-stu-id="14fca-398">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-399">Cadena de versión del recurso de versión (si está presente).</span><span class="sxs-lookup"><span data-stu-id="14fca-399">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="14fca-400">Esta propiedad se hereda del [**\_ archivo**](cim-datafile.md)de propiedades CIM.</span><span class="sxs-lookup"><span data-stu-id="14fca-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14fca-401">**Writeable (Grabable)**</span><span class="sxs-lookup"><span data-stu-id="14fca-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14fca-402">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14fca-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14fca-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14fca-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14fca-404">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("grabable")</span><span class="sxs-lookup"><span data-stu-id="14fca-404">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="14fca-405">Si **es true**, se puede escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="14fca-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="14fca-406">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14fca-407">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14fca-407">Remarks</span></span>

<span data-ttu-id="14fca-408">La clase de archivo de **\_ paginación Win32** se deriva del [**\_ directorio CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="14fca-408">The **Win32\_PageFile** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="14fca-409">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="14fca-409">Examples</span></span>

<span data-ttu-id="14fca-410">En el ejemplo de código de VBScript siguiente se muestra cómo recuperar estadísticas de archivo de paginación desde instancias del archivo de **\_ paginación de Win32**.</span><span class="sxs-lookup"><span data-stu-id="14fca-410">The following VBScript code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



<span data-ttu-id="14fca-411">En el ejemplo de código Perl siguiente se muestra cómo recuperar estadísticas del archivo de paginación desde instancias del archivo de **\_ paginación de Win32**.</span><span class="sxs-lookup"><span data-stu-id="14fca-411">The following Perl code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```
use strict;
use Win32::OLE;

my $PageFileSet;

eval { $PageFileSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 InstancesOf ("Win32_PageFile"); };
if (!$@ && defined $PageFileSet)
{
 foreach my $PageFileInst (in $PageFileSet)
 {
  print "\n$PageFileInst->{Name}\n";
  print " Initial: $PageFileInst->{InitialSize} MB\n";
  print " Maximum: $PageFileInst->{MaximumSize} MB\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="14fca-412">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14fca-412">Requirements</span></span>



| <span data-ttu-id="14fca-413">Requisito</span><span class="sxs-lookup"><span data-stu-id="14fca-413">Requirement</span></span> | <span data-ttu-id="14fca-414">Value</span><span class="sxs-lookup"><span data-stu-id="14fca-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14fca-415">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14fca-415">Minimum supported client</span></span><br/> | <span data-ttu-id="14fca-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14fca-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="14fca-417">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14fca-417">Minimum supported server</span></span><br/> | <span data-ttu-id="14fca-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14fca-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="14fca-419">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="14fca-419">Namespace</span></span><br/>                | <span data-ttu-id="14fca-420">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="14fca-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="14fca-421">MOF</span><span class="sxs-lookup"><span data-stu-id="14fca-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14fca-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14fca-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="14fca-423">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14fca-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14fca-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14fca-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14fca-425">Vea también</span><span class="sxs-lookup"><span data-stu-id="14fca-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14fca-426">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="14fca-426">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="14fca-427">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="14fca-427">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
