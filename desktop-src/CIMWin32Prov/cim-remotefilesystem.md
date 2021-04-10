---
description: La \_ clase CIM RemoteFileSystem representa un sistema de archivos remoto al que se tiene acceso por medio de un servicio relacionado con la red. En este caso, el almacén de archivos está hospedado en un equipo, que actúa como servidor de archivos.
ms.assetid: 932970a8-0ab3-45d8-912d-c4ba7cf433b5
ms.tgt_platform: multiple
title: CIM_RemoteFileSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoteFileSystem
- CIM_RemoteFileSystem.AvailableSpace
- CIM_RemoteFileSystem.BlockSize
- CIM_RemoteFileSystem.Caption
- CIM_RemoteFileSystem.CasePreserved
- CIM_RemoteFileSystem.CaseSensitive
- CIM_RemoteFileSystem.CodeSet
- CIM_RemoteFileSystem.CompressionMethod
- CIM_RemoteFileSystem.CreationClassName
- CIM_RemoteFileSystem.CSCreationClassName
- CIM_RemoteFileSystem.CSName
- CIM_RemoteFileSystem.Description
- CIM_RemoteFileSystem.EncryptionMethod
- CIM_RemoteFileSystem.FileSystemSize
- CIM_RemoteFileSystem.InstallDate
- CIM_RemoteFileSystem.MaxFileNameLength
- CIM_RemoteFileSystem.Name
- CIM_RemoteFileSystem.ReadOnly
- CIM_RemoteFileSystem.Root
- CIM_RemoteFileSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c29e0212ba55b37abd734fb149d118ccc693908
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152874"
---
# <a name="cim_remotefilesystem-class"></a><span data-ttu-id="a9884-104">\_Clase RemoteFileSystem de CIM</span><span class="sxs-lookup"><span data-stu-id="a9884-104">CIM\_RemoteFileSystem class</span></span>

