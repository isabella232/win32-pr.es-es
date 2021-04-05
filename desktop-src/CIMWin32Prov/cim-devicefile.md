---
description: La \_ clase CIM DeviceFile representa un tipo de archivo lógico, que representa un dispositivo.
ms.assetid: b07f039c-8ab0-4e13-96d5-3621da19e66d
ms.tgt_platform: multiple
title: CIM_DeviceFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile
- CIM_DeviceFile.AccessMask
- CIM_DeviceFile.Archive
- CIM_DeviceFile.Caption
- CIM_DeviceFile.Compressed
- CIM_DeviceFile.CompressionMethod
- CIM_DeviceFile.CreationClassName
- CIM_DeviceFile.CreationDate
- CIM_DeviceFile.CSCreationClassName
- CIM_DeviceFile.CSName
- CIM_DeviceFile.Description
- CIM_DeviceFile.Drive
- CIM_DeviceFile.EightDotThreeFileName
- CIM_DeviceFile.Encrypted
- CIM_DeviceFile.EncryptionMethod
- CIM_DeviceFile.Extension
- CIM_DeviceFile.FileName
- CIM_DeviceFile.FileSize
- CIM_DeviceFile.FileType
- CIM_DeviceFile.FSCreationClassName
- CIM_DeviceFile.FSName
- CIM_DeviceFile.Hidden
- CIM_DeviceFile.InstallDate
- CIM_DeviceFile.InUseCount
- CIM_DeviceFile.LastAccessed
- CIM_DeviceFile.LastModified
- CIM_DeviceFile.Name
- CIM_DeviceFile.Path
- CIM_DeviceFile.Readable
- CIM_DeviceFile.Status
- CIM_DeviceFile.System
- CIM_DeviceFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 476f0ecd212247e1fc96db3efedcc0c18a6a2e06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000692"
---
# <a name="cim_devicefile-class"></a><span data-ttu-id="2dc3a-103">\_Clase DeviceFile de CIM</span><span class="sxs-lookup"><span data-stu-id="2dc3a-103">CIM\_DeviceFile class</span></span>

<span data-ttu-id="2dc3a-104">La clase **CIM \_ DeviceFile** representa un tipo de archivo lógico, que representa un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-104">The **CIM\_DeviceFile** class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="2dc3a-105">Esta Convención es útil para los sistemas operativos que administran dispositivos mediante un modelo de e/s de secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-105">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="2dc3a-106">El dispositivo lógico asociado a este archivo se especifica mediante la relación [**\_ DeviceAccessedByFile de CIM**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2dc3a-106">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2dc3a-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2dc3a-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2dc3a-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2dc3a-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc3a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dc3a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{4333BD60-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceFile : CIM_LogicalFile
{
  uint32   AccessMask;
  boolean  Archive;
  string   Caption;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
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
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="2dc3a-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="2dc3a-112">Members</span></span>

<span data-ttu-id="2dc3a-113">La clase **CIM \_ DeviceFile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2dc3a-113">The **CIM\_DeviceFile** class has these types of members:</span></span>

-   [<span data-ttu-id="2dc3a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="2dc3a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2dc3a-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2dc3a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2dc3a-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="2dc3a-116">Methods</span></span>

<span data-ttu-id="2dc3a-117">La clase **CIM \_ DeviceFile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-117">The **CIM\_DeviceFile** class has these methods.</span></span>



| <span data-ttu-id="2dc3a-118">Método</span><span class="sxs-lookup"><span data-stu-id="2dc3a-118">Method</span></span>                                                                                            | <span data-ttu-id="2dc3a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2dc3a-119">Description</span></span>                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dc3a-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)     | <span data-ttu-id="2dc3a-121">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="2dc3a-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-122">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="2dc3a-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md) | <span data-ttu-id="2dc3a-124">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="2dc3a-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-125">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="2dc3a-126">**Comprimir**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-126">**Compress**</span></span>](compress-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="2dc3a-127">Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-127">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="2dc3a-128">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-128">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="2dc3a-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-129">**CompressEx**</span></span>](compressex-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="2dc3a-130">Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="2dc3a-131">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-131">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="2dc3a-132">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-132">**Copy**</span></span>](copy-method-in-class-cim-devicefile.md)                                               | <span data-ttu-id="2dc3a-133">Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="2dc3a-134">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-134">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="2dc3a-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-135">**CopyEx**</span></span>](copyex-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="2dc3a-136">Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="2dc3a-137">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-137">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="2dc3a-138">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-138">**Delete**</span></span>](delete-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="2dc3a-139">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="2dc3a-140">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-140">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="2dc3a-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="2dc3a-142">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="2dc3a-143">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-143">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="2dc3a-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)           | <span data-ttu-id="2dc3a-145">Determina si el llamador tiene los permisos agregados especificados por el argumento de **permiso** .</span><span class="sxs-lookup"><span data-stu-id="2dc3a-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="2dc3a-146">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-146">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="2dc3a-147">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-147">**Rename**</span></span>](rename-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="2dc3a-148">Cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="2dc3a-149">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-149">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="2dc3a-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-devicefile.md)                             | <span data-ttu-id="2dc3a-151">Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="2dc3a-152">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-152">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="2dc3a-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-devicefile.md)                         | <span data-ttu-id="2dc3a-154">Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="2dc3a-155">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-155">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="2dc3a-156">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="2dc3a-157">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="2dc3a-158">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-158">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="2dc3a-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-devicefile.md)                               | <span data-ttu-id="2dc3a-160">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="2dc3a-161">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-161">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="2dc3a-162">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2dc3a-162">Properties</span></span>

