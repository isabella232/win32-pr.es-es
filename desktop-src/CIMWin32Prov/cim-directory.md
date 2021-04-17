---
description: La \_ clase de directorio CIM representa un tipo de archivo que agrupa lógicamente los archivos de datos que contiene y proporciona información de la ruta de acceso para los archivos agrupados.
ms.assetid: a9594f53-08f0-4a47-9edc-51686c80c5ea
ms.tgt_platform: multiple
title: CIM_Directory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory
- CIM_Directory.AccessMask
- CIM_Directory.Archive
- CIM_Directory.Caption
- CIM_Directory.Compressed
- CIM_Directory.CompressionMethod
- CIM_Directory.CreationClassName
- CIM_Directory.CreationDate
- CIM_Directory.CSCreationClassName
- CIM_Directory.CSName
- CIM_Directory.Description
- CIM_Directory.Drive
- CIM_Directory.EightDotThreeFileName
- CIM_Directory.Encrypted
- CIM_Directory.EncryptionMethod
- CIM_Directory.Extension
- CIM_Directory.FileName
- CIM_Directory.FileSize
- CIM_Directory.FileType
- CIM_Directory.FSCreationClassName
- CIM_Directory.FSName
- CIM_Directory.Hidden
- CIM_Directory.InstallDate
- CIM_Directory.InUseCount
- CIM_Directory.LastAccessed
- CIM_Directory.LastModified
- CIM_Directory.Name
- CIM_Directory.Path
- CIM_Directory.Readable
- CIM_Directory.Status
- CIM_Directory.System
- CIM_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cebab65cc067018b3a57aa5f6890fffad1cb4c7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659651"
---
# <a name="cim_directory-class"></a><span data-ttu-id="b8190-103">\_Clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="b8190-103">CIM\_Directory class</span></span>

<span data-ttu-id="b8190-104">La clase de **\_ directorio CIM** representa un tipo de archivo que agrupa lógicamente los archivos de datos que contiene y proporciona información de la ruta de acceso para los archivos agrupados.</span><span class="sxs-lookup"><span data-stu-id="b8190-104">The **CIM\_Directory** class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8190-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b8190-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b8190-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b8190-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b8190-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b8190-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b8190-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8190-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8190-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C55F-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Directories (CIM)"), AMENDMENT]
class CIM_Directory : CIM_LogicalFile
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

## <a name="members"></a><span data-ttu-id="b8190-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8190-110">Members</span></span>

<span data-ttu-id="b8190-111">La clase de **\_ directorio CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b8190-111">The **CIM\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="b8190-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8190-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8190-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8190-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8190-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8190-114">Methods</span></span>

<span data-ttu-id="b8190-115">La clase de **\_ directorio CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b8190-115">The **CIM\_Directory** class has these methods.</span></span>



| <span data-ttu-id="b8190-116">Método</span><span class="sxs-lookup"><span data-stu-id="b8190-116">Method</span></span>                                                                                           | <span data-ttu-id="b8190-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8190-117">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8190-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="b8190-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)     | <span data-ttu-id="b8190-119">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="b8190-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="b8190-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="b8190-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md) | <span data-ttu-id="b8190-122">Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="b8190-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="b8190-124">**Comprimir**</span><span class="sxs-lookup"><span data-stu-id="b8190-124">**Compress**</span></span>](compress-method-in-class-cim-directory.md)                                       | <span data-ttu-id="b8190-125">Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="b8190-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="b8190-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="b8190-127">**CompressEx**</span></span>](compressex-method-in-class-cim-directory.md)                                   | <span data-ttu-id="b8190-128">Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="b8190-129">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="b8190-130">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="b8190-130">**Copy**</span></span>](copy-method-in-class-cim-directory.md)                                               | <span data-ttu-id="b8190-131">Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="b8190-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="b8190-132">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="b8190-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="b8190-133">**CopyEx**</span></span>](copyex-method-in-class-cim-directory.md)                                           | <span data-ttu-id="b8190-134">Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="b8190-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="b8190-135">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="b8190-136">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="b8190-136">**Delete**</span></span>](delete-method-in-class-cim-directory.md)                                           | <span data-ttu-id="b8190-137">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="b8190-138">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="b8190-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="b8190-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-directory.md)                                       | <span data-ttu-id="b8190-140">Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="b8190-141">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="b8190-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="b8190-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)           | <span data-ttu-id="b8190-143">Determina si el llamador tiene los permisos agregados especificados por el argumento de **permiso** .</span><span class="sxs-lookup"><span data-stu-id="b8190-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="b8190-144">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="b8190-145">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="b8190-145">**Rename**</span></span>](rename-method-in-class-cim-directory.md)                                           | <span data-ttu-id="b8190-146">Cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="b8190-147">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="b8190-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="b8190-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-directory.md)                             | <span data-ttu-id="b8190-149">Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-149">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="b8190-150">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-150">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="b8190-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="b8190-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-directory.md)                         | <span data-ttu-id="b8190-152">Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-152">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="b8190-153">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-153">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="b8190-154">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="b8190-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-directory.md)                                   | <span data-ttu-id="b8190-155">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="b8190-156">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="b8190-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="b8190-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-directory.md)                               | <span data-ttu-id="b8190-158">Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="b8190-159">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b8190-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="b8190-160">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8190-160">Properties</span></span>

