---
description: La \_ clase de NFS de CIM representa un sistema de archivos remoto que se monta mediante el protocolo Network File System (NFS), desde un equipo.
ms.assetid: 24eba28f-fbd5-4aa3-a7c7-a611269d55ac
ms.tgt_platform: multiple
title: CIM_NFS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NFS
- CIM_NFS.AttributeCaching
- CIM_NFS.AttributeCachingForDirectoriesMax
- CIM_NFS.AttributeCachingForDirectoriesMin
- CIM_NFS.AttributeCachingForRegularFilesMax
- CIM_NFS.AttributeCachingForRegularFilesMin
- CIM_NFS.AvailableSpace
- CIM_NFS.BlockSize
- CIM_NFS.Caption
- CIM_NFS.CasePreserved
- CIM_NFS.CaseSensitive
- CIM_NFS.CodeSet
- CIM_NFS.CompressionMethod
- CIM_NFS.CreationClassName
- CIM_NFS.CSCreationClassName
- CIM_NFS.CSName
- CIM_NFS.Description
- CIM_NFS.EncryptionMethod
- CIM_NFS.FileSystemSize
- CIM_NFS.ForegroundMount
- CIM_NFS.HardMount
- CIM_NFS.InstallDate
- CIM_NFS.Interrupt
- CIM_NFS.MaxFileNameLength
- CIM_NFS.MountFailureRetries
- CIM_NFS.Name
- CIM_NFS.ReadBufferSize
- CIM_NFS.ReadOnly
- CIM_NFS.RetransmissionAttempts
- CIM_NFS.RetransmissionTimeout
- CIM_NFS.Root
- CIM_NFS.ServerCommunicationPort
- CIM_NFS.Status
- CIM_NFS.WriteBufferSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0dcfb44fdcd035ca47cbe3056da2a081ef2ae07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807591"
---
# <a name="cim_nfs-class"></a><span data-ttu-id="42405-103">Clase de NFS de CIM \_</span><span class="sxs-lookup"><span data-stu-id="42405-103">CIM\_NFS class</span></span>