<span data-ttu-id="2dc3a-163">La clase **CIM \_ DeviceFile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-163">The **CIM\_DeviceFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2dc3a-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-167">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("derechos de acceso")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-168">Matriz de bits que representa los derechos de acceso al archivo o directorio especificado que mantiene el usuario o grupo en cuyo nombre se devuelve la instancia.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-168">Bit array that represents the access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="2dc3a-169">En los volúmenes FAT, se devuelve **\_ acceso completo** , que indica que no se ha establecido ninguna seguridad en el objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-169">On FAT volumes, **FULL\_ACCESS** is returned, which indicates that no security has been set on the object.</span></span>

<span data-ttu-id="2dc3a-170">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-170">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="2dc3a-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-172">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-172">Grants the right to read data from the file.</span></span> <span data-ttu-id="2dc3a-173">Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-173">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="2dc3a-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-175">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-175">Grants the right to write data to the file.</span></span> <span data-ttu-id="2dc3a-176">Para un directorio, este valor concede el derecho a crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-176">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="2dc3a-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Archivo \_ de ANEXAr \_ datos (archivo) o archivo \_ agregar \_ subdirectorio (directorio)** (4)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-178">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-178">Grants the right to append data to the file.</span></span> <span data-ttu-id="2dc3a-179">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-179">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="2dc3a-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-181">Concede el derecho para leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-181">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="2dc3a-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-183">Concede el derecho para escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-183">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="2dc3a-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-185">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-185">Grants the right to execute a file.</span></span> <span data-ttu-id="2dc3a-186">Para un directorio, se puede atravesar el directorio.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-186">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="2dc3a-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-188">Concede el derecho para eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-188">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="2dc3a-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-190">Concede el derecho a leer los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-190">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="2dc3a-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-192">Concede el derecho para cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-192">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="2dc3a-193"><span id="DELETE"></span><span id="delete"></span>**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-193"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-194">Concede acceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-194">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="2dc3a-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-196">Concede acceso de lectura al descriptor de seguridad y al propietario.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-196">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="2dc3a-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-198">Concede acceso de escritura a la ACL discrecional.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-198">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="2dc3a-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-200">Asigna el propietario de la escritura.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-200">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="2dc3a-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="2dc3a-202">Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-202">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2dc3a-203">**Archivar**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-203">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-204">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-206">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("se debe archivar")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-206">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-207">Si **es true**, se debe archivar el archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-207">If **True**, the file should be archived.</span></span>

