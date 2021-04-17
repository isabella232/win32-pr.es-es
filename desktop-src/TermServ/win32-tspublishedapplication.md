---
title: Win32_TSPublishedApplication (clase)
description: Define las aplicaciones que se ponen a disposición del uso remoto a través de RemoteApp de Windows Server 2008 R2.
ms.assetid: 5b9cb36b-3d8d-4105-acea-c79440d977fe
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplication clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSPublishedApplication de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplication
- Win32_TSPublishedApplication.Caption
- Win32_TSPublishedApplication.Description
- Win32_TSPublishedApplication.InstallDate
- Win32_TSPublishedApplication.Name
- Win32_TSPublishedApplication.Status
- Win32_TSPublishedApplication.Alias
- Win32_TSPublishedApplication.SecurityDescriptor
- Win32_TSPublishedApplication.Path
- Win32_TSPublishedApplication.PathExists
- Win32_TSPublishedApplication.VPath
- Win32_TSPublishedApplication.IconPath
- Win32_TSPublishedApplication.IconIndex
- Win32_TSPublishedApplication.IconContents
- Win32_TSPublishedApplication.CommandLineSetting
- Win32_TSPublishedApplication.RequiredCommandLine
- Win32_TSPublishedApplication.ShowInPortal
- Win32_TSPublishedApplication.RDPFileContents
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3825087d05b622818c74f011f30b325ed8ff7f60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685954"
---
# <a name="win32_tspublishedapplication-class"></a><span data-ttu-id="d8528-105">\_Clase Win32 TSPublishedApplication</span><span class="sxs-lookup"><span data-stu-id="d8528-105">Win32\_TSPublishedApplication class</span></span>

