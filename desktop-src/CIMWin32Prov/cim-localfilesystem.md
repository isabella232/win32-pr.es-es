---
description: La \_ clase CIM LocalFileSystem representa el almacén de archivos controlado por un sistema informático a través de medios locales (por ejemplo, acceso directo al controlador de dispositivo).
ms.assetid: eab52a25-ca24-4a69-b030-091603d3582c
ms.tgt_platform: multiple
title: CIM_LocalFileSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LocalFileSystem
- CIM_LocalFileSystem.Caption
- CIM_LocalFileSystem.Description
- CIM_LocalFileSystem.InstallDate
- CIM_LocalFileSystem.Name
- CIM_LocalFileSystem.Status
- CIM_LocalFileSystem.AvailableSpace
- CIM_LocalFileSystem.BlockSize
- CIM_LocalFileSystem.CasePreserved
- CIM_LocalFileSystem.CaseSensitive
- CIM_LocalFileSystem.CodeSet
- CIM_LocalFileSystem.CompressionMethod
- CIM_LocalFileSystem.CreationClassName
- CIM_LocalFileSystem.CSCreationClassName
- CIM_LocalFileSystem.CSName
- CIM_LocalFileSystem.EncryptionMethod
- CIM_LocalFileSystem.FileSystemSize
- CIM_LocalFileSystem.MaxFileNameLength
- CIM_LocalFileSystem.ReadOnly
- CIM_LocalFileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a4a45541a651c92b45baba70828ba99c911d59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907284"
---
# <a name="cim_localfilesystem-class"></a><span data-ttu-id="4ad11-103">\_Clase LocalFileSystem de CIM</span><span class="sxs-lookup"><span data-stu-id="4ad11-103">CIM\_LocalFileSystem class</span></span>

