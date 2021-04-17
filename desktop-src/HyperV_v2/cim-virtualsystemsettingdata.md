---
description: Describe los aspectos virtuales de un sistema virtual a través de un conjunto de propiedades específicas de virtualización. CIM \_ VirtualSystemSettingData también se utiliza como clase de nivel superior de configuraciones del sistema virtual.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: CIM_VirtualSystemSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668091"
---
# <a name="cim_virtualsystemsettingdata-class"></a><span data-ttu-id="2f9e7-104">\_Clase VirtualSystemSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="2f9e7-104">CIM\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="2f9e7-105">Describe los aspectos virtuales de un sistema virtual a través de un conjunto de propiedades específicas de virtualización.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-105">Describes the virtual aspects of a virtual system through a set of virtualization specific properties.</span></span> <span data-ttu-id="2f9e7-106">**CIM \_ VirtualSystemSettingData** también se utiliza como clase de nivel superior de configuraciones del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-106">**CIM\_VirtualSystemSettingData** is also used as the top level class of virtual system configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9e7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f9e7-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a><span data-ttu-id="2f9e7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2f9e7-108">Members</span></span>

<span data-ttu-id="2f9e7-109">La clase **CIM \_ VirtualSystemSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2f9e7-109">The **CIM\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2f9e7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f9e7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f9e7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f9e7-111">Properties</span></span>

<span data-ttu-id="2f9e7-112">La clase **CIM \_ VirtualSystemSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-112">The **CIM\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f9e7-113">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-113">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-116">La acción que se debe realizar para el sistema virtual cuando se produce un error en el software ejecutado por el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-116">The action to take for the virtual system when the software executed by the virtual system fails.</span></span> <span data-ttu-id="2f9e7-117">Los errores resueltos por esta propiedad solo incluyen aquellos que son detectables por la plataforma del host, como una condición de estado de espera no interrumpida.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-117">The failures addressed by this property only include those that are detectable by the host platform, such as a non-interruptible wait state condition.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="2f9e7-118">**Ninguno** (2)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-118">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="2f9e7-119">**Reiniciar** (3)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-119">**Restart** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

<span data-ttu-id="2f9e7-120">**Revertir a instantánea** (4)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-120">**Revert to snapshot** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2f9e7-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f9e7-122">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-122">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-123">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-125">La acción que se realizará para el sistema virtual cuando se apague el host.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-125">The action to take for the virtual system when the host is shut down.</span></span>

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

<span data-ttu-id="2f9e7-126">**Desactivar** (2)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-126">**Turn Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

<span data-ttu-id="2f9e7-127">**Guardar estado** (3)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-127">**Save state** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

<span data-ttu-id="2f9e7-128">**Shutdown** (4)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-128">**Shutdown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2f9e7-129">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-129">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f9e7-130">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-130">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-133">Acción que se realizará en el sistema virtual cuando se inicie el host.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-133">The action to take on the virtual system when the host is started.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="2f9e7-134">**Ninguno** (2)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-134">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

<span data-ttu-id="2f9e7-135">**Reiniciar si previamente estaba activo** (3)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-135">**Restart if previously active** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

<span data-ttu-id="2f9e7-136">**Siempre startup** (4)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-136">**Always startup** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2f9e7-137">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2f9e7-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f9e7-138">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-138">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-139">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-141">Retraso de la acción de inicio.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-141">The delay for the startup action.</span></span> <span data-ttu-id="2f9e7-142">Este valor es una variante de intervalo del tipo de datos **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="2f9e7-142">This value is an interval variant of the **datetime** data type.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-143">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-143">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-146">El número de secuencia para la activación del sistema virtual cuando se inicia el sistema host.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-146">The sequence number for virtual system activation when the host system is started.</span></span> <span data-ttu-id="2f9e7-147">Un número menor indica la activación anterior.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-147">A lower number indicates earlier activation.</span></span> <span data-ttu-id="2f9e7-148">Si una o más configuraciones muestran el mismo valor, la secuencia depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-148">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="2f9e7-149">Un valor de "0" indica que la secuencia depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-149">A value of "0" indicates that the sequence is implementation dependent.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-150">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-150">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-153">La ruta de acceso del directorio donde se almacena la información sobre la configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-153">The file path of the directory where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="2f9e7-154">El formato de esta propiedad es un URI basado en RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-154">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-155">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-155">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-158">La ruta de acceso relativa del archivo donde se almacena la información sobre la configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-158">The relative path of the file where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="2f9e7-159">La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="2f9e7-159">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="2f9e7-160">El formato de esta propiedad es un URI basado en RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-160">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-161">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-161">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-164">Identificador único de la configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-164">The unique id of the virtual system configuration.</span></span>

