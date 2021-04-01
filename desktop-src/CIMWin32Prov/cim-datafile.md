---
description: La \_ clase de archivo de datos CIM representa una colección con nombre de datos o código ejecutable. Solo se devolverán las instancias de los archivos de los discos fijos locales.
ms.assetid: e90e1216-e943-4f3a-9f6c-8a0b4568a11f
ms.tgt_platform: multiple
title: CIM_DataFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile
- CIM_DataFile.Caption
- CIM_DataFile.Description
- CIM_DataFile.InstallDate
- CIM_DataFile.Status
- CIM_DataFile.AccessMask
- CIM_DataFile.Archive
- CIM_DataFile.Compressed
- CIM_DataFile.CompressionMethod
- CIM_DataFile.CreationClassName
- CIM_DataFile.CreationDate
- CIM_DataFile.CSCreationClassName
- CIM_DataFile.CSName
- CIM_DataFile.Drive
- CIM_DataFile.EightDotThreeFileName
- CIM_DataFile.Encrypted
- CIM_DataFile.EncryptionMethod
- CIM_DataFile.Name
- CIM_DataFile.Extension
- CIM_DataFile.FileName
- CIM_DataFile.FileSize
- CIM_DataFile.FileType
- CIM_DataFile.FSCreationClassName
- CIM_DataFile.FSName
- CIM_DataFile.Hidden
- CIM_DataFile.InUseCount
- CIM_DataFile.LastAccessed
- CIM_DataFile.LastModified
- CIM_DataFile.Path
- CIM_DataFile.Readable
- CIM_DataFile.System
- CIM_DataFile.Writeable
- CIM_DataFile.Manufacturer
- CIM_DataFile.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0badba05eafa5cba06e48b8494ca893936af360e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907302"
---
# <a name="cim_datafile-class"></a><span data-ttu-id="77a70-104">CIM ( \_ clase de archivo de archivos)</span><span class="sxs-lookup"><span data-stu-id="77a70-104">CIM\_DataFile class</span></span>