<span data-ttu-id="42405-104">La clase de **\_ NFS de CIM** representa un sistema de archivos remoto que se monta mediante el protocolo Network File System (NFS), desde un equipo.</span><span class="sxs-lookup"><span data-stu-id="42405-104">The **CIM\_NFS** class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span> <span data-ttu-id="42405-105">Las propiedades del objeto NFS se corresponden con los aspectos operativos del montaje y representan la configuración del lado cliente para el acceso a NFS.</span><span class="sxs-lookup"><span data-stu-id="42405-105">The properties of the NFS object correspond to the operational aspects of the mount and represent the client-side configuration for NFS access.</span></span> <span data-ttu-id="42405-106">El tipo de sistema de archivos se debe establecer para indicar el tipo de sistema de archivos tal como aparece en el cliente.</span><span class="sxs-lookup"><span data-stu-id="42405-106">The file system type should be set to indicate the type of file system as it appears to the client.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42405-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="42405-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="42405-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="42405-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="42405-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="42405-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="42405-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="42405-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="42405-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42405-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FB-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_NFS : CIM_RemoteFileSystem
{
  boolean  AttributeCaching;
  uint16   AttributeCachingForDirectoriesMax;
  uint16   AttributeCachingForDirectoriesMin;
  uint16   AttributeCachingForRegularFilesMax;
  uint16   AttributeCachingForRegularFilesMin;
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  boolean  ForegroundMount;
  boolean  HardMount;
  datetime InstallDate;
  boolean  Interrupt;
  uint32   MaxFileNameLength;
  uint16   MountFailureRetries;
  string   Name;
  uint64   ReadBufferSize;
  boolean  ReadOnly;
  uint16   RetransmissionAttempts;
  uint32   RetransmissionTimeout;
  string   Root;
  uint32   ServerCommunicationPort;
  string   Status;
  uint64   WriteBufferSize;
};
```

## <a name="members"></a><span data-ttu-id="42405-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="42405-112">Members</span></span>

<span data-ttu-id="42405-113">La clase **CIM \_ NFS** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="42405-113">The **CIM\_NFS** class has these types of members:</span></span>

-   [<span data-ttu-id="42405-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42405-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42405-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42405-115">Properties</span></span>

<span data-ttu-id="42405-116">La clase **CIM \_ NFS** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="42405-116">The **CIM\_NFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42405-117">**AttributeCaching**</span><span class="sxs-lookup"><span data-stu-id="42405-117">**AttributeCaching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-118">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42405-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42405-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-120">Si es **true**, se habilita el almacenamiento en caché de atributos de control.</span><span class="sxs-lookup"><span data-stu-id="42405-120">If **TRUE**, control attribute caching is enabled.</span></span> <span data-ttu-id="42405-121">Si es **false**, se deshabilita el almacenamiento de atributos de control.</span><span class="sxs-lookup"><span data-stu-id="42405-121">If **FALSE**, control attribute caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="42405-122">**AttributeCachingForDirectoriesMax**</span><span class="sxs-lookup"><span data-stu-id="42405-122">**AttributeCachingForDirectoriesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-123">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42405-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42405-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-125">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="42405-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="42405-126">Número máximo de segundos que se mantienen los atributos almacenados en caché después de actualizar el directorio.</span><span class="sxs-lookup"><span data-stu-id="42405-126">Maximum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="42405-127">**AttributeCachingForDirectoriesMin**</span><span class="sxs-lookup"><span data-stu-id="42405-127">**AttributeCachingForDirectoriesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42405-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42405-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-130">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="42405-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="42405-131">Número mínimo de segundos que se mantienen los atributos almacenados en caché después de actualizar el directorio.</span><span class="sxs-lookup"><span data-stu-id="42405-131">Minimum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="42405-132">**AttributeCachingForRegularFilesMax**</span><span class="sxs-lookup"><span data-stu-id="42405-132">**AttributeCachingForRegularFilesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42405-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42405-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-135">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="42405-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="42405-136">Número máximo de segundos que se conservan los atributos almacenados en caché después de la modificación del archivo.</span><span class="sxs-lookup"><span data-stu-id="42405-136">Maximum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="42405-137">**AttributeCachingForRegularFilesMin**</span><span class="sxs-lookup"><span data-stu-id="42405-137">**AttributeCachingForRegularFilesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-138">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42405-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42405-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-140">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="42405-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="42405-141">Número mínimo de segundos que se conservan los atributos almacenados en caché después de la modificación del archivo.</span><span class="sxs-lookup"><span data-stu-id="42405-141">Minimum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="42405-142">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="42405-142">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-143">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42405-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42405-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-145">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="42405-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="42405-146">Cantidad total de espacio disponible, en bytes, para el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="42405-146">Total amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="42405-147">Si es desconocido, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="42405-147">If unknown, enter 0.</span></span>

<span data-ttu-id="42405-148">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-148">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="42405-149">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="42405-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="42405-150">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="42405-150">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-151">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42405-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42405-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-153">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="42405-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="42405-154">Los sistemas de archivos pueden leer o escribir datos en bloques que se definen de forma independiente de las extensiones de almacenamiento subyacentes.</span><span class="sxs-lookup"><span data-stu-id="42405-154">File systems can read or write data in blocks that are defined independently of the underlying storage extents.</span></span> <span data-ttu-id="42405-155">Esta propiedad captura el tamaño de bloque del sistema de archivos para el almacenamiento y la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="42405-155">This property captures the file system's block size for data storage and retrieval.</span></span>

<span data-ttu-id="42405-156">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-156">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="42405-157">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="42405-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="42405-158">**Caption**</span><span class="sxs-lookup"><span data-stu-id="42405-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-161">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="42405-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="42405-162">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="42405-162">Short textual description of the object.</span></span>

<span data-ttu-id="42405-163">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="42405-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-164">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="42405-164">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-165">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42405-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42405-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-167">Si **es true**, se conserva el caso de los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="42405-167">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="42405-168">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-168">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-169">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="42405-169">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-170">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42405-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42405-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-172">Si **es true**, se admiten los nombres de archivo que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="42405-172">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="42405-173">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-174">**Dese**</span><span class="sxs-lookup"><span data-stu-id="42405-174">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-175">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42405-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="42405-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-177">Juegos de caracteres o codificación admitidos por el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="42405-177">Character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="42405-178">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-178">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="42405-179">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="42405-179">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="42405-180">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="42405-180">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="42405-181">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="42405-181">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="42405-182">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="42405-182">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="42405-183">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="42405-183">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="42405-184">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="42405-184">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="42405-185">**Código UNIX extendido** (6)</span><span class="sxs-lookup"><span data-stu-id="42405-185">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="42405-186">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="42405-186">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="42405-187">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="42405-187">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="42405-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="42405-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-191">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="42405-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="42405-192">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="42405-192">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="42405-193">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="42405-193">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="42405-194">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="42405-194">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="42405-195">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="42405-195">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="42405-196">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-196">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="42405-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-200">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="42405-200">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="42405-201">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="42405-201">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="42405-202">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="42405-202">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="42405-203">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-203">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-204">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="42405-204">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-207">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="42405-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="42405-208">Ámbito del nombre de la clase de creación del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="42405-208">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="42405-209">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-209">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-210">**CSName**</span><span class="sxs-lookup"><span data-stu-id="42405-210">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-213">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="42405-213">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="42405-214">Ámbito del nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="42405-214">Scoping computer system's name.</span></span>

<span data-ttu-id="42405-215">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-215">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-216">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42405-216">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-219">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="42405-219">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="42405-220">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="42405-220">Textual description of the object.</span></span>

<span data-ttu-id="42405-221">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="42405-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-222">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="42405-222">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-225">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="42405-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="42405-226">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="42405-226">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="42405-227">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="42405-227">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="42405-228">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="42405-228">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="42405-229">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="42405-229">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="42405-230">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-230">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-231">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="42405-231">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-232">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42405-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42405-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-234">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="42405-234">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="42405-235">Tamaño total del sistema de archivos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="42405-235">Total size of the file system, in bytes.</span></span> <span data-ttu-id="42405-236">Si es desconocido, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="42405-236">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="42405-237">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-237">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="42405-238">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="42405-238">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="42405-239">**ForegroundMount**</span><span class="sxs-lookup"><span data-stu-id="42405-239">**ForegroundMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-240">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42405-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42405-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-242">Si **es true**, los reintentos se realizan en primer plano.</span><span class="sxs-lookup"><span data-stu-id="42405-242">If **TRUE**, retries are performed in the foreground.</span></span> <span data-ttu-id="42405-243">Si **es false**, y se produce un error en el primer intento de montaje, los reintentos se realizan en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="42405-243">If **FALSE**, and the first mount attempt fails, retries are performed in the background.</span></span>

</dd> <dt>

<span data-ttu-id="42405-244">**HardMount**</span><span class="sxs-lookup"><span data-stu-id="42405-244">**HardMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-245">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42405-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42405-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-247">Si es **true**, después de montar el sistema de archivos, se reintentan las solicitudes de NFS hasta que el sistema de hospedaje responde.</span><span class="sxs-lookup"><span data-stu-id="42405-247">If **TRUE**, after the file system is mounted, NFS requests are retried until the hosting system responds.</span></span> <span data-ttu-id="42405-248">Si es **false**, una vez montado el sistema de archivos, se devuelve un error si el sistema de hospedaje no responde.</span><span class="sxs-lookup"><span data-stu-id="42405-248">If **FALSE**, after the file system is mounted, an error is returned if the hosting system does not respond.</span></span>

</dd> <dt>

<span data-ttu-id="42405-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="42405-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-250">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="42405-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="42405-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-252">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="42405-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="42405-253">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="42405-253">Date and time the object was installed.</span></span> <span data-ttu-id="42405-254">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="42405-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="42405-255">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="42405-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-256">**Interrupción**</span><span class="sxs-lookup"><span data-stu-id="42405-256">**Interrupt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-257">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42405-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42405-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-259">Si **es true**, se permiten interrupciones para montajes forzados.</span><span class="sxs-lookup"><span data-stu-id="42405-259">If **TRUE**, interrupts are permitted for hard mounts.</span></span> <span data-ttu-id="42405-260">Si **es false**, las interrupciones se omiten para los montajes forzados.</span><span class="sxs-lookup"><span data-stu-id="42405-260">If **FALSE**, interrupts are ignored for hard mounts.</span></span>

</dd> <dt>

<span data-ttu-id="42405-261">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="42405-261">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-262">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42405-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42405-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-264">Longitud máxima de un nombre de archivo en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="42405-264">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="42405-265">Un valor de 0 (cero) indica que no hay límite para la longitud del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="42405-265">A value of 0 (zero)indicates that there is no limit for file name length.</span></span>

<span data-ttu-id="42405-266">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-266">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-267">**MountFailureRetries**</span><span class="sxs-lookup"><span data-stu-id="42405-267">**MountFailureRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-268">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42405-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42405-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-270">Número máximo de reintentos de error de montaje permitidos.</span><span class="sxs-lookup"><span data-stu-id="42405-270">Maximum number of mount failure retries that are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="42405-271">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="42405-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-272">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-274">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="42405-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="42405-275">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="42405-275">Label by which the object is known.</span></span> <span data-ttu-id="42405-276">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="42405-276">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="42405-277">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="42405-277">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-278">**ReadBufferSize**</span><span class="sxs-lookup"><span data-stu-id="42405-278">**ReadBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-279">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42405-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42405-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-281">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="42405-281">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="42405-282">Tamaño del búfer de lectura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="42405-282">Read buffer size, in bytes.</span></span>

<span data-ttu-id="42405-283">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="42405-283">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="42405-284">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="42405-284">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-285">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42405-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42405-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-287">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="42405-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="42405-288">Si es **true**, el sistema de archivos se designa como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="42405-288">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="42405-289">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-289">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-290">**RetransmissionAttempts**</span><span class="sxs-lookup"><span data-stu-id="42405-290">**RetransmissionAttempts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-291">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42405-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42405-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-293">Número máximo de retransmisiones NFS permitidas.</span><span class="sxs-lookup"><span data-stu-id="42405-293">Maximum number of NFS retransmissions allowed.</span></span>

</dd> <dt>

<span data-ttu-id="42405-294">**RetransmissionTimeout**</span><span class="sxs-lookup"><span data-stu-id="42405-294">**RetransmissionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-295">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42405-295">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42405-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-297">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("décimas de segundo")</span><span class="sxs-lookup"><span data-stu-id="42405-297">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of seconds")</span></span>
</dt> </dl>

<span data-ttu-id="42405-298">Tiempo de espera de NFS, en décimas de segundo.</span><span class="sxs-lookup"><span data-stu-id="42405-298">NFS time-out, in tenths of a second.</span></span>

</dd> <dt>

<span data-ttu-id="42405-299">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="42405-299">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-302">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="42405-302">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="42405-303">Nombre de ruta de acceso u otra información que define la raíz del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="42405-303">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="42405-304">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-304">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="42405-305">**ServerCommunicationPort**</span><span class="sxs-lookup"><span data-stu-id="42405-305">**ServerCommunicationPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-306">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42405-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42405-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42405-308">Número de puerto UDP del equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="42405-308">Remote computer system's UDP port number.</span></span>

</dd> <dt>

<span data-ttu-id="42405-309">**Estado**</span><span class="sxs-lookup"><span data-stu-id="42405-309">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42405-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42405-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-312">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="42405-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="42405-313">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="42405-313">Current status of the object.</span></span>

<span data-ttu-id="42405-314">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="42405-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="42405-315">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="42405-315">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="42405-316">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="42405-316">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="42405-317">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="42405-317">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="42405-318">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="42405-318">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="42405-319">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="42405-319">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="42405-320">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="42405-320">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="42405-321">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="42405-321">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="42405-322">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="42405-322">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="42405-323">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="42405-323">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="42405-324">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="42405-324">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="42405-325">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="42405-325">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="42405-326">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="42405-326">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="42405-327">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="42405-327">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="42405-328">**WriteBufferSize**</span><span class="sxs-lookup"><span data-stu-id="42405-328">**WriteBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42405-329">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42405-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42405-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42405-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42405-331">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="42405-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="42405-332">Tamaño del búfer de escritura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="42405-332">Write buffer size, in bytes.</span></span>

<span data-ttu-id="42405-333">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="42405-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42405-334">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42405-334">Remarks</span></span>

<span data-ttu-id="42405-335">La clase de **\_ NFS de CIM** se deriva de [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md).</span><span class="sxs-lookup"><span data-stu-id="42405-335">The **CIM\_NFS** class is derived from [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md).</span></span>

<span data-ttu-id="42405-336">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="42405-336">WMI does not implement this class.</span></span>

<span data-ttu-id="42405-337">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="42405-337">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="42405-338">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="42405-338">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="42405-339">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42405-339">Requirements</span></span>



| <span data-ttu-id="42405-340">Requisito</span><span class="sxs-lookup"><span data-stu-id="42405-340">Requirement</span></span> | <span data-ttu-id="42405-341">Value</span><span class="sxs-lookup"><span data-stu-id="42405-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42405-342">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42405-342">Minimum supported client</span></span><br/> | <span data-ttu-id="42405-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42405-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42405-344">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42405-344">Minimum supported server</span></span><br/> | <span data-ttu-id="42405-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42405-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42405-346">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="42405-346">Namespace</span></span><br/>                | <span data-ttu-id="42405-347">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="42405-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="42405-348">MOF</span><span class="sxs-lookup"><span data-stu-id="42405-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42405-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42405-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="42405-350">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42405-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42405-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42405-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42405-352">Vea también</span><span class="sxs-lookup"><span data-stu-id="42405-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42405-353">**\_REMOTEFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="42405-353">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> </dl>

 