> [!Note]  
> <span data-ttu-id="2f9e7-165">**ConfigurationID** es diferente del **InstanceID** y se asigna mediante la implementación a un sistema virtual o una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-165">**ConfigurationID** is different from the **InstanceID**, and is assigned by the implementation to a virtual system or a virtual system configuration.</span></span> <span data-ttu-id="2f9e7-166">**ConfigurationID** no es una clave y se puede producir el mismo valor para más de una instancia.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-166">**ConfigurationID** is not a key, and the same value may occur for more than one instance.</span></span>

 

</dd> <dt>

<span data-ttu-id="2f9e7-167">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-167">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-168">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-170">Fecha y hora en que se creó la configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-170">The date and time when the virtual system configuration was created.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-171">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-171">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-174">La ruta de acceso relativa del directorio donde se almacena la información de registro del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-174">The relative file path of the directory where log information for the virtual system is stored.</span></span> <span data-ttu-id="2f9e7-175">La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="2f9e7-175">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="2f9e7-176">El formato de esta propiedad es un URI basado en RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-176">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-177">**Notas**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-177">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-178">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-178">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-180">Una matriz que contiene las notas proporcionadas por el usuario que están relacionadas con el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-180">An array that contains user supplied notes that are related to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-181">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-181">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-184">La ruta de acceso del archivo donde se almacena la información relacionada con la recuperación del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-184">The path of the file where recovery related information of the virtual system is stored.</span></span> <span data-ttu-id="2f9e7-185">El formato de esta propiedad es un URI basado en RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-185">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-186">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-186">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-189">La ruta de acceso relativa del directorio donde se almacena la información sobre las instantáneas del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-189">The relative path of the directory where information about virtual system snapshots is stored.</span></span> <span data-ttu-id="2f9e7-190">La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="2f9e7-190">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="2f9e7-191">El formato de esta propiedad es un URI basado en RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-191">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-192">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-192">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-195">La ruta de acceso relativa del directorio donde se almacena la información relacionada con la suspensión del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-195">The relative path of the directory where suspend related information about the virtual system is stored.</span></span> <span data-ttu-id="2f9e7-196">La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="2f9e7-196">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="2f9e7-197">El formato de esta propiedad es un URI basado en RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-197">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-198">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-198">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-201">Ruta de acceso relativa al archivo del directorio donde se almacenan los archivos de intercambio del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-201">The relative file path of the directory where swap files of the virtual system are stored.</span></span> <span data-ttu-id="2f9e7-202">La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="2f9e7-202">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="2f9e7-203">El formato de esta propiedad es un URI basado en RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-203">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-204">**Virtualsystemidentifer**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-204">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-207">Nombre único del sistema dentro de la plataforma de virtualización.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-207">The unique name for the system within the virtualization platform.</span></span> <span data-ttu-id="2f9e7-208">**Virtualsystemidentifer** no es el nombre de host asignado a la instancia del sistema operativo que se ejecuta dentro del sistema virtual, ni tampoco es una dirección IP o dirección MAC asignada a ninguno de sus puertos de red.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-208">**VirtualSystemIdentifier** is not the hostname assigned to the operating system instance running within the virtual system, nor is it an IP address or MAC address assigned to any of its network ports.</span></span>

<span data-ttu-id="2f9e7-209">**Virtualsystemidentifer** puede contener reglas específicas de implementación, como patrones simples o una expresión regular que la implementación pueda interpretar al establecer **virtualsystemidentifer**.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-209">The **VirtualSystemIdentifier** may contain implementation specific rules, like simple patterns or a regular expression that may be interpreted by the implementation when setting **VirtualSystemIdentifier**.</span></span>

</dd> <dt>

<span data-ttu-id="2f9e7-210">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-210">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9e7-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9e7-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f9e7-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9e7-213">Tipo del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-213">The type of the virtual system.</span></span>

> [!Note]  
> <span data-ttu-id="2f9e7-214">Si no se conoce el tipo de sistema virtual, este valor debe establecerse en "DMTF: Unknown".</span><span class="sxs-lookup"><span data-stu-id="2f9e7-214">If the virtual system type is unknown, this value must be set to "DMTF:unknown".</span></span>

 

<span data-ttu-id="2f9e7-215">A esta propiedad se le da formato con el siguiente formato de Backus Naur form (ABNF) ampliado:</span><span class="sxs-lookup"><span data-stu-id="2f9e7-215">This property is formatted using the following Augmented Backus Naur Form (ABNF) format:</span></span>

