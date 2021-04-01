---
description: Win32 \_ CodecFile&\# 32; La clase WMI representa el códec de audio o vídeo instalado en el sistema del equipo.
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Win32_CodecFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile
- Win32_CodecFile.AccessMask
- Win32_CodecFile.Archive
- Win32_CodecFile.Caption
- Win32_CodecFile.Compressed
- Win32_CodecFile.CompressionMethod
- Win32_CodecFile.CreationClassName
- Win32_CodecFile.CreationDate
- Win32_CodecFile.CSCreationClassName
- Win32_CodecFile.CSName
- Win32_CodecFile.Description
- Win32_CodecFile.Drive
- Win32_CodecFile.EightDotThreeFileName
- Win32_CodecFile.Encrypted
- Win32_CodecFile.EncryptionMethod
- Win32_CodecFile.Extension
- Win32_CodecFile.FileName
- Win32_CodecFile.FileSize
- Win32_CodecFile.FileType
- Win32_CodecFile.FSCreationClassName
- Win32_CodecFile.FSName
- Win32_CodecFile.Group
- Win32_CodecFile.Hidden
- Win32_CodecFile.InstallDate
- Win32_CodecFile.InUseCount
- Win32_CodecFile.LastAccessed
- Win32_CodecFile.LastModified
- Win32_CodecFile.Manufacturer
- Win32_CodecFile.Name
- Win32_CodecFile.Path
- Win32_CodecFile.Readable
- Win32_CodecFile.Status
- Win32_CodecFile.System
- Win32_CodecFile.Version
- Win32_CodecFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc7a6073ab2841fde4492cd59ae1696aeca9f6a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153362"
---
# <a name="win32_codecfile-class"></a><span data-ttu-id="ddb10-103">\_Clase Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="ddb10-103">Win32\_CodecFile class</span></span>

<span data-ttu-id="ddb10-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CodecFile de Win32** representa el códec de audio o vídeo instalado en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-104">The **Win32\_CodecFile** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the audio or video codec installed on the computer system.</span></span> <span data-ttu-id="ddb10-105">Los códecs convierten un tipo de formato multimedia en otro, normalmente un formato comprimido a un formato sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="ddb10-105">Codecs convert one media format type to another, typically a compressed format to an uncompressed format.</span></span> <span data-ttu-id="ddb10-106">El nombre "Codec" se deriva de una combinación de comprimir y descomprimir.</span><span class="sxs-lookup"><span data-stu-id="ddb10-106">The name "codec" is derived from a combination of compress and decompress.</span></span> <span data-ttu-id="ddb10-107">Por ejemplo, un códec puede convertir un formato comprimido, como MS-ADPCM, en un formato sin comprimir, como PCM, que la mayoría del hardware de audio puede reproducir directamente.</span><span class="sxs-lookup"><span data-stu-id="ddb10-107">For example, a codec can convert a compressed format, such as MS-ADPCM, to an uncompressed format such as PCM, which most audio hardware can play directly.</span></span>

<span data-ttu-id="ddb10-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ddb10-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ddb10-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb10-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddb10-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CodecFile : CIM_DataFile
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
  string   Group;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Manufacturer;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  string   Version;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="ddb10-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ddb10-111">Members</span></span>

<span data-ttu-id="ddb10-112">La **clase \_ CodecFile de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ddb10-112">The **Win32\_CodecFile** class has these types of members:</span></span>