<span data-ttu-id="2dc3a-208">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-209">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-209">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-212">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-213">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-213">Short textual description of the object.</span></span>

<span data-ttu-id="2dc3a-214">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-215">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-215">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-216">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-218">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("comprimido")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-218">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-219">Si es **true**, el archivo se comprime.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-219">If **True**, the file is compressed.</span></span>

<span data-ttu-id="2dc3a-220">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-221">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-221">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-224">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compresión")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-224">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-225">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="2dc3a-226">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="2dc3a-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="2dc3a-227">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="2dc3a-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="2dc3a-228">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="2dc3a-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="2dc3a-229">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-229">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-230">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-230">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-233">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-233">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-234">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-234">Name of the class.</span></span>

<span data-ttu-id="2dc3a-235">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-235">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-236">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-236">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-237">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-239">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fecha de creación")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-240">Fecha de creación del archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-240">File's creation date.</span></span>

<span data-ttu-id="2dc3a-241">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-242">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-242">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-245">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase de sistema de equipo ")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-245">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-246">Clase del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-246">Class of the computer system.</span></span>

<span data-ttu-id="2dc3a-247">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-247">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-248">**CSName**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-248">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-251">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-251">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-252">Nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-252">Name of the computer system.</span></span>

<span data-ttu-id="2dc3a-253">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-254">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-257">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-258">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-258">Textual description of the object.</span></span>

<span data-ttu-id="2dc3a-259">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-260">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-260">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-263">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-263">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-264">Letra de unidad (incluidos los dos puntos que siguen a la letra de unidad) del archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-264">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="2dc3a-265">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="2dc3a-266">Ejemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="2dc3a-266">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-267">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-267">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-268">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-270">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo de ocho puntos tres")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-270">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-271">Nombre de archivo compatible con DOS para el archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-271">DOS-compatible file name for the file.</span></span> <span data-ttu-id="2dc3a-272">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="2dc3a-273">Ejemplo: "c: \\ programa ~ 1"</span><span class="sxs-lookup"><span data-stu-id="2dc3a-273">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-274">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-274">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-275">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-277">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("cifrado")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-278">Si es **true**, el archivo está cifrado.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-278">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="2dc3a-279">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-280">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-280">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-281">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-283">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de cifrado")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-283">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-284">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-284">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="2dc3a-285">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="2dc3a-285">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="2dc3a-286">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="2dc3a-286">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="2dc3a-287">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="2dc3a-287">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="2dc3a-288">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-289">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-289">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-290">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-292">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensión de archivo")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-292">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-293">Extensión de nombre de archivo sin el punto anterior (punto).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-293">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="2dc3a-294">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="2dc3a-295">Ejemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="2dc3a-295">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-296">**FileName**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-296">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-299">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-299">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-300">Nombre de archivo sin la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-300">File name without the file name extension.</span></span>

<span data-ttu-id="2dc3a-301">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="2dc3a-302">Ejemplo: "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="2dc3a-302">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-303">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-303">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-304">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-306">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-307">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-307">Size of the file, in bytes.</span></span>

<span data-ttu-id="2dc3a-308">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="2dc3a-309">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-310">**FileType**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-310">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-311">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-313">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de archivo")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-313">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-314">Descriptor que representa el tipo de archivo (indicado por la propiedad de **extensión** ).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-314">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="2dc3a-315">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-315">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-316">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-316">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-319">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-319">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-320">Clase del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-320">Class of the file system.</span></span>

<span data-ttu-id="2dc3a-321">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-321">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-322">**FSName**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-322">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-323">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-325">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-325">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-326">Nombre del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-326">Name of the file system.</span></span>

<span data-ttu-id="2dc3a-327">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-328">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-328">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-329">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-331">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-332">Si es **true**, el archivo está oculto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-332">If **True**, the file is hidden.</span></span>

