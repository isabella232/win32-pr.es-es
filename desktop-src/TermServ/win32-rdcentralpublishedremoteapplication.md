---
title: Win32_RDCentralPublishedRemoteApplication (clase)
description: Describe una aplicación publicada en otro equipo, para su uso remoto a través de Terminal Services.
ms.assetid: 8605bd1e-e825-4fd9-b14f-9d3bdac489f1
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedRemoteApplication clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDCentralPublishedRemoteApplication de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteApplication
- Win32_RDCentralPublishedRemoteApplication.Caption
- Win32_RDCentralPublishedRemoteApplication.Description
- Win32_RDCentralPublishedRemoteApplication.InstallDate
- Win32_RDCentralPublishedRemoteApplication.Name
- Win32_RDCentralPublishedRemoteApplication.Status
- Win32_RDCentralPublishedRemoteApplication.PublishingFarm
- Win32_RDCentralPublishedRemoteApplication.Alias
- Win32_RDCentralPublishedRemoteApplication.SecurityDescriptor
- Win32_RDCentralPublishedRemoteApplication.Path
- Win32_RDCentralPublishedRemoteApplication.VPath
- Win32_RDCentralPublishedRemoteApplication.IconContents
- Win32_RDCentralPublishedRemoteApplication.CommandLineSetting
- Win32_RDCentralPublishedRemoteApplication.RequiredCommandLine
- Win32_RDCentralPublishedRemoteApplication.ShowInPortal
- Win32_RDCentralPublishedRemoteApplication.AppID
- Win32_RDCentralPublishedRemoteApplication.RDPFileContents
- Win32_RDCentralPublishedRemoteApplication.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd837f62d8d0787d992e8eed7316ed1ef3f199ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996256"
---
# <a name="win32_rdcentralpublishedremoteapplication-class"></a><span data-ttu-id="e97c4-105">\_Clase Win32 RDCentralPublishedRemoteApplication</span><span class="sxs-lookup"><span data-stu-id="e97c4-105">Win32\_RDCentralPublishedRemoteApplication class</span></span>

<span data-ttu-id="e97c4-106">Describe una aplicación publicada en otro equipo, para su uso remoto a través de Terminal Services.</span><span class="sxs-lookup"><span data-stu-id="e97c4-106">Describes an application published on another computer, for remote use through Terminal Services.</span></span>

<span data-ttu-id="e97c4-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e97c4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e97c4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e97c4-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  string   VPath;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   AppID;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="e97c4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e97c4-109">Members</span></span>

<span data-ttu-id="e97c4-110">La **clase \_ RDCentralPublishedRemoteApplication de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e97c4-110">The **Win32\_RDCentralPublishedRemoteApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="e97c4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e97c4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e97c4-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e97c4-112">Properties</span></span>

<span data-ttu-id="e97c4-113">La **clase \_ RDCentralPublishedRemoteApplication de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e97c4-113">The **Win32\_RDCentralPublishedRemoteApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e97c4-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="e97c4-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-117">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e97c4-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-118">Alias de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e97c4-118">Alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-119">**AppID**</span><span class="sxs-lookup"><span data-stu-id="e97c4-119">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-122">AppID se usa para el anclaje en los clientes.</span><span class="sxs-lookup"><span data-stu-id="e97c4-122">AppID is used for pinning on the clients.</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e97c4-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e97c4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-126">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e97c4-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-127">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="e97c4-127">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e97c4-128">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e97c4-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-129">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="e97c4-129">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e97c4-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-132">Indica si se requieren argumentos de línea de comandos para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e97c4-132">Whether command-line arguments are required for this application.</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="e97c4-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span><span class="sxs-lookup"><span data-stu-id="e97c4-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e97c4-134">No permitir</span><span class="sxs-lookup"><span data-stu-id="e97c4-134">Do not allow</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="e97c4-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Permitir** (1)</span><span class="sxs-lookup"><span data-stu-id="e97c4-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="e97c4-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Requerir** (2)</span><span class="sxs-lookup"><span data-stu-id="e97c4-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e97c4-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e97c4-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e97c4-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-140">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e97c4-140">Description of the object.</span></span>