<span data-ttu-id="2f9e7-216">vs-Type = DMTF-Value/Other-org-Value/Legacy-Value; DMTF-Value = "DMTF:" Defining-org ":" org-vs-Type; otro: org-Value = Defining-org ":" org-vs-Type;</span><span class="sxs-lookup"><span data-stu-id="2f9e7-216">vs-type = dmtf-value / other-org-value / legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;</span></span>

<span data-ttu-id="2f9e7-217">El valor del formato ABNF anterior es:</span><span class="sxs-lookup"><span data-stu-id="2f9e7-217">The value of the above ABNF format are:</span></span>

-   <span data-ttu-id="2f9e7-218">*DMTF:*   valor de propiedad definido por DMTF y que se define en la descripción de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-218">*dmtf-value*   a property value defined by DMTF and is defined in the description of this property.</span></span>
-   <span data-ttu-id="2f9e7-219">*other-org-Value*   es un valor de propiedad definido por una entidad comercial distinta de DMTF y no se define en la descripción de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-219">*other-org-value*   is a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span>
-   <span data-ttu-id="2f9e7-220">valor *heredado:* valor de propiedad definido por una entidad comercial distinta de DMTF y no se define en la descripción de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-220">*legacy-value*   a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span> <span data-ttu-id="2f9e7-221">Estos valores están permitidos pero se recomienda que estén en desuso a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-221">These values are permitted but recommended to be deprecated over time.</span></span>
-   <span data-ttu-id="2f9e7-222">*definir: org*   un identificador para la entidad comercial que define el tipo de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-222">*defining-org*   an identifier for the business entity that defines the virtual system type.</span></span> <span data-ttu-id="2f9e7-223">Debe incluir un nombre con copyright, marca registrada o un nombre único que sea propiedad de la entidad empresarial.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-223">It should include a copyrighted, trademarked, or a unique name that is owned by the business entity.</span></span> <span data-ttu-id="2f9e7-224">No debe ser "DMTF" y no debe contener un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-224">It should not be "DMTF" and shall not contain a colon.</span></span>
-   <span data-ttu-id="2f9e7-225">*org-vs-escriba*   un identificador para el tipo de sistema virtual dentro de la entidad empresarial que lo define.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-225">*org-vs-type*   an identifier for the virtual system type within the defining business entity.</span></span> <span data-ttu-id="2f9e7-226">Debe ser único dentro de la definición de-org. org-vs-Type puede usar cualquier carácter permitido para las cadenas CIM, excepto los siguientes: U0000-U001F (controles C0 Unicode), U0020 (espacio), U007F (controles C0 Unicode) o U0080-U009F (controles C1 de Unicode).</span><span class="sxs-lookup"><span data-stu-id="2f9e7-226">It should be unique within defining-org. org-vs-type may use any character allowed for CIM strings, except the following: U0000-U001F (Unicode C0 controls), U0020 (space), U007F (Unicode C0 controls), or U0080-U009F (Unicode C1 controls).</span></span>
-   <span data-ttu-id="2f9e7-227">Si es necesario estructurar el valor en segmentos, los segmentos deben separarse con un solo signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-227">If there is a need to structure the value into segments, the segments should be separated with a single colon.</span></span>
-   <span data-ttu-id="2f9e7-228">Los valores de esta propiedad deben procesarse de forma confidencial.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-228">The values of this property should be processed case sensitively.</span></span> <span data-ttu-id="2f9e7-229">Están diseñados para procesarse mediante programación, en lugar de ser un nombre para mostrar y deben ser cortos.</span><span class="sxs-lookup"><span data-stu-id="2f9e7-229">They are intended to be processed programmatically, instead of being a display name, and should be short.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f9e7-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f9e7-230">Requirements</span></span>



| <span data-ttu-id="2f9e7-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f9e7-231">Requirement</span></span> | <span data-ttu-id="2f9e7-232">Value</span><span class="sxs-lookup"><span data-stu-id="2f9e7-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9e7-233">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f9e7-233">Minimum supported client</span></span><br/> | <span data-ttu-id="2f9e7-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f9e7-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2f9e7-235">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f9e7-235">Minimum supported server</span></span><br/> | <span data-ttu-id="2f9e7-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f9e7-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2f9e7-237">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2f9e7-237">Namespace</span></span><br/>                | <span data-ttu-id="2f9e7-238">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2f9e7-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2f9e7-239">MOF</span><span class="sxs-lookup"><span data-stu-id="2f9e7-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f9e7-240"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e7-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f9e7-241">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f9e7-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f9e7-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e7-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f9e7-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f9e7-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f9e7-244">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2f9e7-244">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