-   [<span data-ttu-id="ddb10-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ddb10-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="ddb10-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddb10-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ddb10-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="ddb10-115">Methods</span></span>

<span data-ttu-id="ddb10-116">La clase **Win32 \_ CodecFile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ddb10-116">The **Win32\_CodecFile** class has these methods.</span></span>



| <span data-ttu-id="ddb10-117">Método</span><span class="sxs-lookup"><span data-stu-id="ddb10-117">Method</span></span>                                                                                             | <span data-ttu-id="ddb10-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddb10-118">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddb10-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="ddb10-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-codecfile.md)     | <span data-ttu-id="ddb10-120">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-120">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="ddb10-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="ddb10-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | <span data-ttu-id="ddb10-122">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-122">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="ddb10-123">**Comprimir**</span><span class="sxs-lookup"><span data-stu-id="ddb10-123">**Compress**</span></span>](compress-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="ddb10-124">Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-124">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="ddb10-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="ddb10-125">**CompressEx**</span></span>](compressex-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="ddb10-126">Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-126">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="ddb10-127">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="ddb10-127">**Copy**</span></span>](copy-method-in-class-win32-codecfile.md)                                               | <span data-ttu-id="ddb10-128">Copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="ddb10-128">Copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                         |
| [<span data-ttu-id="ddb10-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="ddb10-129">**CopyEx**</span></span>](copyex-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="ddb10-130">Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName.</span><span class="sxs-lookup"><span data-stu-id="ddb10-130">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                    |
| [<span data-ttu-id="ddb10-131">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="ddb10-131">**Delete**</span></span>](delete-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="ddb10-132">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-132">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="ddb10-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="ddb10-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="ddb10-134">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-134">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="ddb10-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="ddb10-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-codecfile.md)           | <span data-ttu-id="ddb10-136">Determina si el llamador tiene los permisos agregados especificados por el argumento **Permission** no solo en el objeto File, sino en el recurso compartido en el que reside el archivo o directorio (si está en un recurso compartido).</span><span class="sxs-lookup"><span data-stu-id="ddb10-136">Determines whether the caller has the aggregated permissions specified by the **permission** argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="ddb10-137">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="ddb10-137">**Rename**</span></span>](rename-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="ddb10-138">Método de clase que cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="ddb10-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="ddb10-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-codecfile.md)                             | <span data-ttu-id="ddb10-140">Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-140">Obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="ddb10-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="ddb10-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-codecfile.md)                         | <span data-ttu-id="ddb10-142">Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="ddb10-143">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="ddb10-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="ddb10-144">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-144">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="ddb10-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="ddb10-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-codecfile.md)                               | <span data-ttu-id="ddb10-146">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-146">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="ddb10-147">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddb10-147">Properties</span></span>

<span data-ttu-id="ddb10-148">La **clase \_ CodecFile de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ddb10-148">The **Win32\_CodecFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddb10-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="ddb10-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddb10-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-152">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("derechos de acceso")</span><span class="sxs-lookup"><span data-stu-id="ddb10-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-153">Máscara de archivos que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el archivo de códec.</span><span class="sxs-lookup"><span data-stu-id="ddb10-153">Bitmask that represents the access rights required to access or perform specific operations on the codec file.</span></span> <span data-ttu-id="ddb10-154">Para los valores de bit, consulte [**constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="ddb10-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="ddb10-155">En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="ddb10-156">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ddb10-157">**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="ddb10-157">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="ddb10-158">**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="ddb10-158">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ddb10-159">**Archivo \_ de ANEXAr \_ datos (archivo) o archivo \_ agregar \_ subdirectorio (directorio)** (4)</span><span class="sxs-lookup"><span data-stu-id="ddb10-159">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="ddb10-160">**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="ddb10-160">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="ddb10-161">**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="ddb10-161">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="ddb10-162">**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="ddb10-162">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="ddb10-163">**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="ddb10-163">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="ddb10-164">**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="ddb10-164">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="ddb10-165">**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="ddb10-165">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="ddb10-166">**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="ddb10-166">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="ddb10-167">**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="ddb10-167">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="ddb10-168">**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="ddb10-168">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="ddb10-169">**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="ddb10-169">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="ddb10-170">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="ddb10-170">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddb10-171">**Archivar**</span><span class="sxs-lookup"><span data-stu-id="ddb10-171">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-172">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ddb10-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-174">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("se debe archivar")</span><span class="sxs-lookup"><span data-stu-id="ddb10-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-175">Si **es true**, se debe archivar el archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-175">If **True**, the file should be archived.</span></span>

<span data-ttu-id="ddb10-176">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-176">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-177">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ddb10-177">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-180">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ddb10-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-181">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-181">Short description of the object.</span></span>

<span data-ttu-id="ddb10-182">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-183">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="ddb10-183">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ddb10-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-186">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("comprimido")</span><span class="sxs-lookup"><span data-stu-id="ddb10-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-187">Si es **true**, el archivo se comprime.</span><span class="sxs-lookup"><span data-stu-id="ddb10-187">If **True**, the file is compressed.</span></span>