<span data-ttu-id="d8528-106">Define las aplicaciones que se ponen a disposición del uso remoto a través de RemoteApp de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="d8528-106">Defines the applications that are made available for remote use through Windows Server 2008 R2 RemoteApp.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8528-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8528-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  boolean  PathExists;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   RDPFileContents;
};
```

## <a name="members"></a><span data-ttu-id="d8528-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d8528-108">Members</span></span>

<span data-ttu-id="d8528-109">La **clase \_ TSPublishedApplication de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d8528-109">The **Win32\_TSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="d8528-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d8528-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8528-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d8528-111">Properties</span></span>

<span data-ttu-id="d8528-112">La **clase \_ TSPublishedApplication de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d8528-112">The **Win32\_TSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8528-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="d8528-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d8528-116">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="d8528-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d8528-117">El alias de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8528-117">The alias of the application.</span></span> <span data-ttu-id="d8528-118">El alias es un identificador único del programa cuyo valor predeterminado es el nombre de archivo del programa (sin la extensión).</span><span class="sxs-lookup"><span data-stu-id="d8528-118">The alias is a unique identifier for the program that defaults to the program's file name (without the extension).</span></span>

</dd> <dt>

<span data-ttu-id="d8528-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d8528-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d8528-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8528-122">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8528-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8528-123">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="d8528-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d8528-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8528-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8528-125">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="d8528-125">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-126">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d8528-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8528-128">La configuración de los argumentos de la línea de comandos para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8528-128">The command-line arguments setting for the application.</span></span> <span data-ttu-id="d8528-129">Los valores siguientes son posibles.</span><span class="sxs-lookup"><span data-stu-id="d8528-129">The following values are possible.</span></span>

<dt>

<span data-ttu-id="d8528-130">0</span><span class="sxs-lookup"><span data-stu-id="d8528-130">0</span></span>
</dt> <dd>

<span data-ttu-id="d8528-131">No se permiten argumentos de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d8528-131">Do not allow command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-132">1</span><span class="sxs-lookup"><span data-stu-id="d8528-132">1</span></span>
</dt> <dd>

<span data-ttu-id="d8528-133">Permite cualquier argumento de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d8528-133">Allow any command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-134">2</span><span class="sxs-lookup"><span data-stu-id="d8528-134">2</span></span>
</dt> <dd>

<span data-ttu-id="d8528-135">Use siempre los argumentos de línea de comandos necesarios (especificados en **RequiredCommandLine**).</span><span class="sxs-lookup"><span data-stu-id="d8528-135">Always use the required command-line arguments (specified in **RequiredCommandLine**).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d8528-136">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8528-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d8528-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8528-139">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d8528-139">Description of the object.</span></span>

<span data-ttu-id="d8528-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8528-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8528-141">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="d8528-141">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-142">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="d8528-142">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d8528-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d8528-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8528-144">El contenido de bytes del icono que corresponde a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8528-144">The byte contents of the icon that corresponds to the application.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-145">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="d8528-145">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-146">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d8528-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8528-148">Índice o identificador del icono.</span><span class="sxs-lookup"><span data-stu-id="d8528-148">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-149">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="d8528-149">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8528-152">Ruta de acceso del icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8528-152">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d8528-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-154">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d8528-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d8528-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8528-156">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="d8528-156">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d8528-157">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="d8528-157">The date the object was installed.</span></span> <span data-ttu-id="d8528-158">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="d8528-158">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d8528-159">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8528-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8528-160">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d8528-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d8528-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8528-163">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="d8528-163">The name of the object.</span></span>

<span data-ttu-id="d8528-164">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8528-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8528-165">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="d8528-165">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-167">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8528-168">Ruta de acceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8528-168">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-169">**PathExists**</span><span class="sxs-lookup"><span data-stu-id="d8528-169">**PathExists**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-170">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d8528-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d8528-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8528-172">Indica si la ruta de acceso de la aplicación es válida.</span><span class="sxs-lookup"><span data-stu-id="d8528-172">Indicates whether the application path is valid.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-173">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="d8528-173">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8528-176">Contenido del archivo RDP que corresponde a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8528-176">The contents of the RDP file that correspond to the application.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-177">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="d8528-177">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-179">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8528-180">Argumentos de línea de comandos necesarios para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8528-180">The command-line arguments that are required for the application.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-181">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d8528-181">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-183">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8528-184">Descriptor de seguridad que controla el acceso a la aplicación, en formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="d8528-184">A security descriptor that controls access to the application, in SDDL format.</span></span> <span data-ttu-id="d8528-185">Una cadena vacía implica permitir todo acceso.</span><span class="sxs-lookup"><span data-stu-id="d8528-185">An empty string implies allow all access.</span></span> <span data-ttu-id="d8528-186">Este descriptor de seguridad no admite ACE de denegación ni ACE que hagan referencia a usuarios o grupos que no son de dominio.</span><span class="sxs-lookup"><span data-stu-id="d8528-186">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-187">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="d8528-187">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-188">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d8528-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-189">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-189">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8528-190">Indica si la aplicación debe mostrarse en acceso web de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d8528-190">Indicates whether the application should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="d8528-191">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d8528-191">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d8528-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8528-194">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="d8528-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d8528-195">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d8528-195">Current status of the object.</span></span> <span data-ttu-id="d8528-196">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="d8528-196">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d8528-197">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d8528-197">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d8528-198">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="d8528-198">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d8528-199">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d8528-199">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d8528-200">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="d8528-200">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d8528-201">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8528-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d8528-202">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="d8528-202">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d8528-203">("Error")</span><span class="sxs-lookup"><span data-stu-id="d8528-203">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d8528-204">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="d8528-204">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d8528-205">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="d8528-205">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d8528-206">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d8528-206">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d8528-207">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="d8528-207">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d8528-208">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="d8528-208">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d8528-209">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="d8528-209">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8528-210">**VPath**</span><span class="sxs-lookup"><span data-stu-id="d8528-210">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8528-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d8528-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8528-212">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8528-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8528-213">Ruta de acceso virtual de la aplicación, lo que significa que se incluye la ruta de acceso con variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="d8528-213">The virtual path of the application, meaning the path with environment variables included.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8528-214">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8528-214">Remarks</span></span>

<span data-ttu-id="d8528-215">Debe ser miembro del grupo administradores para establecer las propiedades utilizando esta clase.</span><span class="sxs-lookup"><span data-stu-id="d8528-215">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="d8528-216">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d8528-216">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="d8528-217">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, que se puede establecer mediante la función com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="d8528-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="d8528-218">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="d8528-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="d8528-219">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d8528-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="d8528-220">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d8528-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d8528-221">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d8528-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d8528-222">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d8528-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d8528-223">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d8528-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8528-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8528-224">Requirements</span></span>



| <span data-ttu-id="d8528-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8528-225">Requirement</span></span> | <span data-ttu-id="d8528-226">Value</span><span class="sxs-lookup"><span data-stu-id="d8528-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8528-227">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8528-227">Minimum supported client</span></span><br/> | <span data-ttu-id="d8528-228">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d8528-228">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d8528-229">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8528-229">Minimum supported server</span></span><br/> | <span data-ttu-id="d8528-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8528-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8528-231">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d8528-231">Namespace</span></span><br/>                | <span data-ttu-id="d8528-232">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d8528-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d8528-233">MOF</span><span class="sxs-lookup"><span data-stu-id="d8528-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8528-234"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8528-234"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="d8528-235">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8528-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8528-236"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8528-236"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