<span data-ttu-id="b8190-161">La clase de **\_ directorio CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b8190-161">The **CIM\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8190-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="b8190-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-163">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8190-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-165">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("derechos de acceso")</span><span class="sxs-lookup"><span data-stu-id="b8190-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-166">Máscara de máscara que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el directorio.</span><span class="sxs-lookup"><span data-stu-id="b8190-166">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="b8190-167">Para ver los valores, consulte [**constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="b8190-167">For values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="b8190-168">En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="b8190-169">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-169">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="b8190-170">**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="b8190-170">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="b8190-171">**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="b8190-171">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="b8190-172">**Archivo \_ de ANEXAr \_ datos (archivo) o archivo \_ agregar \_ subdirectorio (directorio)** (4)</span><span class="sxs-lookup"><span data-stu-id="b8190-172">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="b8190-173">**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="b8190-173">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="b8190-174">**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="b8190-174">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="b8190-175">**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="b8190-175">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="b8190-176">**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="b8190-176">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="b8190-177">**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="b8190-177">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="b8190-178">**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="b8190-178">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="b8190-179">**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="b8190-179">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="b8190-180">**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="b8190-180">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="b8190-181">**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="b8190-181">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="b8190-182">**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="b8190-182">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="b8190-183">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="b8190-183">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8190-184">**Archivar**</span><span class="sxs-lookup"><span data-stu-id="b8190-184">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-185">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8190-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-187">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("se debe archivar")</span><span class="sxs-lookup"><span data-stu-id="b8190-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-188">Si **es true**, se debe archivar el archivo.</span><span class="sxs-lookup"><span data-stu-id="b8190-188">If **True**, the file should be archived.</span></span>

<span data-ttu-id="b8190-189">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-189">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b8190-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-193">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b8190-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-194">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-194">Short textual description of the object.</span></span>

<span data-ttu-id="b8190-195">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-196">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="b8190-196">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-197">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8190-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-199">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("comprimido")</span><span class="sxs-lookup"><span data-stu-id="b8190-199">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-200">Si es **true**, el archivo se comprime.</span><span class="sxs-lookup"><span data-stu-id="b8190-200">If **True**, the file is compressed.</span></span>

<span data-ttu-id="b8190-201">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-202">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="b8190-202">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-205">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compresión")</span><span class="sxs-lookup"><span data-stu-id="b8190-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-206">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b8190-206">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="b8190-207">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="b8190-207">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="b8190-208">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="b8190-208">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="b8190-209">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="b8190-209">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="b8190-210">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-210">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-211">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8190-211">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-212">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-214">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="b8190-214">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-215">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="b8190-215">Name of the class.</span></span>

<span data-ttu-id="b8190-216">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-216">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-217">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="b8190-217">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-218">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8190-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-220">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fecha de creación")</span><span class="sxs-lookup"><span data-stu-id="b8190-220">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-221">Fecha y hora en que se creó el archivo.</span><span class="sxs-lookup"><span data-stu-id="b8190-221">Date and time that the file was created.</span></span>

<span data-ttu-id="b8190-222">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-222">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-223">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8190-223">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-226">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase de sistema de equipo ")</span><span class="sxs-lookup"><span data-stu-id="b8190-226">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-227">Clase del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="b8190-227">Class of the computer system.</span></span>

<span data-ttu-id="b8190-228">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-228">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-229">**CSName**</span><span class="sxs-lookup"><span data-stu-id="b8190-229">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-232">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="b8190-232">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-233">Nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="b8190-233">Name of the computer system.</span></span>

<span data-ttu-id="b8190-234">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-235">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8190-235">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-236">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-238">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b8190-238">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-239">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-239">Textual description of the object.</span></span>

<span data-ttu-id="b8190-240">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-241">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="b8190-241">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-244">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="b8190-244">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-245">Letra de unidad (incluidos los dos puntos que siguen a la letra de unidad) del archivo.</span><span class="sxs-lookup"><span data-stu-id="b8190-245">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="b8190-246">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b8190-247">Ejemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="b8190-247">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="b8190-248">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="b8190-248">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-251">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo de ocho puntos tres")</span><span class="sxs-lookup"><span data-stu-id="b8190-251">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-252">Nombre de archivo compatible con DOS.</span><span class="sxs-lookup"><span data-stu-id="b8190-252">DOS-compatible file name.</span></span> <span data-ttu-id="b8190-253">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b8190-254">Ejemplo: "c: \\ programa ~ 1"</span><span class="sxs-lookup"><span data-stu-id="b8190-254">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="b8190-255">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="b8190-255">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-256">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8190-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-258">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("cifrado")</span><span class="sxs-lookup"><span data-stu-id="b8190-258">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-259">Si es **true**, el archivo está cifrado.</span><span class="sxs-lookup"><span data-stu-id="b8190-259">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="b8190-260">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-261">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="b8190-261">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-262">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-264">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de cifrado")</span><span class="sxs-lookup"><span data-stu-id="b8190-264">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-265">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b8190-265">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="b8190-266">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="b8190-266">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="b8190-267">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="b8190-267">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="b8190-268">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="b8190-268">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="b8190-269">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-270">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="b8190-270">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-271">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-273">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensión de archivo")</span><span class="sxs-lookup"><span data-stu-id="b8190-273">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-274">Extensión de nombre de archivo sin el punto anterior (punto).</span><span class="sxs-lookup"><span data-stu-id="b8190-274">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="b8190-275">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b8190-276">Ejemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="b8190-276">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="b8190-277">**FileName**</span><span class="sxs-lookup"><span data-stu-id="b8190-277">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-280">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo")</span><span class="sxs-lookup"><span data-stu-id="b8190-280">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-281">Nombre de archivo sin la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="b8190-281">File name without the file name extension.</span></span>