<span data-ttu-id="ddb10-188">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-188">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-189">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="ddb10-189">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-192">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compresión")</span><span class="sxs-lookup"><span data-stu-id="ddb10-192">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-193">Algoritmo o herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ddb10-193">Algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="ddb10-194">Si no es posible (o no desea) describir el esquema de compresión (quizás porque no se conoce), use las siguientes palabras: "Unknown" para indicar que no se sabe si el archivo lógico está comprimido o no; "Compressed" para representar que el archivo está comprimido, pero su esquema de compresión no se conoce o no se revela; y "no comprimido" para representar que el archivo lógico no está comprimido.</span><span class="sxs-lookup"><span data-stu-id="ddb10-194">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed or not; "Compressed" to represent that the file is compressed but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="ddb10-195">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ddb10-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-199">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="ddb10-199">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-200">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="ddb10-200">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="ddb10-201">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="ddb10-201">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ddb10-202">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-202">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-203">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="ddb10-203">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-204">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddb10-204">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-206">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fecha de creación")</span><span class="sxs-lookup"><span data-stu-id="ddb10-206">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-207">Fecha de creación del archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-207">File creation date.</span></span>

<span data-ttu-id="ddb10-208">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-209">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ddb10-209">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-212">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase de sistema de equipo ")</span><span class="sxs-lookup"><span data-stu-id="ddb10-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-213">Clase del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-213">Class of the computer system.</span></span>

<span data-ttu-id="ddb10-214">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-214">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-215">**CSName**</span><span class="sxs-lookup"><span data-stu-id="ddb10-215">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-218">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="ddb10-218">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-219">Cadena que representa el nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-219">String representing the name of the computer system.</span></span>

<span data-ttu-id="ddb10-220">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-221">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ddb10-221">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-224">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ MediaResources \\ \\ ICM \| Description")</span><span class="sxs-lookup"><span data-stu-id="ddb10-224">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\icm\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-225">Nombre completo del controlador del códec.</span><span class="sxs-lookup"><span data-stu-id="ddb10-225">Full name of the codec driver.</span></span> <span data-ttu-id="ddb10-226">Esta cadena está pensada para mostrarse en espacios grandes (descriptivos).</span><span class="sxs-lookup"><span data-stu-id="ddb10-226">This string is intended to be displayed in large (descriptive) spaces.</span></span>

<span data-ttu-id="ddb10-227">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ddb10-228">Ejemplo: "Convertidor PCM de Microsoft"</span><span class="sxs-lookup"><span data-stu-id="ddb10-228">Example: "Microsoft PCM Converter"</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-229">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="ddb10-229">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-232">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="ddb10-232">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-233">Letra de unidad (incluyendo dos puntos) del archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-233">Drive letter (including colon) of the file.</span></span>

<span data-ttu-id="ddb10-234">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ddb10-235">Ejemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="ddb10-235">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-236">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="ddb10-236">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-239">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo de ocho puntos tres")</span><span class="sxs-lookup"><span data-stu-id="ddb10-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-240">Nombre de archivo compatible con DOS para este archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-240">DOS-compatible file name for this file.</span></span>

<span data-ttu-id="ddb10-241">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ddb10-242">Ejemplo: "c: \\ programa ~ 1"</span><span class="sxs-lookup"><span data-stu-id="ddb10-242">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-243">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="ddb10-243">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-244">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ddb10-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-246">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("cifrado")</span><span class="sxs-lookup"><span data-stu-id="ddb10-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-247">Si es **true**, el archivo está cifrado.</span><span class="sxs-lookup"><span data-stu-id="ddb10-247">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="ddb10-248">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-248">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-249">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="ddb10-249">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-250">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-252">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de cifrado")</span><span class="sxs-lookup"><span data-stu-id="ddb10-252">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-253">Algoritmo o herramienta que se usa para cifrar el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ddb10-253">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="ddb10-254">Si no es posible (o no desea) describir el esquema de cifrado (quizás por motivos de seguridad), use las siguientes palabras: "Unknown" para representar que no se conoce si el archivo lógico está cifrado o no; "Cifrado" para representar que el archivo está cifrado, pero que el esquema de cifrado no es conocido o no se ha divulgado. y "no cifrado" para representar que el archivo lógico no está cifrado.</span><span class="sxs-lookup"><span data-stu-id="ddb10-254">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted or not; "Encrypted" to represent that the file is encrypted but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="ddb10-255">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-256">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="ddb10-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-259">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensión de archivo")</span><span class="sxs-lookup"><span data-stu-id="ddb10-259">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-260">Extensión de nombre de archivo (sin el punto).</span><span class="sxs-lookup"><span data-stu-id="ddb10-260">File name extension (without the dot).</span></span>

<span data-ttu-id="ddb10-261">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-261">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ddb10-262">Ejemplos: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="ddb10-262">Examples: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="ddb10-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-266">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo")</span><span class="sxs-lookup"><span data-stu-id="ddb10-266">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-267">Nombre (sin la extensión) del archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-267">Name (without the extension) of the file.</span></span>

