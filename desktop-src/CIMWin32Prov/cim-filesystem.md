---
description: La clase de sistema de archivos CIM \_ representa un archivo o un conjunto de datos local de un equipo o montado de forma remota desde un servidor de archivos.
ms.assetid: 5a54ab35-b9b6-49e6-96a8-cb2820b054eb
ms.tgt_platform: multiple
title: CIM_FileSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSystem
- CIM_FileSystem.Caption
- CIM_FileSystem.Description
- CIM_FileSystem.InstallDate
- CIM_FileSystem.Name
- CIM_FileSystem.Status
- CIM_FileSystem.AvailableSpace
- CIM_FileSystem.BlockSize
- CIM_FileSystem.CasePreserved
- CIM_FileSystem.CaseSensitive
- CIM_FileSystem.CodeSet
- CIM_FileSystem.CompressionMethod
- CIM_FileSystem.CreationClassName
- CIM_FileSystem.CSCreationClassName
- CIM_FileSystem.CSName
- CIM_FileSystem.EncryptionMethod
- CIM_FileSystem.FileSystemSize
- CIM_FileSystem.MaxFileNameLength
- CIM_FileSystem.ReadOnly
- CIM_FileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2795e76c686e8f2bb4079aee376dae397b36f510
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907293"
---
# <a name="cim_filesystem-class"></a><span data-ttu-id="f5c24-103">\_Clase FILESYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="f5c24-103">CIM\_FileSystem class</span></span>

<span data-ttu-id="f5c24-104">La clase de sistema de archivos **CIM \_** representa un archivo o un conjunto de datos local de un equipo o montado de forma remota desde un servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="f5c24-104">The **CIM\_FileSystem** class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5c24-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f5c24-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f5c24-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f5c24-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f5c24-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f5c24-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f5c24-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c24-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5c24-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4DA18760-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_FileSystem : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="f5c24-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f5c24-110">Members</span></span>

<span data-ttu-id="f5c24-111">La **clase \_ filesystem CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f5c24-111">The **CIM\_FileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="f5c24-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5c24-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5c24-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5c24-113">Properties</span></span>

<span data-ttu-id="f5c24-114">La **clase \_ filesystem CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f5c24-114">The **CIM\_FileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5c24-115">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="f5c24-115">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-116">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5c24-116">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-118">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="f5c24-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-119">Cantidad de espacio disponible, en bytes, para el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="f5c24-119">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="f5c24-120">Si es desconocido, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="f5c24-120">If unknown, enter 0.</span></span>

<span data-ttu-id="f5c24-121">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f5c24-121">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="f5c24-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-123">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5c24-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-125">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f5c24-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-126">Tamaño de bloque del sistema de archivos para el almacenamiento y la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="f5c24-126">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="f5c24-127">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f5c24-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f5c24-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-131">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f5c24-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-132">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f5c24-132">A short textual description of the object.</span></span>

<span data-ttu-id="f5c24-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5c24-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-134">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="f5c24-134">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-135">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f5c24-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-137">Si **es true**, se conserva el caso de los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="f5c24-137">If **TRUE**, the case of file names are preserved.</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-138">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="f5c24-138">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f5c24-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-141">Si **es true**, se admiten los nombres de archivo que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-141">If **TRUE**, case-sensitive file names are supported.</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-142">**Dese**</span><span class="sxs-lookup"><span data-stu-id="f5c24-142">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-143">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f5c24-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-145">Matriz que define los juegos de caracteres o la codificación admitidos por el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="f5c24-145">Array that defines the character sets or encoding supported by the file system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5c24-146">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f5c24-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f5c24-147">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f5c24-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="f5c24-148">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="f5c24-148">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="f5c24-149">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="f5c24-149">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="f5c24-150">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="f5c24-150">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="f5c24-151">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="f5c24-151">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="f5c24-152">**Código UNIX extendido** (6)</span><span class="sxs-lookup"><span data-stu-id="f5c24-152">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="f5c24-153">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="f5c24-153">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="f5c24-154">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="f5c24-154">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f5c24-155">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="f5c24-155">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-158">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="f5c24-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-159">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f5c24-159">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="f5c24-160">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="f5c24-160">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="f5c24-161">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="f5c24-161">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="f5c24-162">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="f5c24-162">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f5c24-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-166">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f5c24-166">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-167">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="f5c24-167">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f5c24-168">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="f5c24-168">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-169">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f5c24-169">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-172">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="f5c24-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-173">Ámbito del nombre de la clase de creación del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="f5c24-173">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-174">**CSName**</span><span class="sxs-lookup"><span data-stu-id="f5c24-174">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-177">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="f5c24-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-178">Ámbito del nombre del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="f5c24-178">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-179">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f5c24-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-182">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="f5c24-182">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-183">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f5c24-183">A textual description of the object.</span></span>

