---
description: La \_ clase CIM LogicalFile representa una colección con nombre de datos, que puede ser código ejecutable, que se encuentra en un sistema de archivos en una extensión de almacenamiento.
ms.assetid: 96bf95a1-c8d7-4035-8d5a-38cdb9c75cce
ms.tgt_platform: multiple
title: CIM_LogicalFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile
- CIM_LogicalFile.Caption
- CIM_LogicalFile.Description
- CIM_LogicalFile.InstallDate
- CIM_LogicalFile.Status
- CIM_LogicalFile.AccessMask
- CIM_LogicalFile.Archive
- CIM_LogicalFile.Compressed
- CIM_LogicalFile.CompressionMethod
- CIM_LogicalFile.CreationClassName
- CIM_LogicalFile.CreationDate
- CIM_LogicalFile.CSCreationClassName
- CIM_LogicalFile.CSName
- CIM_LogicalFile.Drive
- CIM_LogicalFile.EightDotThreeFileName
- CIM_LogicalFile.Encrypted
- CIM_LogicalFile.EncryptionMethod
- CIM_LogicalFile.Name
- CIM_LogicalFile.Extension
- CIM_LogicalFile.FileName
- CIM_LogicalFile.FileSize
- CIM_LogicalFile.FileType
- CIM_LogicalFile.FSCreationClassName
- CIM_LogicalFile.FSName
- CIM_LogicalFile.Hidden
- CIM_LogicalFile.InUseCount
- CIM_LogicalFile.LastAccessed
- CIM_LogicalFile.LastModified
- CIM_LogicalFile.Path
- CIM_LogicalFile.Readable
- CIM_LogicalFile.System
- CIM_LogicalFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a06d2abd1c4ad92d751afa6c8aa47c0cfaa8b1f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659424"
---
# <a name="cim_logicalfile-class"></a><span data-ttu-id="c28be-103">\_Clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="c28be-103">CIM\_LogicalFile class</span></span>

<span data-ttu-id="c28be-104">La clase **CIM \_ LogicalFile** representa una colección con nombre de datos, que puede ser código ejecutable, que se encuentra en un sistema de archivos en una extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="c28be-104">The **CIM\_LogicalFile** class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c28be-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c28be-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c28be-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c28be-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c28be-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c28be-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c28be-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c28be-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c28be-109">Syntax</span></span>