<span data-ttu-id="4ad11-104">La clase **CIM \_ LocalFileSystem** representa el almacén de archivos controlado por un sistema informático a través de medios locales (por ejemplo, acceso directo al controlador de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="4ad11-104">The **CIM\_LocalFileSystem** class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="4ad11-105">El almacén de archivos se puede administrar directamente mediante el sistema del equipo, sin necesidad de que otro equipo actúe como servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ad11-105">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="4ad11-106">Sin embargo, para un sistema de archivos en clúster, el sistema de archivos es local y, por lo tanto, se pospone al clúster.</span><span class="sxs-lookup"><span data-stu-id="4ad11-106">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ad11-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4ad11-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4ad11-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4ad11-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4ad11-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4ad11-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4ad11-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4ad11-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad11-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ad11-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{5B6C820A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LocalFileSystem : CIM_FileSystem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint64   AvailableSpace;
  uint64   BlockSize;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  uint32   MaxFileNameLength;
  boolean  ReadOnly;
  string   Root;
};
```

## <a name="members"></a><span data-ttu-id="4ad11-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="4ad11-112">Members</span></span>

<span data-ttu-id="4ad11-113">La clase **CIM \_ LocalFileSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4ad11-113">The **CIM\_LocalFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="4ad11-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ad11-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ad11-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ad11-115">Properties</span></span>

<span data-ttu-id="4ad11-116">La clase **CIM \_ LocalFileSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4ad11-116">The **CIM\_LocalFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ad11-117">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="4ad11-117">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-118">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ad11-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-120">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="4ad11-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-121">Cantidad de espacio disponible, en bytes, para el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ad11-121">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="4ad11-122">Si es desconocido, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="4ad11-122">If unknown, enter 0.</span></span>

<span data-ttu-id="4ad11-123">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4ad11-123">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="4ad11-124">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-124">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-125">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="4ad11-125">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ad11-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-128">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="4ad11-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-129">Tamaño de bloque del sistema de archivos para el almacenamiento y la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="4ad11-129">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="4ad11-130">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4ad11-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="4ad11-131">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-131">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-132">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4ad11-132">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-135">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4ad11-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-136">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4ad11-136">A short textual description of the object.</span></span>

<span data-ttu-id="4ad11-137">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-138">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="4ad11-138">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4ad11-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-141">Si **es true**, se conserva el caso de los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="4ad11-141">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="4ad11-142">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-142">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-143">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="4ad11-143">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-144">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4ad11-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-146">Si **es true**, se admiten los nombres de archivo que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4ad11-146">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="4ad11-147">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-147">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-148">**Dese**</span><span class="sxs-lookup"><span data-stu-id="4ad11-148">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-149">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ad11-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-151">Matriz que define los juegos de caracteres o la codificación admitidos por el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ad11-151">Array that defines the character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="4ad11-152">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-152">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4ad11-153">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4ad11-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4ad11-154">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="4ad11-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="4ad11-155">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="4ad11-155">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="4ad11-156">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="4ad11-156">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="4ad11-157">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="4ad11-157">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="4ad11-158">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="4ad11-158">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="4ad11-159">**Código UNIX extendido** (6)</span><span class="sxs-lookup"><span data-stu-id="4ad11-159">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="4ad11-160">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="4ad11-160">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="4ad11-161">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="4ad11-161">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4ad11-162">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="4ad11-162">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-165">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="4ad11-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-166">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4ad11-166">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="4ad11-167">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="4ad11-167">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="4ad11-168">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="4ad11-168">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="4ad11-169">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="4ad11-169">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="4ad11-170">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-170">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4ad11-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-174">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4ad11-174">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-175">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="4ad11-175">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4ad11-176">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="4ad11-176">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4ad11-177">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-177">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-178">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4ad11-178">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-181">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="4ad11-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-182">Ámbito del nombre de la clase de creación del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="4ad11-182">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="4ad11-183">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-183">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-184">**CSName**</span><span class="sxs-lookup"><span data-stu-id="4ad11-184">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-187">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="4ad11-187">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-188">Ámbito del nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="4ad11-188">Scoping computer system's name.</span></span>

<span data-ttu-id="4ad11-189">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-189">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-190">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4ad11-190">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-193">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="4ad11-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-194">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4ad11-194">A textual description of the object.</span></span>

<span data-ttu-id="4ad11-195">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-196">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="4ad11-196">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-199">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="4ad11-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-200">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4ad11-200">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="4ad11-201">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="4ad11-201">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="4ad11-202">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="4ad11-202">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="4ad11-203">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="4ad11-203">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="4ad11-204">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-204">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-205">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="4ad11-205">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-206">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ad11-206">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-208">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="4ad11-208">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-209">Tamaño del sistema de archivos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="4ad11-209">Size of the file system, in bytes.</span></span> <span data-ttu-id="4ad11-210">Si es desconocido, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="4ad11-210">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="4ad11-211">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4ad11-211">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="4ad11-212">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-212">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-213">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4ad11-213">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-214">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4ad11-214">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-216">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="4ad11-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-217">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="4ad11-217">Indicates when the object was installed.</span></span> <span data-ttu-id="4ad11-218">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="4ad11-218">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4ad11-219">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-219">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-220">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="4ad11-220">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-221">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ad11-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-223">Longitud máxima de un nombre de archivo en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ad11-223">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="4ad11-224">Un valor de 0 (cero) indica que no hay límite para la longitud del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="4ad11-224">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

<span data-ttu-id="4ad11-225">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-225">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-226">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4ad11-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-229">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4ad11-229">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-230">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="4ad11-230">Label by which the object is known.</span></span> <span data-ttu-id="4ad11-231">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="4ad11-231">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4ad11-232">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-233">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="4ad11-233">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-234">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4ad11-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-236">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="4ad11-236">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-237">Si es **true**, el sistema de archivos se designa como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4ad11-237">If **TRUE**, the file system is designated as read only.</span></span>

<span data-ttu-id="4ad11-238">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-238">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-239">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="4ad11-239">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-242">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="4ad11-242">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-243">Nombre de ruta de acceso u otra información que define la raíz del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4ad11-243">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="4ad11-244">Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-244">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad11-245">**Estado**</span><span class="sxs-lookup"><span data-stu-id="4ad11-245">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad11-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4ad11-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ad11-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad11-248">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="4ad11-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4ad11-249">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4ad11-249">String that indicates the current status of the object.</span></span> <span data-ttu-id="4ad11-250">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="4ad11-250">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4ad11-251">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="4ad11-251">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4ad11-252">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="4ad11-252">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4ad11-253">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="4ad11-253">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4ad11-254">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="4ad11-254">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4ad11-255">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="4ad11-255">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4ad11-256">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4ad11-257">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4ad11-257">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4ad11-258">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="4ad11-258">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4ad11-259">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="4ad11-259">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4ad11-260">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="4ad11-260">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4ad11-261">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="4ad11-261">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4ad11-262">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="4ad11-262">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4ad11-263">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="4ad11-263">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4ad11-264">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="4ad11-264">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4ad11-265">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="4ad11-265">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4ad11-266">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="4ad11-266">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4ad11-267">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="4ad11-267">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4ad11-268">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="4ad11-268">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4ad11-269">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="4ad11-269">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="4ad11-270"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4ad11-270"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="4ad11-271">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ad11-271">Remarks</span></span>

<span data-ttu-id="4ad11-272">La clase **CIM \_ LocalFileSystem** se deriva del [**sistema de \_ archivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="4ad11-272">The **CIM\_LocalFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="4ad11-273">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="4ad11-273">WMI does not implement this class.</span></span>

<span data-ttu-id="4ad11-274">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4ad11-274">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4ad11-275">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4ad11-275">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ad11-276">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ad11-276">Requirements</span></span>



| <span data-ttu-id="4ad11-277">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ad11-277">Requirement</span></span> | <span data-ttu-id="4ad11-278">Value</span><span class="sxs-lookup"><span data-stu-id="4ad11-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad11-279">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ad11-279">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad11-280">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ad11-280">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ad11-281">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ad11-281">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad11-282">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ad11-282">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ad11-283">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ad11-283">Namespace</span></span><br/>                | <span data-ttu-id="4ad11-284">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4ad11-284">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4ad11-285">MOF</span><span class="sxs-lookup"><span data-stu-id="4ad11-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ad11-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ad11-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ad11-287">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ad11-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ad11-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ad11-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ad11-289">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ad11-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad11-290">**\_Sistema de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="4ad11-290">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