<span data-ttu-id="b8190-282">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b8190-283">Ejemplo: "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="b8190-283">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="b8190-284">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="b8190-284">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-285">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8190-285">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-287">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b8190-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-288">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b8190-288">Size of the file, in bytes.</span></span>

<span data-ttu-id="b8190-289">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-289">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b8190-290">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b8190-290">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-291">**FileType**</span><span class="sxs-lookup"><span data-stu-id="b8190-291">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-294">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de archivo")</span><span class="sxs-lookup"><span data-stu-id="b8190-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-295">Descriptor que representa el tipo de archivo (indicado por la propiedad de **extensión** ).</span><span class="sxs-lookup"><span data-stu-id="b8190-295">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="b8190-296">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-296">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-297">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8190-297">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-300">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="b8190-300">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-301">Clase del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="b8190-301">Class of the file system.</span></span>

<span data-ttu-id="b8190-302">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-303">**FSName**</span><span class="sxs-lookup"><span data-stu-id="b8190-303">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-306">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema de archivos ")</span><span class="sxs-lookup"><span data-stu-id="b8190-306">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-307">Nombre del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="b8190-307">Name of the file system.</span></span>

<span data-ttu-id="b8190-308">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-309">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="b8190-309">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-310">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8190-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-312">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="b8190-312">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-313">Si es **true**, el archivo está oculto.</span><span class="sxs-lookup"><span data-stu-id="b8190-313">If **True**, the file is hidden.</span></span>

<span data-ttu-id="b8190-314">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-314">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-315">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b8190-315">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-316">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8190-316">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-318">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b8190-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-319">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-319">Date and time when the object was installed.</span></span> <span data-ttu-id="b8190-320">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b8190-320">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b8190-321">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-322">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="b8190-322">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-323">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8190-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-325">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("recuento de apertura de archivos actuales")</span><span class="sxs-lookup"><span data-stu-id="b8190-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-326">Número de "archivos abiertos" que están activos actualmente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="b8190-326">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="b8190-327">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b8190-328">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b8190-328">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-329">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="b8190-329">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-330">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8190-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-332">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acceso")</span><span class="sxs-lookup"><span data-stu-id="b8190-332">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-333">Fecha y hora en que se produjo el último acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="b8190-333">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="b8190-334">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-334">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-335">**Última**</span><span class="sxs-lookup"><span data-stu-id="b8190-335">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-336">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8190-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-338">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificación")</span><span class="sxs-lookup"><span data-stu-id="b8190-338">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-339">Fecha y hora en que se modificó por última vez el archivo.</span><span class="sxs-lookup"><span data-stu-id="b8190-339">Date and time that the file was last modified.</span></span>

