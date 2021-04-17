---
description: La \_ clase CIM FileSpecification representa un archivo que está activado o desactivado en el sistema.
ms.assetid: 25d6cc79-1497-4615-9251-8e00524dff1b
ms.tgt_platform: multiple
title: CIM_FileSpecification (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSpecification
- CIM_FileSpecification.CheckID
- CIM_FileSpecification.Caption
- CIM_FileSpecification.Description
- CIM_FileSpecification.CheckMode
- CIM_FileSpecification.TargetOperatingSystem
- CIM_FileSpecification.Version
- CIM_FileSpecification.SoftwareElementID
- CIM_FileSpecification.SoftwareElementState
- CIM_FileSpecification.Name
- CIM_FileSpecification.CheckSum
- CIM_FileSpecification.CRC1
- CIM_FileSpecification.CRC2
- CIM_FileSpecification.CreateTimeStamp
- CIM_FileSpecification.FileSize
- CIM_FileSpecification.MD5Checksum
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 503cf9678d2be7a3afb3f8c205f0d042b4bcaec2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652335"
---
# <a name="cim_filespecification-class"></a><span data-ttu-id="2389a-103">\_Clase FileSpecification de CIM</span><span class="sxs-lookup"><span data-stu-id="2389a-103">CIM\_FileSpecification class</span></span>

<span data-ttu-id="2389a-104">La clase **CIM \_ FileSpecification** representa un archivo que está activado o desactivado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="2389a-104">The **CIM\_FileSpecification** class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="2389a-105">El archivo se encuentra en el directorio identificado por la [**Asociación \_ DirectorySpecificationFile de CIM**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2389a-105">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="2389a-106">El método [**Invoke**](invoke-method-in-class-cim-filespecification.md) usa la información para comprobar la existencia del archivo.</span><span class="sxs-lookup"><span data-stu-id="2389a-106">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="2389a-107">Tenga en cuenta que las propiedades con un valor **null** no se comprueban.</span><span class="sxs-lookup"><span data-stu-id="2389a-107">Note that properties with a **Null** value are not checked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2389a-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2389a-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2389a-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2389a-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2389a-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2389a-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2389a-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2389a-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2389a-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2389a-112">Syntax</span></span>

``` syntax
[UUID("{41F377B0-DB2A-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_FileSpecification : CIM_Check
{
  string   CheckID;
  string   Caption;
  string   Description;
  boolean  CheckMode;
  uint16   TargetOperatingSystem;
  string   Version;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Name;
  uint32   CheckSum;
  uint32   CRC1;
  uint32   CRC2;
  datetime CreateTimeStamp;
  uint64   FileSize;
  string   MD5Checksum;
};
```

## <a name="members"></a><span data-ttu-id="2389a-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="2389a-113">Members</span></span>

<span data-ttu-id="2389a-114">La clase **CIM \_ FileSpecification** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2389a-114">The **CIM\_FileSpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="2389a-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="2389a-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="2389a-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2389a-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2389a-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="2389a-117">Methods</span></span>

<span data-ttu-id="2389a-118">La clase **CIM \_ FileSpecification** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2389a-118">The **CIM\_FileSpecification** class has these methods.</span></span>



| <span data-ttu-id="2389a-119">Método</span><span class="sxs-lookup"><span data-stu-id="2389a-119">Method</span></span>                                                         | <span data-ttu-id="2389a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2389a-120">Description</span></span>                                                      |
|:---------------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="2389a-121">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="2389a-121">**Invoke**</span></span>](invoke-method-in-class-cim-filespecification.md) | <span data-ttu-id="2389a-122">Evalúa una comprobación determinada.</span><span class="sxs-lookup"><span data-stu-id="2389a-122">Evaluates a particular check.</span></span> <span data-ttu-id="2389a-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2389a-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2389a-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2389a-124">Properties</span></span>

<span data-ttu-id="2389a-125">La clase **CIM \_ FileSpecification** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2389a-125">The **CIM\_FileSpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2389a-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2389a-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2389a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-129">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2389a-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2389a-130">Breve descripción textual del sujeto.</span><span class="sxs-lookup"><span data-stu-id="2389a-130">A short textual description of the subject.</span></span>

<span data-ttu-id="2389a-131">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="2389a-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="2389a-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="2389a-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2389a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-135">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2389a-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2389a-136">Identificador que se usa junto con otras claves para identificar de forma única la comprobación.</span><span class="sxs-lookup"><span data-stu-id="2389a-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="2389a-137">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="2389a-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="2389a-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="2389a-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2389a-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2389a-141">Si es **true**, se espera que la condición exista en el entorno.</span><span class="sxs-lookup"><span data-stu-id="2389a-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="2389a-142">Por ejemplo, se espera que un archivo esté en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="2389a-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="2389a-143">Si es **false**, no se espera que la condición exista.</span><span class="sxs-lookup"><span data-stu-id="2389a-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="2389a-144">Por ejemplo, un archivo no se encuentra en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **false**.</span><span class="sxs-lookup"><span data-stu-id="2389a-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="2389a-145">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="2389a-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="2389a-146">**MD5**</span><span class="sxs-lookup"><span data-stu-id="2389a-146">**CheckSum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2389a-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-149">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Firma de software de DMTF \| \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="2389a-149">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="2389a-150">Valor calculado como la suma de 16 bits de los primeros 32 bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="2389a-150">Value calculated as the 16-bit sum of the file's first 32 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2389a-151">**CRC1**</span><span class="sxs-lookup"><span data-stu-id="2389a-151">**CRC1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2389a-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-154">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Firma de software de DMTF \| \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="2389a-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="2389a-155">Valor CRC calculado con el medio de 512 KB.</span><span class="sxs-lookup"><span data-stu-id="2389a-155">CRC value calculated using the middle 512 KB.</span></span>

</dd> <dt>

<span data-ttu-id="2389a-156">**CRC2**</span><span class="sxs-lookup"><span data-stu-id="2389a-156">**CRC2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2389a-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-159">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Firma de software de DMTF \| \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="2389a-159">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="2389a-160">Valor CRC para el medio de 512 KB del archivo, módulo 3.</span><span class="sxs-lookup"><span data-stu-id="2389a-160">CRC value for the middle 512 KB of the file, modulo 3.</span></span>

</dd> <dt>

<span data-ttu-id="2389a-161">**CreateTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="2389a-161">**CreateTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-162">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2389a-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-164">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2389a-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2389a-165">Fecha y hora de creación del archivo.</span><span class="sxs-lookup"><span data-stu-id="2389a-165">File creation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="2389a-166">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2389a-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2389a-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2389a-169">Descripción de los objetos.</span><span class="sxs-lookup"><span data-stu-id="2389a-169">A description of the objects.</span></span>

<span data-ttu-id="2389a-170">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="2389a-170">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="2389a-171">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="2389a-171">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-172">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2389a-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-174">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="2389a-174">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2389a-175">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2389a-175">Size of the file, in bytes.</span></span>

<span data-ttu-id="2389a-176">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2389a-176">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2389a-177">**MD5Checksum**</span><span class="sxs-lookup"><span data-stu-id="2389a-177">**MD5Checksum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2389a-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-180">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span><span class="sxs-lookup"><span data-stu-id="2389a-180">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span></span>
</dt> </dl>

<span data-ttu-id="2389a-181">Algoritmo para calcular una suma de comprobación de 128 bits para cualquier archivo u objeto.</span><span class="sxs-lookup"><span data-stu-id="2389a-181">Algorithm for computing a 128-bit checksum for any file or object.</span></span> <span data-ttu-id="2389a-182">La probabilidad de dos archivos diferentes que producen la misma suma de comprobación MD5 es muy pequeña (aproximadamente 1 en 2 ^ 64) y la suma de comprobación MD5 de un archivo se puede usar para construir un identificador de contenido confiable que es probable que identifique de forma única el archivo.</span><span class="sxs-lookup"><span data-stu-id="2389a-182">The likelihood of two different files producing the same MD5 checksum is very small (about 1 in 2^64), and the MD5 checksum of a file can be used to construct a reliable content identifier that is likely to uniquely identify the file.</span></span> <span data-ttu-id="2389a-183">Lo contrario también es cierto.</span><span class="sxs-lookup"><span data-stu-id="2389a-183">The reverse is also true.</span></span> <span data-ttu-id="2389a-184">Si dos archivos tienen la misma suma de comprobación MD5, es muy probable que los archivos sean idénticos.</span><span class="sxs-lookup"><span data-stu-id="2389a-184">If two files have the same MD5 checksum, it is very likely that the files are identical.</span></span> <span data-ttu-id="2389a-185">En lo que respecta a la especificación de MOF de la propiedad MD5, el algoritmo MD5 siempre genera una cadena de caracteres 32.</span><span class="sxs-lookup"><span data-stu-id="2389a-185">For purposes of MOF specification of the MD5 property, the MD5 algorithm always generates a 32-character string.</span></span> <span data-ttu-id="2389a-186">Por ejemplo, la cadena "abcdefghijklmnopqrstuvwxyz" genera la cadena "c3fcd3d76192e4007dfb496cca67e13b".</span><span class="sxs-lookup"><span data-stu-id="2389a-186">For example, the string "abcdefghijklmnopqrstuvwxyz" generates the string "c3fcd3d76192e4007dfb496cca67e13b".</span></span> <span data-ttu-id="2389a-187">Para obtener más información acerca de cómo implementar el algoritmo MD5, consulte [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span><span class="sxs-lookup"><span data-stu-id="2389a-187">For more information about implementing the MD5 algorithm, see [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span></span>

</dd> <dt>

<span data-ttu-id="2389a-188">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2389a-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2389a-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-191">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) (nombre), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2389a-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2389a-192">Nombre del archivo o nombre del archivo con un prefijo de directorio.</span><span class="sxs-lookup"><span data-stu-id="2389a-192">Either the name of the file or the name of the file with a directory prefix.</span></span>

</dd> <dt>

<span data-ttu-id="2389a-193">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="2389a-193">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2389a-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-196">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2389a-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2389a-197">Este es un identificador de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="2389a-197">This is an identifier for this software element.</span></span>

<span data-ttu-id="2389a-198">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="2389a-198">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="2389a-199">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="2389a-199">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-200">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2389a-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-202">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2389a-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2389a-203">El estado de elemento de software de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="2389a-203">The software element state of a software element.</span></span>

<span data-ttu-id="2389a-204">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="2389a-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="2389a-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="2389a-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-206">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="2389a-206">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="2389a-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="2389a-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-208">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="2389a-208">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="2389a-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="2389a-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-210">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="2389a-210">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="2389a-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="2389a-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-212">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="2389a-212">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2389a-213">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="2389a-213">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-214">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2389a-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-216">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="2389a-216">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="2389a-217">Sistema operativo de destino del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="2389a-217">Target operating system of the software element.</span></span>

<span data-ttu-id="2389a-218">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="2389a-218">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2389a-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2389a-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2389a-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2389a-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="2389a-221"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="2389a-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-222">Mac OS</span><span class="sxs-lookup"><span data-stu-id="2389a-222">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="2389a-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="2389a-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-224">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="2389a-224">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="2389a-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="2389a-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="2389a-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="2389a-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="2389a-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="2389a-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="2389a-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="2389a-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-229">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="2389a-229">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="2389a-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="2389a-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-231">HP-UX</span><span class="sxs-lookup"><span data-stu-id="2389a-231">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="2389a-232"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="2389a-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="2389a-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="2389a-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="2389a-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="2389a-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="2389a-235"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="2389a-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="2389a-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="2389a-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-237">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="2389a-237">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="2389a-238"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="2389a-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="2389a-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="2389a-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-240">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="2389a-240">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="2389a-241"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="2389a-241"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-242">Windows 95</span><span class="sxs-lookup"><span data-stu-id="2389a-242">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="2389a-243"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="2389a-243"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-244">Windows 98</span><span class="sxs-lookup"><span data-stu-id="2389a-244">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="2389a-245"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="2389a-245"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-246">Windows NT</span><span class="sxs-lookup"><span data-stu-id="2389a-246">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="2389a-247"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="2389a-247"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-248">Windows CE</span><span class="sxs-lookup"><span data-stu-id="2389a-248">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="2389a-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="2389a-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-250">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="2389a-250">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="2389a-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="2389a-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="2389a-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="2389a-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="2389a-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="2389a-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="2389a-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="2389a-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="2389a-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="2389a-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="2389a-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="2389a-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="2389a-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="2389a-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="2389a-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="2389a-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="2389a-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="2389a-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="2389a-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="2389a-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="2389a-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="2389a-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="2389a-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="2389a-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-263">Una serie</span><span class="sxs-lookup"><span data-stu-id="2389a-263">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="2389a-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="2389a-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-265">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="2389a-265">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="2389a-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="2389a-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-267">Tándem</span><span class="sxs-lookup"><span data-stu-id="2389a-267">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="2389a-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="2389a-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-269">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="2389a-269">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="2389a-270"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="2389a-270"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="2389a-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="2389a-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="2389a-272"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="2389a-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="2389a-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="2389a-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="2389a-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="2389a-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="2389a-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="2389a-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-276">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="2389a-276">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="2389a-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="2389a-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="2389a-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="2389a-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="2389a-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="2389a-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="2389a-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="2389a-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-281">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="2389a-281">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="2389a-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="2389a-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="2389a-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="2389a-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="2389a-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="2389a-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="2389a-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="2389a-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="2389a-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="2389a-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="2389a-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="2389a-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="2389a-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="2389a-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="2389a-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="2389a-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="2389a-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="2389a-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="2389a-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="2389a-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="2389a-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="2389a-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="2389a-293">Palm OS</span><span class="sxs-lookup"><span data-stu-id="2389a-293">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="2389a-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="2389a-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="2389a-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="2389a-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="2389a-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="2389a-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="2389a-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="2389a-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="2389a-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="2389a-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2389a-299">**Versión**</span><span class="sxs-lookup"><span data-stu-id="2389a-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389a-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2389a-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2389a-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2389a-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2389a-302">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="2389a-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2389a-303">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="2389a-303">Version of the operation.</span></span>

<span data-ttu-id="2389a-304">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="2389a-304">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="2389a-305"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="2389a-305"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="2389a-306"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="2389a-306"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="2389a-307">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="2389a-307">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2389a-308">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2389a-308">Remarks</span></span>

<span data-ttu-id="2389a-309">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2389a-309">WMI does not implement this class.</span></span> <span data-ttu-id="2389a-310">Para las clases derivadas de **CIM \_ FileSpecification**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2389a-310">For classes derived from **CIM\_FileSpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2389a-311">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2389a-311">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2389a-312">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2389a-312">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2389a-313">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2389a-313">Requirements</span></span>



| <span data-ttu-id="2389a-314">Requisito</span><span class="sxs-lookup"><span data-stu-id="2389a-314">Requirement</span></span> | <span data-ttu-id="2389a-315">Value</span><span class="sxs-lookup"><span data-stu-id="2389a-315">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2389a-316">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2389a-316">Minimum supported client</span></span><br/> | <span data-ttu-id="2389a-317">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2389a-317">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2389a-318">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2389a-318">Minimum supported server</span></span><br/> | <span data-ttu-id="2389a-319">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2389a-319">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2389a-320">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2389a-320">Namespace</span></span><br/>                | <span data-ttu-id="2389a-321">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2389a-321">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2389a-322">MOF</span><span class="sxs-lookup"><span data-stu-id="2389a-322">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2389a-323"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2389a-323"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2389a-324">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2389a-324">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2389a-325"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2389a-325"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2389a-326">Vea también</span><span class="sxs-lookup"><span data-stu-id="2389a-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2389a-327">**Comprobación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2389a-327">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