<span data-ttu-id="ddb10-268">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-268">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ddb10-269">Ejemplo: "Autoexec"</span><span class="sxs-lookup"><span data-stu-id="ddb10-269">Example: "autoexec"</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="ddb10-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-271">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddb10-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-273">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ddb10-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-274">Tamaño del archivo (en bytes).</span><span class="sxs-lookup"><span data-stu-id="ddb10-274">Size of the file (in bytes).</span></span>

<span data-ttu-id="ddb10-275">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ddb10-276">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ddb10-276">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="ddb10-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-280">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de archivo")</span><span class="sxs-lookup"><span data-stu-id="ddb10-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-281">Tipo de archivo (indicado por la propiedad de **extensión** ).</span><span class="sxs-lookup"><span data-stu-id="ddb10-281">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="ddb10-282">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-283">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ddb10-283">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-286">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="ddb10-286">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-287">Clase del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="ddb10-287">Class of the file system.</span></span>

<span data-ttu-id="ddb10-288">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-289">**FSName**</span><span class="sxs-lookup"><span data-stu-id="ddb10-289">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-290">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-292">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="ddb10-292">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-293">Nombre del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="ddb10-293">Name of the file system.</span></span>

<span data-ttu-id="ddb10-294">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-295">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="ddb10-295">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-296">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-298">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ drivers. DESC")</span><span class="sxs-lookup"><span data-stu-id="ddb10-298">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\drivers.desc")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-299">Códec representado por esta clase.</span><span class="sxs-lookup"><span data-stu-id="ddb10-299">Codec represented by this class.</span></span>

<span data-ttu-id="ddb10-300">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="ddb10-300">The values are:</span></span>

<dl> <dd><span data-ttu-id="ddb10-301">Audio</span><span class="sxs-lookup"><span data-stu-id="ddb10-301">"Audio"</span></span></dd> <dd><span data-ttu-id="ddb10-302">Cámara</span><span class="sxs-lookup"><span data-stu-id="ddb10-302">"Video"</span></span></dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

<span data-ttu-id="ddb10-303">**Audio** ("audio")</span><span class="sxs-lookup"><span data-stu-id="ddb10-303">**Audio** ("Audio")</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="ddb10-304">**Vídeo** ("vídeo")</span><span class="sxs-lookup"><span data-stu-id="ddb10-304">**Video** ("Video")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddb10-305">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="ddb10-305">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-306">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ddb10-306">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-308">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="ddb10-308">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-309">Si es **true**, el archivo está oculto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-309">If **True**, the file is hidden.</span></span>

<span data-ttu-id="ddb10-310">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ddb10-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-312">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddb10-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-314">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="ddb10-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-315">Objeto instalado.</span><span class="sxs-lookup"><span data-stu-id="ddb10-315">Object was installed.</span></span> <span data-ttu-id="ddb10-316">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="ddb10-316">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ddb10-317">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-318">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="ddb10-318">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-319">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddb10-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-321">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("recuento de apertura de archivos actuales")</span><span class="sxs-lookup"><span data-stu-id="ddb10-321">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-322">Número de "archivos abiertos" que están activos actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-322">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="ddb10-323">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ddb10-324">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ddb10-324">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-325">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="ddb10-325">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-326">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddb10-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-328">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acceso")</span><span class="sxs-lookup"><span data-stu-id="ddb10-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-329">Se produjo el último acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-329">File was last accessed.</span></span>

<span data-ttu-id="ddb10-330">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-331">**Última**</span><span class="sxs-lookup"><span data-stu-id="ddb10-331">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-332">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddb10-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-334">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificación")</span><span class="sxs-lookup"><span data-stu-id="ddb10-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-335">El archivo se modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="ddb10-335">File was last modified.</span></span>

<span data-ttu-id="ddb10-336">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-337">**Le**</span><span class="sxs-lookup"><span data-stu-id="ddb10-337">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-338">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-340">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("manufacturer")</span><span class="sxs-lookup"><span data-stu-id="ddb10-340">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-341">Cadena de fabricante de un recurso de versión, si está presente.</span><span class="sxs-lookup"><span data-stu-id="ddb10-341">Manufacturer string from version resource, if one is present.</span></span>

