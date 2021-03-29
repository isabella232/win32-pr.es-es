---
description: La \_ clase CIM DirectorySpecification captura la estructura de directorios principal de un elemento de software. Esta clase se usa para organizar los archivos de un elemento de software en unidades administrables que se pueden reubicar en un sistema informático.
ms.assetid: faeab356-e470-477b-97d2-1a19ce1d8d21
ms.tgt_platform: multiple
title: CIM_DirectorySpecification (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification
- CIM_DirectorySpecification.CheckID
- CIM_DirectorySpecification.Caption
- CIM_DirectorySpecification.Description
- CIM_DirectorySpecification.CheckMode
- CIM_DirectorySpecification.Name
- CIM_DirectorySpecification.TargetOperatingSystem
- CIM_DirectorySpecification.Version
- CIM_DirectorySpecification.SoftwareElementID
- CIM_DirectorySpecification.SoftwareElementState
- CIM_DirectorySpecification.DirectoryPath
- CIM_DirectorySpecification.DirectoryType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a7eb6ae627c8ed9b5639e573e1d2d89132698ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153280"
---
# <a name="cim_directoryspecification-class"></a><span data-ttu-id="a9ccc-104">\_Clase DirectorySpecification de CIM</span><span class="sxs-lookup"><span data-stu-id="a9ccc-104">CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="a9ccc-105">La clase **CIM \_ DirectorySpecification** captura la estructura de directorios principal de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-105">The **CIM\_DirectorySpecification** class captures the major directory structure of a software element.</span></span> <span data-ttu-id="a9ccc-106">Esta clase se usa para organizar los archivos de un elemento de software en unidades administrables que se pueden reubicar en un sistema informático.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-106">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9ccc-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a9ccc-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a9ccc-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a9ccc-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ccc-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9ccc-111">Syntax</span></span>

``` syntax
[UUID("{A524EE6E-DB29-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_DirectorySpecification : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  string  DirectoryPath;
  uint16  DirectoryType;
};
```

## <a name="members"></a><span data-ttu-id="a9ccc-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9ccc-112">Members</span></span>

<span data-ttu-id="a9ccc-113">La clase **CIM \_ DirectorySpecification** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a9ccc-113">The **CIM\_DirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="a9ccc-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9ccc-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="a9ccc-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9ccc-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a9ccc-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9ccc-116">Methods</span></span>

<span data-ttu-id="a9ccc-117">La clase **CIM \_ DirectorySpecification** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-117">The **CIM\_DirectorySpecification** class has these methods.</span></span>



| <span data-ttu-id="a9ccc-118">Método</span><span class="sxs-lookup"><span data-stu-id="a9ccc-118">Method</span></span>                                                              | <span data-ttu-id="a9ccc-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9ccc-119">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="a9ccc-120">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-120">**Invoke**</span></span>](invoke-method-in-class-cim-directoryspecification.md) | <span data-ttu-id="a9ccc-121">Evalúa una comprobación determinada.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-121">Evaluates a particular check.</span></span> <span data-ttu-id="a9ccc-122">WMI no implementa este método.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-122">This method is not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a9ccc-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9ccc-123">Properties</span></span>

<span data-ttu-id="a9ccc-124">La clase **CIM \_ DirectorySpecification** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-124">The **CIM\_DirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9ccc-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-128">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-129">Breve descripción textual del sujeto.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-129">A short textual description of the subject.</span></span>

<span data-ttu-id="a9ccc-130">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ccc-131">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-134">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-135">Identificador que se usa junto con otras claves para identificar de forma única la comprobación.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="a9ccc-136">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ccc-137">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-140">Si es **true**, se espera que la condición exista en el entorno.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-140">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="a9ccc-141">Por ejemplo, se espera que un archivo esté en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-141">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="a9ccc-142">Si es **false**, no se espera que la condición exista.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-142">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="a9ccc-143">Por ejemplo, un archivo no se encuentra en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **false**.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-143">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="a9ccc-144">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ccc-145">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-145">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-148">Descripción de los objetos.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-148">A description of the objects.</span></span>

<span data-ttu-id="a9ccc-149">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-149">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ccc-150">**DirectoryPath**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-150">**DirectoryPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-153">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-153">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-154">Nombre del directorio.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-154">Directory name.</span></span> <span data-ttu-id="a9ccc-155">El valor proporcionado por un proveedor de la aplicación es un nombre de ruta de acceso predeterminado o recomendado.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-155">The value supplied by an application provider is a default or recommended path name.</span></span> <span data-ttu-id="a9ccc-156">El valor se puede cambiar en un entorno determinado.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-156">The value can be changed for a particular environment.</span></span>

</dd> <dt>

<span data-ttu-id="a9ccc-157">**DirectoryType**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-157">**DirectoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-158">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-160">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ubicación DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="a9ccc-160">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Location\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-161">Tipo de directorio que se describe.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-161">Type of directory being described.</span></span>

<dt>

<span id="Product_base_directory"></span><span id="product_base_directory"></span><span id="PRODUCT_BASE_DIRECTORY"></span>

<span data-ttu-id="a9ccc-162">**Directorio base del producto** (0)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-162">**Product base directory** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_executable_directory"></span><span id="product_executable_directory"></span><span id="PRODUCT_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="a9ccc-163">**Directorio ejecutable del producto** (1)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-163">**Product executable directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_library_directory"></span><span id="product_library_directory"></span><span id="PRODUCT_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="a9ccc-164">**Directorio** de la biblioteca de productos (2)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-164">**Product library directory** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_configuration_directory"></span><span id="product_configuration_directory"></span><span id="PRODUCT_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="a9ccc-165">**Directorio de configuración del producto** (3)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-165">**Product configuration directory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_include_directory"></span><span id="product_include_directory"></span><span id="PRODUCT_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="a9ccc-166">**Directorio de inclusión de productos** (4)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-166">**Product include directory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_working_directory"></span><span id="product_working_directory"></span><span id="PRODUCT_WORKING_DIRECTORY"></span>

<span data-ttu-id="a9ccc-167">**Directorio de trabajo del producto** (5)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-167">**Product working directory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_log_directory"></span><span id="product_log_directory"></span><span id="PRODUCT_LOG_DIRECTORY"></span>

<span data-ttu-id="a9ccc-168">**Directorio del registro del producto** (6)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-168">**Product log directory** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_base_directory"></span><span id="shared_base_directory"></span><span id="SHARED_BASE_DIRECTORY"></span>

<span data-ttu-id="a9ccc-169">**Directorio base compartido** (7)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-169">**Shared base directory** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_executable_directory"></span><span id="shared_executable_directory"></span><span id="SHARED_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="a9ccc-170">**Directorio ejecutable compartido** (8)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-170">**Shared executable directory** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_library_directory"></span><span id="shared_library_directory"></span><span id="SHARED_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="a9ccc-171">**Directorio de biblioteca compartida** (9)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-171">**Shared library directory** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_include_directory"></span><span id="shared_include_directory"></span><span id="SHARED_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="a9ccc-172">**Directorio de inclusión compartido** (10)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-172">**Shared include directory** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="System_base_directory"></span><span id="system_base_directory"></span><span id="SYSTEM_BASE_DIRECTORY"></span>

<span data-ttu-id="a9ccc-173">**Directorio base del sistema** (11)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-173">**System base directory** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="System_executable_directory"></span><span id="system_executable_directory"></span><span id="SYSTEM_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="a9ccc-174">**Directorio ejecutable del sistema** (12)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-174">**System executable directory** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="System_library_directory"></span><span id="system_library_directory"></span><span id="SYSTEM_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="a9ccc-175">**Directorio de la biblioteca del sistema** (13)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-175">**System library directory** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="System_configuration_directory"></span><span id="system_configuration_directory"></span><span id="SYSTEM_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="a9ccc-176">**Directorio de configuración del sistema** (14)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-176">**System configuration directory** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="System_include_directory"></span><span id="system_include_directory"></span><span id="SYSTEM_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="a9ccc-177">**Directorio de inclusión del sistema** (15)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-177">**System include directory** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="System_log_directory"></span><span id="system_log_directory"></span><span id="SYSTEM_LOG_DIRECTORY"></span>

<span data-ttu-id="a9ccc-178">**Directorio de registro del sistema** (16)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-178">**System log directory** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9ccc-179">**Otro** (17)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-179">**Other** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9ccc-180">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-183">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-184">Nombre usado para identificar el elemento de software</span><span class="sxs-lookup"><span data-stu-id="a9ccc-184">Name used to identify the software element</span></span>

<span data-ttu-id="a9ccc-185">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ccc-186">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-186">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-189">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-190">Este es un identificador de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-190">This is an identifier for this software element.</span></span>

<span data-ttu-id="a9ccc-191">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9ccc-192">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-192">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-193">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-195">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-196">El estado de elemento de software de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-196">The software element state of a software element.</span></span>

<span data-ttu-id="a9ccc-197">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-197">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="a9ccc-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-199">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-199">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="a9ccc-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-201">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-201">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="a9ccc-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-203">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-203">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="a9ccc-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-205">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-205">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a9ccc-206">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-206">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-207">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-209">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="a9ccc-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-210">Sistema operativo de destino del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-210">Target operating system of the software element.</span></span>

<span data-ttu-id="a9ccc-211">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-211">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9ccc-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9ccc-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="a9ccc-214"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-214"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-215">Mac OS</span><span class="sxs-lookup"><span data-stu-id="a9ccc-215">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="a9ccc-216"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-216"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-217">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="a9ccc-217">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="a9ccc-218"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-218"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="a9ccc-219"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-219"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="a9ccc-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="a9ccc-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-222">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="a9ccc-222">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="a9ccc-223"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-223"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-224">HP-UX</span><span class="sxs-lookup"><span data-stu-id="a9ccc-224">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="a9ccc-225"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-225"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="a9ccc-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="a9ccc-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="a9ccc-228"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-228"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="a9ccc-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-230">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="a9ccc-230">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="a9ccc-231"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-231"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="a9ccc-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-233">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="a9ccc-233">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="a9ccc-234"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-234"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-235">Windows 95</span><span class="sxs-lookup"><span data-stu-id="a9ccc-235">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="a9ccc-236"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-236"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-237">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a9ccc-237">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="a9ccc-238"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-238"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-239">Windows NT</span><span class="sxs-lookup"><span data-stu-id="a9ccc-239">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="a9ccc-240"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-240"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-241">Windows CE</span><span class="sxs-lookup"><span data-stu-id="a9ccc-241">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="a9ccc-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-243">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="a9ccc-243">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="a9ccc-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="a9ccc-245"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-245"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="a9ccc-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="a9ccc-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="a9ccc-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="a9ccc-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="a9ccc-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="a9ccc-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="a9ccc-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="a9ccc-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="a9ccc-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="a9ccc-255"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-255"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-256">Una serie</span><span class="sxs-lookup"><span data-stu-id="a9ccc-256">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="a9ccc-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-258">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="a9ccc-258">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="a9ccc-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-260">Tándem</span><span class="sxs-lookup"><span data-stu-id="a9ccc-260">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="a9ccc-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-262">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="a9ccc-262">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="a9ccc-263"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-263"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="a9ccc-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="a9ccc-265"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-265"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="a9ccc-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="a9ccc-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="a9ccc-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-269">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="a9ccc-269">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="a9ccc-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="a9ccc-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="a9ccc-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="a9ccc-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-274">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="a9ccc-274">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="a9ccc-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="a9ccc-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="a9ccc-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="a9ccc-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="a9ccc-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="a9ccc-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="a9ccc-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="a9ccc-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="a9ccc-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="a9ccc-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="a9ccc-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="a9ccc-286">Palm OS</span><span class="sxs-lookup"><span data-stu-id="a9ccc-286">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="a9ccc-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="a9ccc-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="a9ccc-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="a9ccc-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="a9ccc-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9ccc-292">**Versión**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-292">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ccc-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9ccc-295">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="a9ccc-295">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a9ccc-296">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-296">Version of the operation.</span></span>

<span data-ttu-id="a9ccc-297">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="a9ccc-297">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="a9ccc-298"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="a9ccc-298"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="a9ccc-299"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="a9ccc-299"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="a9ccc-300">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-300">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9ccc-301">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9ccc-301">Remarks</span></span>

<span data-ttu-id="a9ccc-302">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-302">WMI does not implement this class.</span></span> <span data-ttu-id="a9ccc-303">Para las clases derivadas de **CIM \_ DirectorySpecification**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-303">For classes derived from **CIM\_DirectorySpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a9ccc-304">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-304">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a9ccc-305">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-305">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ccc-306">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9ccc-306">Requirements</span></span>



| <span data-ttu-id="a9ccc-307">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ccc-307">Requirement</span></span> | <span data-ttu-id="a9ccc-308">Value</span><span class="sxs-lookup"><span data-stu-id="a9ccc-308">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ccc-309">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9ccc-309">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ccc-310">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9ccc-310">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9ccc-311">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9ccc-311">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ccc-312">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9ccc-312">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9ccc-313">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9ccc-313">Namespace</span></span><br/>                | <span data-ttu-id="a9ccc-314">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a9ccc-314">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9ccc-315">MOF</span><span class="sxs-lookup"><span data-stu-id="a9ccc-315">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9ccc-316"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9ccc-316"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9ccc-317">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9ccc-317">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9ccc-318"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9ccc-318"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ccc-319">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9ccc-319">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ccc-320">**Comprobación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a9ccc-320">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