<span data-ttu-id="a9884-105">La clase **CIM \_ RemoteFileSystem** representa un sistema de archivos remoto al que se tiene acceso por medio de un servicio relacionado con la red.</span><span class="sxs-lookup"><span data-stu-id="a9884-105">The **CIM\_RemoteFileSystem** class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="a9884-106">En este caso, el almacén de archivos está hospedado en un equipo, que actúa como servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="a9884-106">In this case, the file store is hosted by a computer, which acts as a file server.</span></span> <span data-ttu-id="a9884-107">Por ejemplo, el almacén de archivos para un sistema de archivos NFS no suele estar en el medio controlado localmente del sistema, ni tampoco se puede acceder directamente a él a través de un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9884-107">For example, the file store for an NFS file system is typically not on a computer system's locally controlled media, nor is it directly accessed through a device driver.</span></span> <span data-ttu-id="a9884-108">Las subclases **de \_ RemoteFileSystem CIM** contienen información de configuración del lado cliente relacionada con el acceso del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a9884-108">Subclasses of **CIM\_RemoteFileSystem** contain client-side configuration information related to the access of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9884-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a9884-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a9884-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a9884-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a9884-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a9884-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a9884-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a9884-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9884-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9884-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F9-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_RemoteFileSystem : CIM_FileSystem
{
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
  datetime InstallDate;
  uint32   MaxFileNameLength;
  string   Name;
  boolean  ReadOnly;
  string   Root;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="a9884-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9884-114">Members</span></span>

<span data-ttu-id="a9884-115">La clase **CIM \_ RemoteFileSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a9884-115">The **CIM\_RemoteFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="a9884-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9884-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9884-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9884-117">Properties</span></span>

<span data-ttu-id="a9884-118">La clase **CIM \_ RemoteFileSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a9884-118">The **CIM\_RemoteFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9884-119">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="a9884-119">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-120">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9884-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-122">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="a9884-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-123">Cantidad de espacio disponible para el sistema de archivos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a9884-123">Amount of free space for the file system, in bytes.</span></span> <span data-ttu-id="a9884-124">Si es desconocido, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="a9884-124">If unknown, enter 0.</span></span>

<span data-ttu-id="a9884-125">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-125">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="a9884-126">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a9884-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-127">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="a9884-127">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9884-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-130">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="a9884-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-131">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a9884-131">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="a9884-132">Si es desconocido, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="a9884-132">If unknown, or if a block concept is not valid, (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="a9884-133">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-133">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="a9884-134">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a9884-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-135">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a9884-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-138">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a9884-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-139">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a9884-139">Textual description of the object.</span></span>

<span data-ttu-id="a9884-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-141">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="a9884-141">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a9884-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9884-144">Si **es true**, se conserva el caso de los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="a9884-144">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="a9884-145">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-145">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-146">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="a9884-146">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-147">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a9884-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9884-149">Si **es true**, se admiten los nombres de archivo que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a9884-149">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="a9884-150">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-150">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-151">**Dese**</span><span class="sxs-lookup"><span data-stu-id="a9884-151">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-152">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9884-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9884-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9884-154">Juegos de caracteres o codificación admitidos por el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a9884-154">Character sets or encoding supported by the file system.</span></span> <span data-ttu-id="a9884-155">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-155">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9884-156">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a9884-156">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9884-157">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a9884-157">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="a9884-158">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="a9884-158">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="a9884-159">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="a9884-159">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="a9884-160">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="a9884-160">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="a9884-161">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="a9884-161">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="a9884-162">**Código UNIX extendido** (6)</span><span class="sxs-lookup"><span data-stu-id="a9884-162">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="a9884-163">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="a9884-163">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="a9884-164">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="a9884-164">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9884-165">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="a9884-165">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-168">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="a9884-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-169">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a9884-169">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="a9884-170">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a9884-170">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="a9884-171">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="a9884-171">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="a9884-172">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="a9884-172">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="a9884-173">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-174">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9884-174">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-177">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9884-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9884-178">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="a9884-178">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a9884-179">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="a9884-179">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a9884-180">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-180">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-181">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9884-181">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-184">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="a9884-184">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-185">Ámbito del nombre de la clase de creación del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="a9884-185">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="a9884-186">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-186">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-187">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a9884-187">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-190">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="a9884-190">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-191">Ámbito del nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="a9884-191">Scoping computer system's name.</span></span>

<span data-ttu-id="a9884-192">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-192">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-193">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9884-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-196">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="a9884-196">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-197">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a9884-197">Textual description of the object.</span></span>

<span data-ttu-id="a9884-198">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-199">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="a9884-199">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-202">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="a9884-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-203">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a9884-203">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="a9884-204">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a9884-204">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="a9884-205">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="a9884-205">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="a9884-206">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="a9884-206">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="a9884-207">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-207">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-208">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="a9884-208">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-209">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9884-209">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-211">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="a9884-211">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-212">Tamaño total del sistema de archivos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a9884-212">Total size of the file system, in bytes.</span></span> <span data-ttu-id="a9884-213">Si es desconocido, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="a9884-213">If unknown, enter 0.</span></span>

<span data-ttu-id="a9884-214">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-214">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="a9884-215">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a9884-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-216">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a9884-216">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-217">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9884-217">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-219">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="a9884-219">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-220">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a9884-220">Date and time the object was installed.</span></span> <span data-ttu-id="a9884-221">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a9884-221">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a9884-222">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-223">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="a9884-223">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-224">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9884-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9884-226">Longitud máxima de un nombre de archivo en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a9884-226">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="a9884-227">Un valor de 0 indica que la longitud del nombre de archivo es ilimitada.</span><span class="sxs-lookup"><span data-stu-id="a9884-227">A value of 0 indicates that file name length is unlimited.</span></span>

<span data-ttu-id="a9884-228">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-228">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-229">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a9884-229">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-232">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a9884-232">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-233">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a9884-233">Label by which the object is known.</span></span> <span data-ttu-id="a9884-234">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="a9884-234">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a9884-235">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-236">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="a9884-236">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-237">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a9884-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-239">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="a9884-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-240">Si es **true**, el sistema de archivos se designa como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a9884-240">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="a9884-241">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-241">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-242">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="a9884-242">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-245">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="a9884-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-246">Nombre de ruta de acceso u otra información que define la raíz del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a9884-246">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="a9884-247">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-247">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9884-248">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a9884-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9884-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9884-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9884-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9884-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9884-251">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a9884-251">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a9884-252">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a9884-252">Current status of the object.</span></span>

<span data-ttu-id="a9884-253">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a9884-254">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a9884-254">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a9884-255">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="a9884-255">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a9884-256">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="a9884-256">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a9884-257">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a9884-257">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9884-258">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="a9884-258">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a9884-259">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a9884-259">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a9884-260">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="a9884-260">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a9884-261">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="a9884-261">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a9884-262">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="a9884-262">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a9884-263">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="a9884-263">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a9884-264">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a9884-264">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a9884-265">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="a9884-265">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a9884-266">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="a9884-266">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a9884-267"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a9884-267"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a9884-268">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9884-268">Remarks</span></span>

<span data-ttu-id="a9884-269">La clase **CIM \_ RemoteFileSystem** se deriva del [**sistema de \_ archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="a9884-269">The **CIM\_RemoteFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="a9884-270">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a9884-270">WMI does not implement this class.</span></span>

<span data-ttu-id="a9884-271">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a9884-271">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a9884-272">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a9884-272">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9884-273">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9884-273">Requirements</span></span>



| <span data-ttu-id="a9884-274">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9884-274">Requirement</span></span> | <span data-ttu-id="a9884-275">Value</span><span class="sxs-lookup"><span data-stu-id="a9884-275">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9884-276">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9884-276">Minimum supported client</span></span><br/> | <span data-ttu-id="a9884-277">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9884-277">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9884-278">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9884-278">Minimum supported server</span></span><br/> | <span data-ttu-id="a9884-279">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9884-279">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9884-280">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9884-280">Namespace</span></span><br/>                | <span data-ttu-id="a9884-281">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a9884-281">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9884-282">MOF</span><span class="sxs-lookup"><span data-stu-id="a9884-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9884-283"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9884-283"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9884-284">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9884-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9884-285"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9884-285"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9884-286">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9884-286">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9884-287">**\_Sistema de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="a9884-287">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