``` syntax
[SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C559-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Files (CIM)"), AMENDMENT]
class CIM_LogicalFile : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="c28be-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c28be-110">Members</span></span>

<span data-ttu-id="c28be-111">La clase **CIM \_ LogicalFile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c28be-111">The **CIM\_LogicalFile** class has these types of members:</span></span>

-   [<span data-ttu-id="c28be-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c28be-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c28be-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c28be-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c28be-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c28be-114">Methods</span></span>

<span data-ttu-id="c28be-115">La clase **CIM \_ LogicalFile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c28be-115">The **CIM\_LogicalFile** class has these methods.</span></span>



| <span data-ttu-id="c28be-116">Método</span><span class="sxs-lookup"><span data-stu-id="c28be-116">Method</span></span>                                                                                             | <span data-ttu-id="c28be-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c28be-117">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c28be-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="c28be-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | <span data-ttu-id="c28be-119">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="c28be-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="c28be-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="c28be-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | <span data-ttu-id="c28be-122">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="c28be-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="c28be-124">**Comprimir**</span><span class="sxs-lookup"><span data-stu-id="c28be-124">**Compress**</span></span>](compress-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="c28be-125">Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c28be-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="c28be-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="c28be-127">**CompressEx**</span></span>](compressex-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="c28be-128">Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c28be-129">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="c28be-130">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="c28be-130">**Copy**</span></span>](copy-method-in-class-cim-logicalfile.md)                                               | <span data-ttu-id="c28be-131">Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c28be-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="c28be-132">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="c28be-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="c28be-133">**CopyEx**</span></span>](copyex-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="c28be-134">Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c28be-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="c28be-135">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="c28be-136">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="c28be-136">**Delete**</span></span>](delete-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="c28be-137">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c28be-138">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="c28be-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="c28be-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="c28be-140">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c28be-141">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="c28be-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="c28be-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)           | <span data-ttu-id="c28be-143">Determina si el llamador tiene los permisos agregados especificados por el argumento de **permiso** .</span><span class="sxs-lookup"><span data-stu-id="c28be-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="c28be-144">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="c28be-145">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="c28be-145">**Rename**</span></span>](rename-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="c28be-146">Cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c28be-147">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="c28be-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="c28be-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-logicalfile.md)                             | <span data-ttu-id="c28be-149">Obtiene la propiedad del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-149">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c28be-150">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-150">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="c28be-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="c28be-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)                         | <span data-ttu-id="c28be-152">Obtiene la propiedad del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-152">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c28be-153">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-153">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="c28be-154">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="c28be-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="c28be-155">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c28be-156">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="c28be-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="c28be-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-logicalfile.md)                               | <span data-ttu-id="c28be-158">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c28be-159">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c28be-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="c28be-160">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c28be-160">Properties</span></span>

<span data-ttu-id="c28be-161">La clase **CIM \_ LogicalFile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c28be-161">The **CIM\_LogicalFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c28be-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="c28be-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-163">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c28be-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-165">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("derechos de acceso")</span><span class="sxs-lookup"><span data-stu-id="c28be-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-166">Máscara de archivos que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="c28be-166">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="c28be-167">Para los valores de bit, consulte [**constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="c28be-167">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="c28be-168">En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="c28be-169">**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="c28be-169">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="c28be-170">**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="c28be-170">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="c28be-171">**Archivo \_ de ANEXAr \_ datos (archivo) o archivo \_ agregar \_ subdirectorio (directorio)** (4)</span><span class="sxs-lookup"><span data-stu-id="c28be-171">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="c28be-172">**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="c28be-172">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="c28be-173">**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="c28be-173">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="c28be-174">**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="c28be-174">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="c28be-175">**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="c28be-175">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="c28be-176">**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="c28be-176">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="c28be-177">**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="c28be-177">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="c28be-178">**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="c28be-178">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="c28be-179">**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="c28be-179">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="c28be-180">**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="c28be-180">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="c28be-181">**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="c28be-181">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="c28be-182">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="c28be-182">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c28be-183">**Archivar**</span><span class="sxs-lookup"><span data-stu-id="c28be-183">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c28be-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-186">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("se debe archivar")</span><span class="sxs-lookup"><span data-stu-id="c28be-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-187">Si **es true**, se debe archivar el archivo.</span><span class="sxs-lookup"><span data-stu-id="c28be-187">If **True**, the file should be archived.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-188">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c28be-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-191">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c28be-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-192">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-192">A short textual description of the object.</span></span>

<span data-ttu-id="c28be-193">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c28be-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c28be-194">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="c28be-194">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-195">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c28be-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-197">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("comprimido")</span><span class="sxs-lookup"><span data-stu-id="c28be-197">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-198">Si es **true**, el archivo se comprime.</span><span class="sxs-lookup"><span data-stu-id="c28be-198">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="c28be-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-202">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compresión")</span><span class="sxs-lookup"><span data-stu-id="c28be-202">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-203">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c28be-203">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="c28be-204">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="c28be-204">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="c28be-205">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="c28be-205">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="c28be-206">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="c28be-206">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="c28be-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c28be-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-210">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="c28be-210">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-211">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="c28be-211">Name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-212">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="c28be-212">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-213">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c28be-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-215">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fecha de creación")</span><span class="sxs-lookup"><span data-stu-id="c28be-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-216">Fecha y hora de creación del archivo.</span><span class="sxs-lookup"><span data-stu-id="c28be-216">Date and time of the file's creation.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-217">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c28be-217">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-220">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase de sistema de equipo ")</span><span class="sxs-lookup"><span data-stu-id="c28be-220">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-221">Clase del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="c28be-221">Class of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-222">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c28be-222">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-225">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="c28be-225">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-226">Nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="c28be-226">Name of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-227">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c28be-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-230">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="c28be-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-231">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-231">A textual description of the object.</span></span>

<span data-ttu-id="c28be-232">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c28be-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c28be-233">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="c28be-233">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-236">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="c28be-236">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-237">Letra de unidad (incluidos los dos puntos que siguen a la letra de unidad) del archivo.</span><span class="sxs-lookup"><span data-stu-id="c28be-237">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="c28be-238">Esta propiedad se hereda de **\_ LogicalFile CIM**. Ejemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="c28be-238">This property is inherited from **CIM\_LogicalFile**.Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="c28be-239">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="c28be-239">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-242">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo de ocho puntos tres")</span><span class="sxs-lookup"><span data-stu-id="c28be-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-243">Nombre de archivo compatible con DOS.</span><span class="sxs-lookup"><span data-stu-id="c28be-243">DOS-compatible file name.</span></span> <span data-ttu-id="c28be-244">Ejemplo: "c: \\ programa ~ 1"</span><span class="sxs-lookup"><span data-stu-id="c28be-244">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="c28be-245">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="c28be-245">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-246">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c28be-246">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-248">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("cifrado")</span><span class="sxs-lookup"><span data-stu-id="c28be-248">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-249">Si es **true**, el archivo está cifrado.</span><span class="sxs-lookup"><span data-stu-id="c28be-249">If **True**, the file is encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-250">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="c28be-250">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-253">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de cifrado")</span><span class="sxs-lookup"><span data-stu-id="c28be-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-254">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c28be-254">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="c28be-255">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="c28be-255">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="c28be-256">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="c28be-256">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="c28be-257">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="c28be-257">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="c28be-258">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="c28be-258">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-259">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-261">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensión de archivo")</span><span class="sxs-lookup"><span data-stu-id="c28be-261">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-262">Extensión de nombre de archivo sin el punto anterior (punto).</span><span class="sxs-lookup"><span data-stu-id="c28be-262">File name extension without the preceding period (dot).</span></span> <span data-ttu-id="c28be-263">Ejemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="c28be-263">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="c28be-264">**FileName**</span><span class="sxs-lookup"><span data-stu-id="c28be-264">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-265">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-267">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo")</span><span class="sxs-lookup"><span data-stu-id="c28be-267">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-268">Nombre de archivo sin la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c28be-268">File name without the file name extension.</span></span> <span data-ttu-id="c28be-269">Ejemplo: "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="c28be-269">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="c28be-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="c28be-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-271">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c28be-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-273">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c28be-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-274">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c28be-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="c28be-275">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c28be-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c28be-276">**FileType**</span><span class="sxs-lookup"><span data-stu-id="c28be-276">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-277">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-279">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de archivo")</span><span class="sxs-lookup"><span data-stu-id="c28be-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-280">Descriptor que representa el tipo de archivo indicado por la propiedad de **extensión** .</span><span class="sxs-lookup"><span data-stu-id="c28be-280">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c28be-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-284">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="c28be-284">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-285">Clase del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c28be-285">Class of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-286">**FSName**</span><span class="sxs-lookup"><span data-stu-id="c28be-286">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-287">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-289">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="c28be-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-290">Nombre del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c28be-290">Name of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-291">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="c28be-291">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-292">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c28be-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-294">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="c28be-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-295">Si es **true**, el archivo está oculto.</span><span class="sxs-lookup"><span data-stu-id="c28be-295">If **True**, the file is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-296">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c28be-296">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-297">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c28be-297">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-299">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="c28be-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-300">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-300">Indicates when the object was installed.</span></span> <span data-ttu-id="c28be-301">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="c28be-301">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c28be-302">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c28be-302">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c28be-303">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="c28be-303">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-304">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c28be-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-306">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("recuento de apertura de archivos actuales")</span><span class="sxs-lookup"><span data-stu-id="c28be-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-307">Número de "archivos abiertos" que están activos actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="c28be-307">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="c28be-308">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c28be-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c28be-309">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="c28be-309">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-310">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c28be-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-312">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acceso")</span><span class="sxs-lookup"><span data-stu-id="c28be-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-313">Fecha y hora en que se produjo el último acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="c28be-313">Date and time the file was last accessed.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-314">**Última**</span><span class="sxs-lookup"><span data-stu-id="c28be-314">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-315">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c28be-315">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-317">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificación")</span><span class="sxs-lookup"><span data-stu-id="c28be-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-318">Fecha y hora en que se modificó el archivo por última vez.</span><span class="sxs-lookup"><span data-stu-id="c28be-318">Date and time the file was last modified.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-319">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c28be-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-322">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c28be-322">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c28be-323">La propiedad Name es una cadena que representa el nombre heredado que actúa como clave de una instancia de archivo lógico dentro de un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c28be-323">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="c28be-324">Se deben proporcionar los nombres de ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="c28be-324">Full path names should be provided.</span></span> <span data-ttu-id="c28be-325">Ejemplo: C: \\ Windows \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="c28be-325">Example: C:\\Windows\\system\\win.ini</span></span>

</dd> <dt>

<span data-ttu-id="c28be-326">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="c28be-326">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-327">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-329">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="c28be-329">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-330">Ruta de acceso del archivo, incluidas las barras diagonales inversas iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="c28be-330">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="c28be-331">Ejemplo: " \\ sistema de Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="c28be-331">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="c28be-332">**Puedan**</span><span class="sxs-lookup"><span data-stu-id="c28be-332">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-333">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c28be-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-335">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legible")</span><span class="sxs-lookup"><span data-stu-id="c28be-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-336">Si **es true**, se puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="c28be-336">If **True**, the file can be read.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-337">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c28be-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-338">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c28be-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-340">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c28be-340">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-341">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c28be-341">String that indicates the current status of the object.</span></span> <span data-ttu-id="c28be-342">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="c28be-342">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c28be-343">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="c28be-343">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c28be-344">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="c28be-344">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c28be-345">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="c28be-345">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c28be-346">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="c28be-346">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c28be-347">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="c28be-347">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c28be-348">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c28be-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c28be-349">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c28be-349">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c28be-350">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="c28be-350">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c28be-351">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="c28be-351">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c28be-352">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c28be-352">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c28be-353">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="c28be-353">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c28be-354">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="c28be-354">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c28be-355">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="c28be-355">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c28be-356">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="c28be-356">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c28be-357">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="c28be-357">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c28be-358">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="c28be-358">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c28be-359">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c28be-359">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c28be-360">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="c28be-360">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c28be-361">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="c28be-361">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c28be-362">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="c28be-362">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-363">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c28be-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-365">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("archivo del sistema")</span><span class="sxs-lookup"><span data-stu-id="c28be-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-366">Si es **true**, el archivo es un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="c28be-366">If **True**, the file is a system file.</span></span>

</dd> <dt>

<span data-ttu-id="c28be-367">**Writeable (Grabable)**</span><span class="sxs-lookup"><span data-stu-id="c28be-367">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c28be-368">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c28be-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c28be-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c28be-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c28be-370">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("grabable")</span><span class="sxs-lookup"><span data-stu-id="c28be-370">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="c28be-371">Si **es true**, se puede escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="c28be-371">If **True**, the file can be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c28be-372">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c28be-372">Remarks</span></span>

<span data-ttu-id="c28be-373">La clase **CIM \_ LogicalFile** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c28be-373">The **CIM\_LogicalFile** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="c28be-374">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c28be-374">WMI does not implement this class.</span></span> <span data-ttu-id="c28be-375">Para las clases derivadas de **CIM \_ LogicalFile**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c28be-375">For classes derived from **CIM\_LogicalFile**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c28be-376">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c28be-376">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c28be-377">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c28be-377">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c28be-378">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c28be-378">Requirements</span></span>



| <span data-ttu-id="c28be-379">Requisito</span><span class="sxs-lookup"><span data-stu-id="c28be-379">Requirement</span></span> | <span data-ttu-id="c28be-380">Value</span><span class="sxs-lookup"><span data-stu-id="c28be-380">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c28be-381">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c28be-381">Minimum supported client</span></span><br/> | <span data-ttu-id="c28be-382">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c28be-382">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c28be-383">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c28be-383">Minimum supported server</span></span><br/> | <span data-ttu-id="c28be-384">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c28be-384">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c28be-385">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c28be-385">Namespace</span></span><br/>                | <span data-ttu-id="c28be-386">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c28be-386">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c28be-387">MOF</span><span class="sxs-lookup"><span data-stu-id="c28be-387">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c28be-388"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c28be-388"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c28be-389">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c28be-389">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c28be-390"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c28be-390"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c28be-391">Vea también</span><span class="sxs-lookup"><span data-stu-id="c28be-391">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c28be-392">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="c28be-392">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