<span data-ttu-id="e97c4-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e97c4-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-142">**Carpetas**</span><span class="sxs-lookup"><span data-stu-id="e97c4-142">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-143">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e97c4-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-145">Lista de las carpetas en las que se debe mostrar este recurso.</span><span class="sxs-lookup"><span data-stu-id="e97c4-145">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-146">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="e97c4-146">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-147">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="e97c4-147">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-149">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e97c4-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-150">Contenido del icono correspondiente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e97c4-150">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e97c4-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-152">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e97c4-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e97c4-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-154">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="e97c4-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-155">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="e97c4-155">The date the object was installed.</span></span> <span data-ttu-id="e97c4-156">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="e97c4-156">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e97c4-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e97c4-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-158">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e97c4-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e97c4-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-161">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="e97c4-161">The name of the object.</span></span>

<span data-ttu-id="e97c4-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e97c4-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-163">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="e97c4-163">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-166">Ruta de acceso a la aplicación</span><span class="sxs-lookup"><span data-stu-id="e97c4-166">Path to the application</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-167">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="e97c4-167">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-170">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e97c4-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-171">Alias de la granja que publicó la aplicación</span><span class="sxs-lookup"><span data-stu-id="e97c4-171">Alias of the farm that published the Application</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-172">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="e97c4-172">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e97c4-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-175">Contenido del archivo RDP correspondiente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e97c4-175">Contents of the RDP file corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-176">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="e97c4-176">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-179">Argumentos de línea de comandos necesarios para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e97c4-179">Command-line arguments required for this application.</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-180">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e97c4-180">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-182">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-183">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e97c4-183">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-184">Descriptor de seguridad que controla el acceso a la aplicación, en formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="e97c4-184">Security Descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="e97c4-185">Una cadena vacía implica permitir todo acceso.</span><span class="sxs-lookup"><span data-stu-id="e97c4-185">Empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-186">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="e97c4-186">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-187">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e97c4-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-188">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-189">**true** si esta aplicación debe mostrarse en el acceso web de TS; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e97c4-189">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="e97c4-190">**Estado**</span><span class="sxs-lookup"><span data-stu-id="e97c4-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e97c4-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-193">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e97c4-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-194">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e97c4-194">Current status of the object.</span></span> <span data-ttu-id="e97c4-195">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="e97c4-195">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e97c4-196">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="e97c4-196">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e97c4-197">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="e97c4-197">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e97c4-198">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="e97c4-198">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e97c4-199">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="e97c4-199">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e97c4-200">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e97c4-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e97c4-201">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="e97c4-201">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e97c4-202">("Error")</span><span class="sxs-lookup"><span data-stu-id="e97c4-202">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e97c4-203">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="e97c4-203">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e97c4-204">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="e97c4-204">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e97c4-205">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="e97c4-205">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e97c4-206">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e97c4-206">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e97c4-207">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="e97c4-207">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e97c4-208">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="e97c4-208">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e97c4-209">**VPath**</span><span class="sxs-lookup"><span data-stu-id="e97c4-209">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e97c4-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e97c4-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e97c4-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e97c4-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e97c4-212">Ruta de acceso virtual a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e97c4-212">Virtual Path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e97c4-213">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e97c4-213">Requirements</span></span>



| <span data-ttu-id="e97c4-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="e97c4-214">Requirement</span></span> | <span data-ttu-id="e97c4-215">Value</span><span class="sxs-lookup"><span data-stu-id="e97c4-215">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e97c4-216">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e97c4-216">Minimum supported client</span></span><br/> | <span data-ttu-id="e97c4-217">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e97c4-217">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e97c4-218">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e97c4-218">Minimum supported server</span></span><br/> | <span data-ttu-id="e97c4-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e97c4-219">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="e97c4-220">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e97c4-220">Namespace</span></span><br/>                | <span data-ttu-id="e97c4-221">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e97c4-221">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e97c4-222">MOF</span><span class="sxs-lookup"><span data-stu-id="e97c4-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e97c4-223"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e97c4-223"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="e97c4-224">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e97c4-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e97c4-225"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e97c4-225"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