<span data-ttu-id="b8190-340">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-340">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-341">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b8190-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-344">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b8190-344">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b8190-345">Nombre heredado que sirve como clave de una instancia de archivo lógico dentro de un sistema de archivos (proporcione nombres de ruta completos).</span><span class="sxs-lookup"><span data-stu-id="b8190-345">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="b8190-346">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b8190-347">Ejemplo: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="b8190-347">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="b8190-348">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="b8190-348">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-351">Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="b8190-351">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-352">Ruta de acceso del archivo, incluidas las barras diagonales inversas iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="b8190-352">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="b8190-353">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b8190-354">Ejemplo: " \\ sistema de Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="b8190-354">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="b8190-355">**Puedan**</span><span class="sxs-lookup"><span data-stu-id="b8190-355">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-356">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8190-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-358">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legible")</span><span class="sxs-lookup"><span data-stu-id="b8190-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-359">Si **es true**, se puede leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="b8190-359">If **True**, the file can be read.</span></span>

<span data-ttu-id="b8190-360">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-360">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-361">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b8190-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-362">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8190-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-364">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b8190-364">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-365">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8190-365">String that indicates the current status of the object.</span></span>

<span data-ttu-id="b8190-366">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b8190-367">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b8190-367">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b8190-368">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b8190-368">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b8190-369">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b8190-369">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b8190-370">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b8190-370">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8190-371">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b8190-371">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b8190-372">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b8190-372">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b8190-373">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b8190-373">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b8190-374">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b8190-374">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b8190-375">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b8190-375">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b8190-376">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b8190-376">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b8190-377">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b8190-377">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b8190-378">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b8190-378">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b8190-379">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b8190-379">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8190-380">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="b8190-380">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-381">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8190-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-383">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("archivo del sistema")</span><span class="sxs-lookup"><span data-stu-id="b8190-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-384">Si es **true**, el archivo es un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="b8190-384">If **True**, the file is a system file.</span></span>

<span data-ttu-id="b8190-385">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-385">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8190-386">**Writeable (Grabable)**</span><span class="sxs-lookup"><span data-stu-id="b8190-386">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8190-387">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8190-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8190-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8190-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8190-389">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("grabable")</span><span class="sxs-lookup"><span data-stu-id="b8190-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="b8190-390">Si **es true**, se puede escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="b8190-390">If **True**, the file can be written.</span></span>

<span data-ttu-id="b8190-391">Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-391">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8190-392">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8190-392">Remarks</span></span>

<span data-ttu-id="b8190-393">La clase de **\_ directorio CIM** se deriva de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-393">The **CIM\_Directory** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b8190-394">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="b8190-394">WMI does not implement this class.</span></span> <span data-ttu-id="b8190-395">Para obtener más información acerca de las clases derivadas del **\_ directorio CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b8190-395">For more information about classes derived from **CIM\_Directory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b8190-396">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b8190-396">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b8190-397">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b8190-397">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8190-398">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8190-398">Requirements</span></span>



| <span data-ttu-id="b8190-399">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8190-399">Requirement</span></span> | <span data-ttu-id="b8190-400">Value</span><span class="sxs-lookup"><span data-stu-id="b8190-400">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8190-401">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8190-401">Minimum supported client</span></span><br/> | <span data-ttu-id="b8190-402">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8190-402">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8190-403">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8190-403">Minimum supported server</span></span><br/> | <span data-ttu-id="b8190-404">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8190-404">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8190-405">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8190-405">Namespace</span></span><br/>                | <span data-ttu-id="b8190-406">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b8190-406">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8190-407">MOF</span><span class="sxs-lookup"><span data-stu-id="b8190-407">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8190-408"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8190-408"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8190-409">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8190-409">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8190-410"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8190-410"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8190-411">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8190-411">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8190-412">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="b8190-412">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