<span data-ttu-id="77a70-105">La clase de **\_ archivo** de datos CIM representa una colección con nombre de datos o código ejecutable.</span><span class="sxs-lookup"><span data-stu-id="77a70-105">The **CIM\_DataFile** class represents a named collection of data or executable code.</span></span> <span data-ttu-id="77a70-106">Solo se devolverán las instancias de los archivos de los discos fijos locales.</span><span class="sxs-lookup"><span data-stu-id="77a70-106">Only instances of files on local fixed disks will be returned.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77a70-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="77a70-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="77a70-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="77a70-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="77a70-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="77a70-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="77a70-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a70-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77a70-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C55A-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("All Files (CIM)"), AMENDMENT]
class CIM_DataFile : CIM_LogicalFile
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
};
```

## <a name="members"></a><span data-ttu-id="77a70-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="77a70-112">Members</span></span>

<span data-ttu-id="77a70-113">La clase de **\_ archivo de archivos CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="77a70-113">The **CIM\_DataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="77a70-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="77a70-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="77a70-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="77a70-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="77a70-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="77a70-116">Methods</span></span>

<span data-ttu-id="77a70-117">La clase de **\_ archivo de archivos CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="77a70-117">The **CIM\_DataFile** class has these methods.</span></span>



| <span data-ttu-id="77a70-118">Método</span><span class="sxs-lookup"><span data-stu-id="77a70-118">Method</span></span>                                                                                          | <span data-ttu-id="77a70-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="77a70-119">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77a70-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="77a70-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)     | <span data-ttu-id="77a70-121">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="77a70-122">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-122">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="77a70-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="77a70-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md) | <span data-ttu-id="77a70-124">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="77a70-125">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-125">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="77a70-126">**Comprimir**</span><span class="sxs-lookup"><span data-stu-id="77a70-126">**Compress**</span></span>](compress-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="77a70-127">Usa la compresión NTFS para comprimir el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-127">Uses NTFS compression to compress the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="77a70-128">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-128">Implemented by WMI.</span></span><br/>                       |
| [<span data-ttu-id="77a70-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="77a70-129">**CompressEx**</span></span>](compressex-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="77a70-130">Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="77a70-131">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-131">Implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="77a70-132">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="77a70-132">**Copy**</span></span>](copy-method-in-class-cim-datafile.md)                                               | <span data-ttu-id="77a70-133">Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="77a70-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="77a70-134">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-134">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="77a70-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="77a70-135">**CopyEx**</span></span>](copyex-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="77a70-136">Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="77a70-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="77a70-137">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-137">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="77a70-138">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="77a70-138">**Delete**</span></span>](delete-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="77a70-139">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="77a70-140">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-140">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="77a70-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="77a70-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="77a70-142">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="77a70-143">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-143">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="77a70-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="77a70-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-datafile.md)           | <span data-ttu-id="77a70-145">Determina si el llamador tiene los permisos agregados especificados por el argumento de **permiso** .</span><span class="sxs-lookup"><span data-stu-id="77a70-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="77a70-146">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-146">Implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="77a70-147">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="77a70-147">**Rename**</span></span>](rename-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="77a70-148">Cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="77a70-149">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-149">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="77a70-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="77a70-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-datafile.md)                             | <span data-ttu-id="77a70-151">Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="77a70-152">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-152">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="77a70-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="77a70-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-datafile.md)                         | <span data-ttu-id="77a70-154">Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="77a70-155">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-155">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="77a70-156">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="77a70-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="77a70-157">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="77a70-158">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-158">Implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="77a70-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="77a70-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-datafile.md)                               | <span data-ttu-id="77a70-160">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="77a70-161">Implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="77a70-161">Implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="77a70-162">Propiedades</span><span class="sxs-lookup"><span data-stu-id="77a70-162">Properties</span></span>

<span data-ttu-id="77a70-163">La clase de **\_ archivo de archivos CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="77a70-163">The **CIM\_DataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77a70-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="77a70-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a70-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-167">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("derechos de acceso")</span><span class="sxs-lookup"><span data-stu-id="77a70-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-168">Máscara de archivos que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-168">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="77a70-169">Para los valores de bit, consulte [**constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="77a70-169">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="77a70-170">En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-170">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="77a70-171">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-171">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="77a70-172">**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="77a70-172">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="77a70-173">**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="77a70-173">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="77a70-174">**Archivo \_ de ANEXAr \_ datos (archivo) o archivo \_ agregar \_ subdirectorio (directorio)** (4)</span><span class="sxs-lookup"><span data-stu-id="77a70-174">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="77a70-175">**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="77a70-175">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="77a70-176">**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="77a70-176">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="77a70-177">**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="77a70-177">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="77a70-178">**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="77a70-178">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="77a70-179">**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="77a70-179">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="77a70-180">**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="77a70-180">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="77a70-181">**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="77a70-181">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="77a70-182">**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="77a70-182">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="77a70-183">**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="77a70-183">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="77a70-184">**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="77a70-184">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="77a70-185">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="77a70-185">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="77a70-186">**Archivar**</span><span class="sxs-lookup"><span data-stu-id="77a70-186">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-187">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="77a70-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-189">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("se debe archivar")</span><span class="sxs-lookup"><span data-stu-id="77a70-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-190">Si **es true**, se debe archivar el archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-190">If **True**, the file should be archived.</span></span>

<span data-ttu-id="77a70-191">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-191">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-192">**Caption**</span><span class="sxs-lookup"><span data-stu-id="77a70-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-195">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="77a70-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-196">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-196">A short textual description of the object.</span></span>

<span data-ttu-id="77a70-197">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-198">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="77a70-198">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-199">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="77a70-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-201">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("comprimido")</span><span class="sxs-lookup"><span data-stu-id="77a70-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-202">Si es **true**, el archivo se comprime.</span><span class="sxs-lookup"><span data-stu-id="77a70-202">If **True**, the file is compressed.</span></span>

<span data-ttu-id="77a70-203">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-203">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-204">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="77a70-204">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-207">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compresión")</span><span class="sxs-lookup"><span data-stu-id="77a70-207">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-208">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="77a70-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="77a70-209">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="77a70-209">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="77a70-210">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="77a70-210">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="77a70-211">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="77a70-211">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="77a70-212">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-213">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="77a70-213">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-216">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="77a70-216">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-217">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="77a70-217">Name of the class.</span></span>

<span data-ttu-id="77a70-218">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-219">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="77a70-219">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-220">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="77a70-220">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-222">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fecha de creación")</span><span class="sxs-lookup"><span data-stu-id="77a70-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-223">Fecha y hora de creación del archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-223">Date and time of the file's creation.</span></span>

<span data-ttu-id="77a70-224">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-224">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-225">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="77a70-225">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-226">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-228">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase de sistema de equipo ")</span><span class="sxs-lookup"><span data-stu-id="77a70-228">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-229">Clase del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="77a70-229">Class of the computer system.</span></span>

<span data-ttu-id="77a70-230">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-230">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-231">**CSName**</span><span class="sxs-lookup"><span data-stu-id="77a70-231">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-234">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="77a70-234">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-235">Nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="77a70-235">Name of the computer system.</span></span>

<span data-ttu-id="77a70-236">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-236">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-237">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77a70-237">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-238">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-240">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="77a70-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-241">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-241">A textual description of the object.</span></span>

<span data-ttu-id="77a70-242">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-243">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="77a70-243">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-246">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="77a70-246">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-247">Letra de unidad (incluidos los dos puntos que siguen a la letra de unidad) del archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-247">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="77a70-248">Ejemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="77a70-248">Example: "c:"</span></span>

<span data-ttu-id="77a70-249">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-249">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-250">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="77a70-250">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-253">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo de ocho puntos tres")</span><span class="sxs-lookup"><span data-stu-id="77a70-253">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-254">Nombre de archivo compatible con DOS.</span><span class="sxs-lookup"><span data-stu-id="77a70-254">DOS-compatible file name.</span></span>

<span data-ttu-id="77a70-255">Ejemplo: "c: \\ programa ~ 1"</span><span class="sxs-lookup"><span data-stu-id="77a70-255">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="77a70-256">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-256">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-257">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="77a70-257">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-258">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="77a70-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-260">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("cifrado")</span><span class="sxs-lookup"><span data-stu-id="77a70-260">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-261">Si es **true**, el archivo está cifrado.</span><span class="sxs-lookup"><span data-stu-id="77a70-261">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="77a70-262">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-263">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="77a70-263">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-266">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de cifrado")</span><span class="sxs-lookup"><span data-stu-id="77a70-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-267">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="77a70-267">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="77a70-268">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="77a70-268">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="77a70-269">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="77a70-269">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="77a70-270">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="77a70-270">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="77a70-271">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-271">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-272">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="77a70-272">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-275">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensión de archivo")</span><span class="sxs-lookup"><span data-stu-id="77a70-275">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-276">Extensión de nombre de archivo sin el punto anterior (punto).</span><span class="sxs-lookup"><span data-stu-id="77a70-276">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="77a70-277">Ejemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="77a70-277">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="77a70-278">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-278">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-279">**FileName**</span><span class="sxs-lookup"><span data-stu-id="77a70-279">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-280">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-282">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo")</span><span class="sxs-lookup"><span data-stu-id="77a70-282">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-283">Nombre de archivo sin la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-283">File name without the file name extension.</span></span> <span data-ttu-id="77a70-284">Ejemplo: "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="77a70-284">Example: "MyDataFile"</span></span>

<span data-ttu-id="77a70-285">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-285">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-286">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="77a70-286">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-287">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="77a70-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-289">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="77a70-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-290">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="77a70-290">Size of the file, in bytes.</span></span>

<span data-ttu-id="77a70-291">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="77a70-291">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="77a70-292">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-293">**FileType**</span><span class="sxs-lookup"><span data-stu-id="77a70-293">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-296">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de archivo")</span><span class="sxs-lookup"><span data-stu-id="77a70-296">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-297">Descriptor que representa el tipo de archivo indicado por la propiedad de **extensión** .</span><span class="sxs-lookup"><span data-stu-id="77a70-297">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="77a70-298">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-299">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="77a70-299">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-302">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="77a70-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-303">Clase del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="77a70-303">Class of the file system.</span></span>

<span data-ttu-id="77a70-304">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-304">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-305">**FSName**</span><span class="sxs-lookup"><span data-stu-id="77a70-305">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-306">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-308">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="77a70-308">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-309">Nombre del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="77a70-309">Name of the file system.</span></span>

<span data-ttu-id="77a70-310">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-311">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="77a70-311">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-312">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="77a70-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-314">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="77a70-314">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-315">Si es **true**, el archivo está oculto.</span><span class="sxs-lookup"><span data-stu-id="77a70-315">If **True**, the file is hidden.</span></span>

<span data-ttu-id="77a70-316">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-316">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="77a70-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-318">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="77a70-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-320">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="77a70-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-321">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-321">Indicates when the object was installed.</span></span> <span data-ttu-id="77a70-322">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="77a70-322">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="77a70-323">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-324">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="77a70-324">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-325">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="77a70-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-327">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("recuento de apertura de archivos actuales")</span><span class="sxs-lookup"><span data-stu-id="77a70-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-328">Número de "archivos abiertos" que están activos actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-328">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="77a70-329">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="77a70-329">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="77a70-330">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-331">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="77a70-331">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-332">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="77a70-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-334">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acceso")</span><span class="sxs-lookup"><span data-stu-id="77a70-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-335">Fecha y hora en que se produjo el último acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-335">Date and time the file was last accessed.</span></span>

<span data-ttu-id="77a70-336">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-337">**Última**</span><span class="sxs-lookup"><span data-stu-id="77a70-337">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-338">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="77a70-338">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-340">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificación")</span><span class="sxs-lookup"><span data-stu-id="77a70-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-341">Fecha y hora en que se modificó el archivo por última vez.</span><span class="sxs-lookup"><span data-stu-id="77a70-341">Date and time the file was last modified.</span></span>

<span data-ttu-id="77a70-342">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-342">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-343">**Le**</span><span class="sxs-lookup"><span data-stu-id="77a70-343">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-344">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-346">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("manufacturer")</span><span class="sxs-lookup"><span data-stu-id="77a70-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-347">Cadena del fabricante del recurso de versión (si está presente).</span><span class="sxs-lookup"><span data-stu-id="77a70-347">Manufacturer string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-348">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="77a70-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-351">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77a70-351">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77a70-352">La propiedad Name es una cadena que representa el nombre heredado que actúa como clave de una instancia de archivo lógico dentro de un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="77a70-352">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="77a70-353">Se deben proporcionar los nombres de ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="77a70-353">Full path names should be provided.</span></span>

<span data-ttu-id="77a70-354">Ejemplo: C: \\ Windows \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="77a70-354">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="77a70-355">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-355">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-356">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="77a70-356">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-357">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-359">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="77a70-359">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-360">Ruta de acceso del archivo, incluidas las barras diagonales inversas iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="77a70-360">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="77a70-361">Ejemplo: " \\ sistema de Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="77a70-361">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="77a70-362">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-362">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-363">**Puedan**</span><span class="sxs-lookup"><span data-stu-id="77a70-363">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-364">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="77a70-364">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-366">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legible")</span><span class="sxs-lookup"><span data-stu-id="77a70-366">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-367">Si **es true**, se puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-367">If **True**, the file can be read.</span></span>

<span data-ttu-id="77a70-368">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-368">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-369">**Estado**</span><span class="sxs-lookup"><span data-stu-id="77a70-369">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-370">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-372">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="77a70-372">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-373">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="77a70-373">String that indicates the current status of the object.</span></span> <span data-ttu-id="77a70-374">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="77a70-374">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="77a70-375">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="77a70-375">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="77a70-376">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="77a70-376">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="77a70-377">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="77a70-377">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="77a70-378">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="77a70-378">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="77a70-379">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="77a70-379">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="77a70-380">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="77a70-381">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="77a70-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="77a70-382">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="77a70-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="77a70-383">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="77a70-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="77a70-384">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="77a70-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="77a70-385">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="77a70-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="77a70-386">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="77a70-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="77a70-387">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="77a70-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="77a70-388">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="77a70-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="77a70-389">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="77a70-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="77a70-390">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="77a70-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="77a70-391">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="77a70-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="77a70-392">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="77a70-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="77a70-393">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="77a70-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="77a70-394">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="77a70-394">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-395">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="77a70-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-397">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("archivo del sistema")</span><span class="sxs-lookup"><span data-stu-id="77a70-397">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-398">Si es **true**, el archivo es un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="77a70-398">If **True**, the file is a system file.</span></span>

<span data-ttu-id="77a70-399">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-400">**Versión**</span><span class="sxs-lookup"><span data-stu-id="77a70-400">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="77a70-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-403">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("versión")</span><span class="sxs-lookup"><span data-stu-id="77a70-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-404">Cadena de versión del recurso de versión (si está presente).</span><span class="sxs-lookup"><span data-stu-id="77a70-404">Version string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="77a70-405">**Writeable (Grabable)**</span><span class="sxs-lookup"><span data-stu-id="77a70-405">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a70-406">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="77a70-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a70-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="77a70-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a70-408">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("grabable")</span><span class="sxs-lookup"><span data-stu-id="77a70-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="77a70-409">Si **es true**, se puede escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-409">If **True**, the file can be written.</span></span>

<span data-ttu-id="77a70-410">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77a70-411">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77a70-411">Remarks</span></span>

<span data-ttu-id="77a70-412">La clase de **\_ archivo de archivos CIM** se deriva de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="77a70-412">The **CIM\_DataFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="77a70-413">WMI implementa la clase **de \_ archivo de archivos CIM** y todos sus métodos.</span><span class="sxs-lookup"><span data-stu-id="77a70-413">WMI implements the **CIM\_DataFile** class and all of its methods.</span></span> <span data-ttu-id="77a70-414">La clase de **\_ archivo de archivos CIM** es una clase dinámica.</span><span class="sxs-lookup"><span data-stu-id="77a70-414">The **CIM\_DataFile** class is a dynamic class.</span></span>

<span data-ttu-id="77a70-415">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="77a70-415">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="77a70-416">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="77a70-416">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="77a70-417">Por motivos de seguridad, WMI no admite directamente la llamada a un equipo remoto y le indica que copie archivos en sí mismo.</span><span class="sxs-lookup"><span data-stu-id="77a70-417">Due to security purposes, WMI does not directly support calling a remote computer and instructing it to copy files to itself.</span></span> <span data-ttu-id="77a70-418">Sin embargo, puede usar el lenguaje de programación pertinente para llamar a FTP o RoboCopy, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="77a70-418">However, you can use the relevant programming language to call FTP or RoboCopy, for example.</span></span>

## <a name="examples"></a><span data-ttu-id="77a70-419">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="77a70-419">Examples</span></span>

<span data-ttu-id="77a70-420">En el siguiente ejemplo de [código](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) del centro de scripting se usa una clase de **archivo de \_ archivos CIM** como parte de una aplicación más grande para generar informes de entorno de Exchange mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77a70-420">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) uses a **CIM\_DataFile** class as part of a larger application to Generate exchange environment reports using Powershell.</span></span>

<span data-ttu-id="77a70-421">El ejemplo de código [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) de la galería de TechNet usa un **\_ archivo** de información de CIM para buscar uno o varios archivos en varios equipos.</span><span class="sxs-lookup"><span data-stu-id="77a70-421">The [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) code sample in TechNet Gallery uses a **CIM\_DataFile** to search for one or more files across multiple computers.</span></span>

<span data-ttu-id="77a70-422">El siguiente ejemplo de código VBS describe cómo realizar una búsqueda con caracteres comodín estándar en un archivo de archivos.</span><span class="sxs-lookup"><span data-stu-id="77a70-422">The following VBS code sample describes how to perform a standard wildcard search on a datafile.</span></span> <span data-ttu-id="77a70-423">Tenga en cuenta que los delimitadores de barra diagonal inversa deben tener otra barra diagonal inversa ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="77a70-423">Note that the backslash delimiters must be escaped with another backslash (\\\\).</span></span> <span data-ttu-id="77a70-424">Además, cuando se usa **" \_ archivo de archivos CIM**.**Nombre de archivo**"en la cláusula WHERE, el proceso de WMIPRVSE examinará todos los directorios de cualquier dispositivo de almacenamiento disponible.</span><span class="sxs-lookup"><span data-stu-id="77a70-424">Also, when using "**CIM\_DataFile**.**FileName**" in the WHERE clause, the WMIPRVSE process will scan all directories on any available storage device.</span></span> <span data-ttu-id="77a70-425">Esto puede tardar algún tiempo, especialmente si ha asignado recursos compartidos remotos, y puede desencadenar advertencias del antivirus.</span><span class="sxs-lookup"><span data-stu-id="77a70-425">This may take some time, especially if you have mapped remote shares, and can trigger antivirus warnings.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



<span data-ttu-id="77a70-426">El siguiente fragmento de código limita el intervalo de búsqueda a una unidad específica, una ruta de acceso y una extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="77a70-426">The following snippet limits the search range to a specific drive, path, and file extension.</span></span>


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



<span data-ttu-id="77a70-427">El siguiente ejemplo de código de PowerShell recupera un valor de atributo único.</span><span class="sxs-lookup"><span data-stu-id="77a70-427">The following PowerShell code sample retrieves a single attribute value.</span></span>


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



## <a name="requirements"></a><span data-ttu-id="77a70-428">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77a70-428">Requirements</span></span>



| <span data-ttu-id="77a70-429">Requisito</span><span class="sxs-lookup"><span data-stu-id="77a70-429">Requirement</span></span> | <span data-ttu-id="77a70-430">Value</span><span class="sxs-lookup"><span data-stu-id="77a70-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77a70-431">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77a70-431">Minimum supported client</span></span><br/> | <span data-ttu-id="77a70-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77a70-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77a70-433">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77a70-433">Minimum supported server</span></span><br/> | <span data-ttu-id="77a70-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77a70-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77a70-435">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="77a70-435">Namespace</span></span><br/>                | <span data-ttu-id="77a70-436">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="77a70-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="77a70-437">MOF</span><span class="sxs-lookup"><span data-stu-id="77a70-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77a70-438"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77a70-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="77a70-439">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77a70-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77a70-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77a70-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77a70-441">Vea también</span><span class="sxs-lookup"><span data-stu-id="77a70-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77a70-442">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="77a70-442">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="77a70-443">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="77a70-443">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="77a70-444">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="77a70-444">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

