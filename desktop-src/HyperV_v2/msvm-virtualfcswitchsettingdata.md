---
description: Representa la configuración de un modificador de Canal de fibra virtual.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Msvm_VirtualFcSwitchSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540315"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a><span data-ttu-id="ae75e-103">MSVM \_ VirtualFcSwitchSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="ae75e-103">Msvm\_VirtualFcSwitchSettingData class</span></span>

<span data-ttu-id="ae75e-104">Representa la configuración de un modificador de Canal de fibra virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-104">Represents the configuration of a virtual Fibre Channel switch.</span></span>

<span data-ttu-id="ae75e-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ae75e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae75e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae75e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
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

## <a name="members"></a><span data-ttu-id="ae75e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae75e-107">Members</span></span>

<span data-ttu-id="ae75e-108">La clase **MSVM \_ VirtualFcSwitchSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ae75e-108">The **Msvm\_VirtualFcSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ae75e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae75e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae75e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae75e-110">Properties</span></span>

<span data-ttu-id="ae75e-111">La clase **MSVM \_ VirtualFcSwitchSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ae75e-111">The **Msvm\_VirtualFcSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae75e-112">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="ae75e-112">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae75e-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-115">Acción que se debe realizar para la máquina virtual cuando se produce un error en el software ejecutado por la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-115">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="ae75e-116">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae75e-116">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-117">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="ae75e-117">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-118">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae75e-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-120">Acción que se realizará para la máquina virtual cuando se apague el host.</span><span class="sxs-lookup"><span data-stu-id="ae75e-120">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="ae75e-121">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae75e-121">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-122">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="ae75e-122">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-123">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae75e-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-125">Acción que se realizará para la máquina virtual cuando se inicie el host.</span><span class="sxs-lookup"><span data-stu-id="ae75e-125">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="ae75e-126">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae75e-126">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-127">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="ae75e-127">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-128">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae75e-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-130">El tiempo de retardo antes de que la máquina virtual se inicie automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ae75e-130">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="ae75e-131">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae75e-131">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-132">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="ae75e-132">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae75e-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-135">Número que indica la secuencia relativa de activación de la máquina virtual cuando se inicia el sistema host.</span><span class="sxs-lookup"><span data-stu-id="ae75e-135">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="ae75e-136">Un número menor indica la activación anterior.</span><span class="sxs-lookup"><span data-stu-id="ae75e-136">A lower number indicates earlier activation.</span></span> <span data-ttu-id="ae75e-137">Si una o más configuraciones muestran el mismo valor, la secuencia depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="ae75e-137">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="ae75e-138">Un valor de 0 indica que la secuencia depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="ae75e-138">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="ae75e-139">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae75e-139">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ae75e-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-143">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ae75e-143">A short description of the object.</span></span> <span data-ttu-id="ae75e-144">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae75e-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-145">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ae75e-145">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-148">La ruta de acceso de un directorio donde se almacena la información sobre la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-148">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="ae75e-149">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-149">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-150">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="ae75e-150">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-153">La ruta de acceso relativa y el nombre de un archivo donde se almacena la información sobre la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-153">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="ae75e-154">Esta ruta de acceso es relativa a la propiedad **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="ae75e-154">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="ae75e-155">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-155">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-156">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="ae75e-156">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-159">Identificador único de la configuración.</span><span class="sxs-lookup"><span data-stu-id="ae75e-159">The unique identifier of the configuration.</span></span> <span data-ttu-id="ae75e-160">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-160">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-161">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="ae75e-161">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-162">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae75e-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-164">Fecha y hora en que se creó la configuración.</span><span class="sxs-lookup"><span data-stu-id="ae75e-164">The date and time at which the settings were created.</span></span> <span data-ttu-id="ae75e-165">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-165">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="ae75e-166">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-166">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-167">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae75e-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-170">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ae75e-170">A description of the object.</span></span> <span data-ttu-id="ae75e-171">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae75e-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ae75e-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-175">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="ae75e-175">A display name for the object.</span></span> <span data-ttu-id="ae75e-176">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-176">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ae75e-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-180">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="ae75e-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-181">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ae75e-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ae75e-182">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-183">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ae75e-183">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-186">La ruta de acceso de un directorio en el que se almacena la información de registro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-186">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="ae75e-187">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae75e-187">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-188">**Notas**</span><span class="sxs-lookup"><span data-stu-id="ae75e-188">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-189">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ae75e-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-191">Notas proporcionadas por el usuario que están relacionadas con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-191">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="ae75e-192">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-192">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-193">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="ae75e-193">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-196">La ruta de acceso completa de un archivo donde se almacena información relacionada con la recuperación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-196">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="ae75e-197">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae75e-197">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-198">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ae75e-198">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-201">La ruta de acceso de un directorio donde se almacena información sobre las instantáneas de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-201">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="ae75e-202">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-203">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ae75e-203">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-206">La ruta de acceso de un directorio donde se almacena información relacionada con la suspensión de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-206">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="ae75e-207">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-208">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ae75e-208">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-211">La ruta de acceso de un directorio donde se almacenan los archivos de intercambio de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae75e-211">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="ae75e-212">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ae75e-212">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-213">**Virtualsystemidentifer**</span><span class="sxs-lookup"><span data-stu-id="ae75e-213">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-216">Nombre del objeto [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) al que pertenecen estos datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="ae75e-216">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="ae75e-217">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae75e-218">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="ae75e-218">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae75e-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae75e-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae75e-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae75e-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae75e-221">Especifica el tipo de máquina virtual que representan los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="ae75e-221">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="ae75e-222">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae75e-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae75e-223">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae75e-223">Requirements</span></span>



| <span data-ttu-id="ae75e-224">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae75e-224">Requirement</span></span> | <span data-ttu-id="ae75e-225">Value</span><span class="sxs-lookup"><span data-stu-id="ae75e-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae75e-226">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae75e-226">Minimum supported client</span></span><br/> | <span data-ttu-id="ae75e-227">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae75e-227">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ae75e-228">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae75e-228">Minimum supported server</span></span><br/> | <span data-ttu-id="ae75e-229">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae75e-229">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae75e-230">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae75e-230">Namespace</span></span><br/>                | <span data-ttu-id="ae75e-231">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ae75e-231">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ae75e-232">MOF</span><span class="sxs-lookup"><span data-stu-id="ae75e-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae75e-233"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae75e-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae75e-234">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae75e-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae75e-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae75e-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