<span data-ttu-id="2dc3a-333">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-333">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-335">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-338">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-338">Date and time when the object was installed.</span></span> <span data-ttu-id="2dc3a-339">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2dc3a-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-341">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-341">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-342">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-344">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("recuento de apertura de archivos actuales")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-344">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-345">Número de "archivos abiertos" que están activos actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-345">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="2dc3a-346">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-346">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="2dc3a-347">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-348">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-348">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-349">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-351">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acceso")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-352">Fecha y hora en que se produjo el último acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-352">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="2dc3a-353">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-354">**Última**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-354">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-355">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-355">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-357">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificación")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-357">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-358">Fecha y hora en que se modificó por última vez el archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-358">Date and time that the file was last modified.</span></span>

<span data-ttu-id="2dc3a-359">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-359">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-360">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-363">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2dc3a-363">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-364">Nombre heredado que sirve como clave de una instancia de archivo lógico dentro de un sistema de archivos (proporcione nombres de ruta completos).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-364">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="2dc3a-365">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2dc3a-366">Ejemplo: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="2dc3a-366">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-367">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-368">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-370">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-371">Ruta de acceso del archivo, incluidas las barras diagonales inversas iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-371">Path of the file including leading and trailing backslashes.</span></span> <span data-ttu-id="2dc3a-372">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-372">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="2dc3a-373">Ejemplo: " \\ sistema de Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="2dc3a-373">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-374">**Puedan**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-374">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-375">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-377">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legible")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-377">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-378">Si **es true**, se puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-378">If **True**, the file can be read.</span></span>

<span data-ttu-id="2dc3a-379">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-379">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-380">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-383">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-384">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="2dc3a-385">Se puede definir el estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-385">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="2dc3a-386">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="2dc3a-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2dc3a-387">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2dc3a-388">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="2dc3a-388">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2dc3a-389">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2dc3a-390">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2dc3a-391">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2dc3a-392">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2dc3a-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2dc3a-393">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2dc3a-394">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2dc3a-395">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2dc3a-396">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2dc3a-397">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2dc3a-398">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2dc3a-399">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2dc3a-400">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2dc3a-401">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2dc3a-402">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2dc3a-403">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2dc3a-404">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2dc3a-405">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-405">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-406">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-408">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("archivo del sistema")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-408">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-409">Si es **true**, el archivo es un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-409">If **True**, the file is a system file.</span></span>

<span data-ttu-id="2dc3a-410">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dc3a-411">**Writeable (Grabable)**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-411">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dc3a-412">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2dc3a-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2dc3a-414">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("grabable")</span><span class="sxs-lookup"><span data-stu-id="2dc3a-414">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="2dc3a-415">Si **es true**, se puede escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-415">If **True**, the file can be written.</span></span>

<span data-ttu-id="2dc3a-416">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-416">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dc3a-417">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dc3a-417">Remarks</span></span>

<span data-ttu-id="2dc3a-418">La clase **CIM \_ DeviceFile** se deriva de [**\_ LogicalFile de CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2dc3a-418">The **CIM\_DeviceFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="2dc3a-419">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-419">WMI does not implement this class.</span></span>

<span data-ttu-id="2dc3a-420">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-420">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2dc3a-421">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2dc3a-421">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc3a-422">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dc3a-422">Requirements</span></span>



| <span data-ttu-id="2dc3a-423">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dc3a-423">Requirement</span></span> | <span data-ttu-id="2dc3a-424">Value</span><span class="sxs-lookup"><span data-stu-id="2dc3a-424">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc3a-425">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dc3a-425">Minimum supported client</span></span><br/> | <span data-ttu-id="2dc3a-426">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2dc3a-426">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2dc3a-427">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dc3a-427">Minimum supported server</span></span><br/> | <span data-ttu-id="2dc3a-428">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2dc3a-428">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2dc3a-429">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2dc3a-429">Namespace</span></span><br/>                | <span data-ttu-id="2dc3a-430">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2dc3a-430">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2dc3a-431">MOF</span><span class="sxs-lookup"><span data-stu-id="2dc3a-431">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2dc3a-432"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2dc3a-432"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2dc3a-433">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2dc3a-433">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dc3a-434"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dc3a-434"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc3a-435">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dc3a-435">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc3a-436">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="2dc3a-436">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