<span data-ttu-id="ddb10-342">Esta propiedad se hereda del [**\_ archivo**](cim-datafile.md)de propiedades CIM.</span><span class="sxs-lookup"><span data-stu-id="ddb10-342">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-343">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ddb10-343">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-344">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-346">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ddb10-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-347">Nombre heredado que sirve como clave de una instancia de archivo lógico dentro de un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="ddb10-347">Inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="ddb10-348">Se deben proporcionar los nombres de ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="ddb10-348">Full path names should be provided.</span></span>

<span data-ttu-id="ddb10-349">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ddb10-350">Ejemplo: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="ddb10-350">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-351">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="ddb10-351">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-354">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="ddb10-354">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-355">Ruta de acceso del archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-355">Path of the file.</span></span> <span data-ttu-id="ddb10-356">Esto incluye barras diagonales inversas iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="ddb10-356">This includes leading and trailing backslashes.</span></span>

<span data-ttu-id="ddb10-357">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-357">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ddb10-358">Ejemplo: " \\ sistema de Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="ddb10-358">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-359">**Puedan**</span><span class="sxs-lookup"><span data-stu-id="ddb10-359">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-360">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ddb10-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-362">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legible")</span><span class="sxs-lookup"><span data-stu-id="ddb10-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-363">Se puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-363">File can be read.</span></span>

<span data-ttu-id="ddb10-364">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-364">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-365">**Estado**</span><span class="sxs-lookup"><span data-stu-id="ddb10-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-366">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-368">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ddb10-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-369">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb10-369">Current status of the object.</span></span> <span data-ttu-id="ddb10-370">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="ddb10-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ddb10-371">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="ddb10-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ddb10-372">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="ddb10-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ddb10-373">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ddb10-374">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="ddb10-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ddb10-375">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ddb10-376">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ddb10-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ddb10-377">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="ddb10-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ddb10-378">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="ddb10-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ddb10-379">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="ddb10-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ddb10-380">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="ddb10-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ddb10-381">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="ddb10-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ddb10-382">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="ddb10-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ddb10-383">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="ddb10-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ddb10-384">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="ddb10-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ddb10-385">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="ddb10-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ddb10-386">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="ddb10-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ddb10-387">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="ddb10-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ddb10-388">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="ddb10-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ddb10-389">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="ddb10-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-390">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ddb10-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-392">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("archivo del sistema")</span><span class="sxs-lookup"><span data-stu-id="ddb10-392">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-393">Si es **true**, el archivo es un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="ddb10-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="ddb10-394">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-395">**Versión**</span><span class="sxs-lookup"><span data-stu-id="ddb10-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-396">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ddb10-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-398">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("versión")</span><span class="sxs-lookup"><span data-stu-id="ddb10-398">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-399">Cadena de versión de un recurso de versión, si está presente.</span><span class="sxs-lookup"><span data-stu-id="ddb10-399">Version string from version resource, if one is present.</span></span>

<span data-ttu-id="ddb10-400">Esta propiedad se hereda del [**\_ archivo**](cim-datafile.md)de propiedades CIM.</span><span class="sxs-lookup"><span data-stu-id="ddb10-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddb10-401">**Writeable (Grabable)**</span><span class="sxs-lookup"><span data-stu-id="ddb10-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb10-402">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ddb10-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddb10-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb10-404">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("grabable")</span><span class="sxs-lookup"><span data-stu-id="ddb10-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="ddb10-405">Si **es true**, se puede escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="ddb10-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="ddb10-406">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddb10-407">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddb10-407">Remarks</span></span>

<span data-ttu-id="ddb10-408">La **clase \_ CodecFile de Win32** se deriva [**del \_ archivo de archivos CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-408">The **Win32\_CodecFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb10-409">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddb10-409">Requirements</span></span>



| <span data-ttu-id="ddb10-410">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddb10-410">Requirement</span></span> | <span data-ttu-id="ddb10-411">Value</span><span class="sxs-lookup"><span data-stu-id="ddb10-411">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb10-412">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddb10-412">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb10-413">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddb10-413">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ddb10-414">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddb10-414">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb10-415">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddb10-415">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ddb10-416">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ddb10-416">Namespace</span></span><br/>                | <span data-ttu-id="ddb10-417">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ddb10-417">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ddb10-418">MOF</span><span class="sxs-lookup"><span data-stu-id="ddb10-418">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddb10-419"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddb10-419"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddb10-420">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddb10-420">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddb10-421"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddb10-421"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb10-422">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddb10-422">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb10-423">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="ddb10-423">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

<span data-ttu-id="ddb10-424">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ddb10-424">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