<span data-ttu-id="f5c24-184">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5c24-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-185">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="f5c24-185">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-188">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="f5c24-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-189">Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f5c24-189">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="f5c24-190">Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="f5c24-190">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="f5c24-191">Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado".</span><span class="sxs-lookup"><span data-stu-id="f5c24-191">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="f5c24-192">Si el archivo lógico no está cifrado, use "no cifrado".</span><span class="sxs-lookup"><span data-stu-id="f5c24-192">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-193">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="f5c24-193">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-194">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5c24-194">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-196">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f5c24-196">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-197">Tamaño del sistema de archivos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="f5c24-197">Size of the file system, in bytes.</span></span> <span data-ttu-id="f5c24-198">Si es desconocido, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="f5c24-198">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="f5c24-199">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f5c24-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f5c24-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-201">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f5c24-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-203">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="f5c24-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-204">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="f5c24-204">Indicates when the object was installed.</span></span> <span data-ttu-id="f5c24-205">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="f5c24-205">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f5c24-206">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5c24-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-207">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="f5c24-207">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-208">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5c24-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-210">Longitud máxima de un nombre de archivo en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="f5c24-210">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="f5c24-211">Un valor de 0 (cero) indica que no hay límite para la longitud del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="f5c24-211">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-212">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f5c24-212">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-215">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f5c24-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-216">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="f5c24-216">Label by which the object is known.</span></span> <span data-ttu-id="f5c24-217">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="f5c24-217">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f5c24-218">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5c24-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-219">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="f5c24-219">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-220">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f5c24-220">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-222">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="f5c24-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-223">Si es **true**, el sistema de archivos se designa como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f5c24-223">If **TRUE**, the file system is designated as read only.</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-224">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="f5c24-224">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-227">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="f5c24-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-228">Nombre de ruta de acceso u otra información que define la raíz del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="f5c24-228">Path name or other information that defines the root of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="f5c24-229">**Estado**</span><span class="sxs-lookup"><span data-stu-id="f5c24-229">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5c24-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f5c24-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5c24-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5c24-232">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f5c24-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f5c24-233">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f5c24-233">String that indicates the current status of the object.</span></span> <span data-ttu-id="f5c24-234">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="f5c24-234">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f5c24-235">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="f5c24-235">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f5c24-236">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="f5c24-236">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f5c24-237">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="f5c24-237">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f5c24-238">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="f5c24-238">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f5c24-239">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="f5c24-239">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f5c24-240">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5c24-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f5c24-241">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5c24-241">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f5c24-242">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="f5c24-242">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f5c24-243">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="f5c24-243">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f5c24-244">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f5c24-244">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5c24-245">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="f5c24-245">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f5c24-246">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="f5c24-246">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f5c24-247">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="f5c24-247">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f5c24-248">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="f5c24-248">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f5c24-249">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="f5c24-249">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f5c24-250">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="f5c24-250">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f5c24-251">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f5c24-251">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f5c24-252">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="f5c24-252">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f5c24-253">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="f5c24-253">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="f5c24-254"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f5c24-254"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f5c24-255">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5c24-255">Remarks</span></span>

<span data-ttu-id="f5c24-256">La clase de **\_ sistema de archivos CIM** se deriva de [**\_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5c24-256">The **CIM\_FileSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="f5c24-257">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f5c24-257">WMI does not implement this class.</span></span>

<span data-ttu-id="f5c24-258">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f5c24-258">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f5c24-259">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f5c24-259">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c24-260">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5c24-260">Requirements</span></span>



| <span data-ttu-id="f5c24-261">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c24-261">Requirement</span></span> | <span data-ttu-id="f5c24-262">Value</span><span class="sxs-lookup"><span data-stu-id="f5c24-262">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c24-263">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5c24-263">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c24-264">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5c24-264">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5c24-265">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5c24-265">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c24-266">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5c24-266">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5c24-267">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f5c24-267">Namespace</span></span><br/>                | <span data-ttu-id="f5c24-268">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f5c24-268">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5c24-269">MOF</span><span class="sxs-lookup"><span data-stu-id="f5c24-269">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5c24-270"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5c24-270"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5c24-271">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5c24-271">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5c24-272"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5c24-272"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c24-273">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5c24-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c24-274">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f5c24-274">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

