---
description: La \_ clase WMI PrinterDriver de Win32 representa los controladores para una \_ instancia de impresora de Win32.
ms.assetid: baf48bbf-60a3-4d9b-93b7-c1b22518a9c1
ms.tgt_platform: multiple
title: Win32_PrinterDriver (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver
- Win32_PrinterDriver.Caption
- Win32_PrinterDriver.ConfigFile
- Win32_PrinterDriver.CreationClassName
- Win32_PrinterDriver.DataFile
- Win32_PrinterDriver.DefaultDataType
- Win32_PrinterDriver.DependentFiles
- Win32_PrinterDriver.Description
- Win32_PrinterDriver.DriverPath
- Win32_PrinterDriver.FilePath
- Win32_PrinterDriver.HelpFile
- Win32_PrinterDriver.InfName
- Win32_PrinterDriver.InstallDate
- Win32_PrinterDriver.MonitorName
- Win32_PrinterDriver.Name
- Win32_PrinterDriver.OEMUrl
- Win32_PrinterDriver.Started
- Win32_PrinterDriver.StartMode
- Win32_PrinterDriver.Status
- Win32_PrinterDriver.SupportedPlatform
- Win32_PrinterDriver.SystemCreationClassName
- Win32_PrinterDriver.SystemName
- Win32_PrinterDriver.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 615d6561e12f67edee34e0de84dade12f250e0f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907252"
---
# <a name="win32_printerdriver-class"></a><span data-ttu-id="c2d7b-103">\_Clase Win32 PrinterDriver</span><span class="sxs-lookup"><span data-stu-id="c2d7b-103">Win32\_PrinterDriver class</span></span>

<span data-ttu-id="c2d7b-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterDriver de Win32** representa los controladores para una instancia de [**\_ impresora de Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="c2d7b-104">The **Win32\_PrinterDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the drivers for a [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="c2d7b-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas, pero excluye los métodos.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties, but excludes methods.</span></span> <span data-ttu-id="c2d7b-106">Para obtener información de referencia acerca de los métodos, vea la tabla de métodos de este tema.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-106">For reference information about methods, see the table of methods in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d7b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2d7b-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriver : CIM_Service
{
  string   Caption;
  string   ConfigFile;
  string   CreationClassName;
  string   DataFile;
  string   DefaultDataType;
  string   DependentFiles[];
  string   Description;
  string   DriverPath;
  string   FilePath;
  string   HelpFile;
  string   InfName;
  datetime InstallDate;
  string   MonitorName;
  string   Name;
  string   OEMUrl;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SupportedPlatform;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Version;
};
```

## <a name="members"></a><span data-ttu-id="c2d7b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2d7b-108">Members</span></span>

<span data-ttu-id="c2d7b-109">La **clase \_ PrinterDriver de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c2d7b-109">The **Win32\_PrinterDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="c2d7b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2d7b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c2d7b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2d7b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c2d7b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2d7b-112">Methods</span></span>

<span data-ttu-id="c2d7b-113">La clase **Win32 \_ PrinterDriver** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-113">The **Win32\_PrinterDriver** class has these methods.</span></span>



| <span data-ttu-id="c2d7b-114">Método</span><span class="sxs-lookup"><span data-stu-id="c2d7b-114">Method</span></span>                                                                           | <span data-ttu-id="c2d7b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2d7b-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="c2d7b-116">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-116">**AddPrinterDriver**</span></span>](addprinterdriver-method-in-class-win32-printerdriver.md) | <span data-ttu-id="c2d7b-117">Crea un nuevo controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-117">Creates a new printer driver.</span></span><br/> |
| [<span data-ttu-id="c2d7b-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-118">**StartService**</span></span>](startservice-method-in-class-win32-printerdriver.md)         | <span data-ttu-id="c2d7b-119">Inicia el servicio de impresión.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-119">Starts print service.</span></span><br/>         |
| [<span data-ttu-id="c2d7b-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-120">**StopService**</span></span>](stopservice-method-in-class-win32-printerdriver.md)           | <span data-ttu-id="c2d7b-121">Detiene el servicio de impresión.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-121">Stops print service.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="c2d7b-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2d7b-122">Properties</span></span>

<span data-ttu-id="c2d7b-123">La **clase \_ PrinterDriver de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-123">The **Win32\_PrinterDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2d7b-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-127">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-127">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-128">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-128">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="c2d7b-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-130">**ConfigFile**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-130">**ConfigFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-133">Archivo de configuración para este controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-133">Configuration file for this printer driver.</span></span>

<span data-ttu-id="c2d7b-134">Ejemplo: "pscrptui.dll"</span><span class="sxs-lookup"><span data-stu-id="c2d7b-134">Example: "pscrptui.dll"</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-135">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-135">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-138">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de clase")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-138">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-139">Nombre de la clase o la subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-139">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="c2d7b-140">Cuando se usa con las otras propiedades de clave de esta clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-140">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c2d7b-141">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-141">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-142">**DataFile**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-142">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-145">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( \_ archivo de archivos CIM. nombredearchivo)</span><span class="sxs-lookup"><span data-stu-id="c2d7b-145">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.FileName)</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-146">Archivo de datos para este controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-146">Data file for this printer driver.</span></span>

<span data-ttu-id="c2d7b-147">Ejemplo: "qms810. PPD"</span><span class="sxs-lookup"><span data-stu-id="c2d7b-147">Example: "qms810.ppd"</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-148">**DefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-148">**DefaultDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-151">Tipo de datos predeterminado para este controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-151">Default data type for this printer driver.</span></span>

<span data-ttu-id="c2d7b-152">Ejemplo: "EMF"</span><span class="sxs-lookup"><span data-stu-id="c2d7b-152">Example: "EMF"</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-153">**DependentFiles**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-153">**DependentFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-154">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-156">Matriz de archivos dependientes para este controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-156">Array of dependent files for this printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-160">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-160">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-161">Comentario que describe el vínculo.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-161">Comment that describes the link.</span></span>

<span data-ttu-id="c2d7b-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-163">**DriverPath**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-163">**DriverPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-166">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( \_ archivo de archivos CIM. rutaDeAcceso)</span><span class="sxs-lookup"><span data-stu-id="c2d7b-166">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.Path)</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-167">Ruta de acceso de este controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-167">Path for this printer driver.</span></span>

<span data-ttu-id="c2d7b-168">Ejemplo: "C: \\ \\ drivers \\ \\pscript.dll"</span><span class="sxs-lookup"><span data-stu-id="c2d7b-168">Example: "C:\\\\drivers\\\\pscript.dll"</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-169">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-169">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-171">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-172">Ruta de acceso al archivo INF que se está usando.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-172">Path to the INF file being used.</span></span>

<span data-ttu-id="c2d7b-173">Ejemplo: "c: \\ \\ temp \\ \\ driver"</span><span class="sxs-lookup"><span data-stu-id="c2d7b-173">Example: "c:\\\\temp\\\\driver"</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-174">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-174">**HelpFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-177">Archivo de ayuda para este controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-177">Help file for this printer driver.</span></span>

<span data-ttu-id="c2d7b-178">Ejemplo: "pscrptui. hlp"</span><span class="sxs-lookup"><span data-stu-id="c2d7b-178">Example: "pscrptui.hlp"</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-179">**InfName**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-179">**InfName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-182">Nombre del archivo INF que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-182">Name of the INF file being used.</span></span> <span data-ttu-id="c2d7b-183">El valor predeterminado es usar un archivo INF de impresora proporcionado por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-183">The default is to use an operating system provided printer INF file.</span></span> <span data-ttu-id="c2d7b-184">Si el fabricante de la impresora y no el sistema operativo proporciona directamente el controlador, se utiliza un nombre de archivo diferente.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-184">A different file name is used if the driver is provided directly by the manufacturer of the printer and not the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-185">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-185">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-186">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-188">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-188">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-189">Fecha y hora de instalación del objeto.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-189">Date and time the object is installed.</span></span> <span data-ttu-id="c2d7b-190">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-190">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c2d7b-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-192">**Nombremonitor**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-192">**MonitorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-195">Nombre del monitor de este controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-195">Name of the monitor for this printer driver.</span></span>

<span data-ttu-id="c2d7b-196">Ejemplo: "monitor PJL"</span><span class="sxs-lookup"><span data-stu-id="c2d7b-196">Example: "PJL monitor"</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-197">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-197">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-200">Calificadores: [ **clave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="c2d7b-200">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-201">Nombre del controlador de esta impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-201">Driver name for this printer.</span></span> <span data-ttu-id="c2d7b-202">Se trata de una clave compuesta formada por los valores de **nombre**, **versión** y **SupportedPlatform** .</span><span class="sxs-lookup"><span data-stu-id="c2d7b-202">This is a compound key composed of the **Name**, **Version**, and **SupportedPlatform** values.</span></span>

<span data-ttu-id="c2d7b-203">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) y invalida la definición de **nombre** en esa clase.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) and overrides the **Name** definition in that class.</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-204">**OEMUrl**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-204">**OEMUrl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-207">Vínculo de World Wide Web (WWW) al sitio web del fabricante de la impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-207">World Wide Web (WWW) link to the printer manufacturer's website.</span></span> <span data-ttu-id="c2d7b-208">Tenga en cuenta que esta propiedad no se rellena cuando se usa el archivo Win32. inf y solo es aplicable a los controladores proporcionados directamente por el fabricante.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-208">Note that this property is not populated when the Win32.inf file is used, and is only applicable for drivers provided directly from the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-209">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-209">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-210">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-212">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-212">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-213">Si es **true**, el servicio se inicia.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-213">If **TRUE**, the service is started.</span></span> <span data-ttu-id="c2d7b-214">Si es **false**, el servicio se detiene.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-214">If **FALSE**, the service is stopped.</span></span>

<span data-ttu-id="c2d7b-215">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-215">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-216">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-216">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-219">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("modo de inicio")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-219">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-220">Un sistema operativo inicia automáticamente el modo de inicio del servicio, o solo se inicia cuando se solicita.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-220">Start mode of the service is automatically started by an operating system, or only started when requested.</span></span>

<span data-ttu-id="c2d7b-221">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-221">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="c2d7b-222">Estos son los valores posibles:</span><span class="sxs-lookup"><span data-stu-id="c2d7b-222">The following are possible values:</span></span>

<dl> <dd><span data-ttu-id="c2d7b-223">Automático</span><span class="sxs-lookup"><span data-stu-id="c2d7b-223">"Automatic"</span></span></dd> <dd><span data-ttu-id="c2d7b-224">Manualmente</span><span class="sxs-lookup"><span data-stu-id="c2d7b-224">"Manual"</span></span></dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="c2d7b-225">**Automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-225">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="c2d7b-226">**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-226">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c2d7b-227">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-227">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-230">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-230">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-231">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-231">Current status of the object.</span></span> <span data-ttu-id="c2d7b-232">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-232">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c2d7b-233">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-233">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c2d7b-234">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="c2d7b-234">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c2d7b-235">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-235">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c2d7b-236">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-236">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c2d7b-237">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c2d7b-238">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2d7b-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c2d7b-239">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c2d7b-240">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c2d7b-241">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c2d7b-242">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c2d7b-243">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c2d7b-244">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c2d7b-245">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c2d7b-246">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c2d7b-247">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c2d7b-248">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c2d7b-249">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c2d7b-250">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c2d7b-251">**SupportedPlatform**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-251">**SupportedPlatform**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-254">Entornos operativos para los que está diseñado el controlador.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-254">Operating environments that the driver is intended for.</span></span>

<span data-ttu-id="c2d7b-255">Ejemplo: "Windows NT x86".</span><span class="sxs-lookup"><span data-stu-id="c2d7b-255">Example: "Windows NT x86".</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-256">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-256">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-259">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" System Class name ")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-259">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-260">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-260">Scoping system's creation class name.</span></span>

<span data-ttu-id="c2d7b-261">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-262">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-262">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-265">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre del sistema ")</span><span class="sxs-lookup"><span data-stu-id="c2d7b-265">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-266">Nombre del sistema que hospeda este servicio.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-266">Name of the system that hosts this service.</span></span>

<span data-ttu-id="c2d7b-267">Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-267">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2d7b-268">**Versión**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2d7b-269">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2d7b-270">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c2d7b-270">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c2d7b-271">Versión del sistema operativo del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-271">Operating system version for the printer driver.</span></span>

<dt>

<span id="3"></span>

<span data-ttu-id="c2d7b-272"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-272"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="c2d7b-273">2000</span><span class="sxs-lookup"><span data-stu-id="c2d7b-273">Win2k</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2d7b-274">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2d7b-274">Remarks</span></span>

<span data-ttu-id="c2d7b-275">La **clase \_ PrinterDriver de Win32** se deriva [**del \_ servicio CIM**](cim-service.md) que deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-275">The **Win32\_PrinterDriver** class is derived from [**CIM\_Service**](cim-service.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="c2d7b-276">Los usuarios pueden desinstalar un controlador de impresora eliminando una instancia de esta clase correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-276">Users can uninstall a printer driver by deleting a corresponding instance of this class.</span></span> <span data-ttu-id="c2d7b-277">Para ello, el proceso de llamada debe tener el privilegio **SeLoadDriverPrivilege** establecido para eliminar una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-277">To do so, the calling process must have the **SeLoadDriverPrivilege** privilege set to delete an instance of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="c2d7b-278">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c2d7b-278">Examples</span></span>

<span data-ttu-id="c2d7b-279">El ejemplo de VBScript [administrar impresoras y controladores de impresora](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) administra controladores y puertos de impresora.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-279">The [Manage Printer and Printer Drivers](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) VBScript sample manages printer drivers and printer ports.</span></span>

<span data-ttu-id="c2d7b-280">En la siguiente [explicación de los foros de TechNet](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) se describe cómo crear una impresora y cargar controladores desde un servidor.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-280">The following [discussion on the TechNet forums](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) describes how to create a printer and upload drivers from a server.</span></span>

<span data-ttu-id="c2d7b-281">En el siguiente ejemplo de VBScript se enumeran todos los controladores de impresora que se han instalado en un equipo.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-281">The following VBScript sample lists all the printer drivers that have been installed on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrinterDriver") 
 
For each objPrinter in colInstalledPrinters 
    Wscript.Echo "Configuration File: " & objPrinter.ConfigFile 
    Wscript.Echo "Data File: " & objPrinter.DataFile 
    Wscript.Echo "Description: " & objPrinter.Description 
    Wscript.Echo "Driver Path: " & objPrinter.DriverPath 
    Wscript.Echo "File Path: " & objPrinter.FilePath 
    Wscript.Echo "Help File: " & objPrinter.HelpFile 
    Wscript.Echo "INF Name: " & objPrinter.InfName 
    Wscript.Echo "Monitor Name: " & objPrinter.MonitorName 
    Wscript.Echo "Name: " & objPrinter.Name 
    Wscript.Echo "OEM Url: " & objPrinter.OEMUrl 
    Wscript.Echo "Supported Platform: " & objPrinter.SupportedPlatform 
    Wscript.Echo "Version: " & objPrinter.Version 
Next 
```



## <a name="requirements"></a><span data-ttu-id="c2d7b-282">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2d7b-282">Requirements</span></span>



| <span data-ttu-id="c2d7b-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2d7b-283">Requirement</span></span> | <span data-ttu-id="c2d7b-284">Value</span><span class="sxs-lookup"><span data-stu-id="c2d7b-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d7b-285">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2d7b-285">Minimum supported client</span></span><br/> | <span data-ttu-id="c2d7b-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2d7b-286">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c2d7b-287">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2d7b-287">Minimum supported server</span></span><br/> | <span data-ttu-id="c2d7b-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2d7b-288">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c2d7b-289">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c2d7b-289">Namespace</span></span><br/>                | <span data-ttu-id="c2d7b-290">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c2d7b-290">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="c2d7b-291">MOF</span><span class="sxs-lookup"><span data-stu-id="c2d7b-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2d7b-292"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2d7b-292"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2d7b-293">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2d7b-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2d7b-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2d7b-294"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c2d7b-295">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2d7b-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d7b-296">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-296">**CIM\_Service**</span></span>](./cim-service.md)
</dt> <dt>

[<span data-ttu-id="c2d7b-297">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="c2d7b-297">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
