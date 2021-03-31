---
description: Representa una entrada de autorización para un servidor de recuperación.
ms.assetid: 8c057b39-7102-4fbf-b4be-f18627a88834
title: Msvm_ReplicationAuthorizationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationAuthorizationSettingData
- Msvm_ReplicationAuthorizationSettingData.InstanceID
- Msvm_ReplicationAuthorizationSettingData.Caption
- Msvm_ReplicationAuthorizationSettingData.Description
- Msvm_ReplicationAuthorizationSettingData.ElementName
- Msvm_ReplicationAuthorizationSettingData.AllowedPrimaryHostSystem
- Msvm_ReplicationAuthorizationSettingData.TrustGroup
- Msvm_ReplicationAuthorizationSettingData.ReplicaStorageLocation
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ba069de1bbe005e8a2a06891db8218ab313baa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277047"
---
# <a name="msvm_replicationauthorizationsettingdata-class"></a><span data-ttu-id="807b4-103">MSVM \_ ReplicationAuthorizationSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="807b4-103">Msvm\_ReplicationAuthorizationSettingData class</span></span>

<span data-ttu-id="807b4-104">Representa una entrada de autorización para un servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="807b4-104">Represents an authorization entry for a recovery server.</span></span>

<span data-ttu-id="807b4-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="807b4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="807b4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="807b4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationAuthorizationSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string AllowedPrimaryHostSystem;
  string TrustGroup;
  string ReplicaStorageLocation;
};
```

## <a name="members"></a><span data-ttu-id="807b4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="807b4-107">Members</span></span>

<span data-ttu-id="807b4-108">La clase **MSVM \_ ReplicationAuthorizationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="807b4-108">The **Msvm\_ReplicationAuthorizationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="807b4-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="807b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="807b4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="807b4-110">Properties</span></span>

<span data-ttu-id="807b4-111">La clase **MSVM \_ ReplicationAuthorizationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="807b4-111">The **Msvm\_ReplicationAuthorizationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="807b4-112">**AllowedPrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="807b4-112">**AllowedPrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807b4-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807b4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807b4-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="807b4-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="807b4-115">El nombre de dominio completo o el nombre de grupo de los servidores principales que pueden replicarse en este servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="807b4-115">The fully qualified domain name or group name of the primary servers that are allowed to replicate to this recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="807b4-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="807b4-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807b4-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807b4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807b4-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807b4-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="807b4-119">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="807b4-119">A short description of the object.</span></span> <span data-ttu-id="807b4-120">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="807b4-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="807b4-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="807b4-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807b4-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807b4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807b4-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807b4-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="807b4-124">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="807b4-124">A description of the object.</span></span> <span data-ttu-id="807b4-125">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="807b4-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="807b4-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="807b4-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807b4-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807b4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807b4-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807b4-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="807b4-129">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="807b4-129">A display name for the object.</span></span> <span data-ttu-id="807b4-130">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="807b4-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="807b4-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="807b4-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807b4-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807b4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807b4-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="807b4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="807b4-134">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="807b4-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="807b4-135">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="807b4-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="807b4-136">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="807b4-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="807b4-137">**ReplicaStorageLocation**</span><span class="sxs-lookup"><span data-stu-id="807b4-137">**ReplicaStorageLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807b4-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807b4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807b4-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="807b4-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="807b4-140">La ubicación donde se almacenarán los archivos de replicación de **AllowedPrimaryHostSystem** .</span><span class="sxs-lookup"><span data-stu-id="807b4-140">The location where replication files from the **AllowedPrimaryHostSystem** will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="807b4-141">**TrustGroup**</span><span class="sxs-lookup"><span data-stu-id="807b4-141">**TrustGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="807b4-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="807b4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="807b4-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="807b4-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="807b4-144">Nombre del grupo de confianza para la entrada de autorización.</span><span class="sxs-lookup"><span data-stu-id="807b4-144">The name of the trust group for the authorization entry.</span></span> <span data-ttu-id="807b4-145">Esto identifica las múltiples entradas de autorización que se agrupan.</span><span class="sxs-lookup"><span data-stu-id="807b4-145">This identifies the multiple authorization entries that are grouped together.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="807b4-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="807b4-146">Requirements</span></span>



| <span data-ttu-id="807b4-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="807b4-147">Requirement</span></span> | <span data-ttu-id="807b4-148">Value</span><span class="sxs-lookup"><span data-stu-id="807b4-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="807b4-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="807b4-149">Minimum supported client</span></span><br/> | <span data-ttu-id="807b4-150">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="807b4-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="807b4-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="807b4-151">Minimum supported server</span></span><br/> | <span data-ttu-id="807b4-152">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="807b4-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="807b4-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="807b4-153">Namespace</span></span><br/>                | <span data-ttu-id="807b4-154">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="807b4-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="807b4-155">MOF</span><span class="sxs-lookup"><span data-stu-id="807b4-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="807b4-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="807b4-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="807b4-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="807b4-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="807b4-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="807b4-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="807b4-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="807b4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="807b4-160">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="807b4-160">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="807b4-161">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="807b4-161">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="807b4-162">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="807b4-162">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="807b4-163">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="807b4-163">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> </dl>

 

