---
description: La macro NOTIFICATION-TYPE contiene los siguientes elementos.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: NOTIFICATION-TYPE (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648241"
---
# <a name="notification-type-macro"></a><span data-ttu-id="a0724-103">NOTIFICATION-TYPE (macro)</span><span class="sxs-lookup"><span data-stu-id="a0724-103">NOTIFICATION-TYPE Macro</span></span>

<span data-ttu-id="a0724-104">La macro NOTIFICATION-TYPE contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="a0724-104">The NOTIFICATION-TYPE macro contains the following elements.</span></span>

> [!Note]  
> <span data-ttu-id="a0724-105">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a0724-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="a0724-106">Componentes</span><span class="sxs-lookup"><span data-stu-id="a0724-106">Components</span></span>

<dl> <dt>

<span data-ttu-id="a0724-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descriptor de objeto</span><span class="sxs-lookup"><span data-stu-id="a0724-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="a0724-108">Adjunta un nombre a un evento SNMP en una macro de tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="a0724-108">Attaches a name to an SNMP event in a NOTIFICATION-TYPE macro.</span></span> <span data-ttu-id="a0724-109">En la lista siguiente se enumeran las reglas para asignar el descriptor de objeto.</span><span class="sxs-lookup"><span data-stu-id="a0724-109">The following list lists the rules for mapping the object descriptor.</span></span>



| <span data-ttu-id="a0724-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0724-110">Type</span></span>                        | <span data-ttu-id="a0724-111">Concatenate</span><span class="sxs-lookup"><span data-stu-id="a0724-111">Concatenate</span></span>                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0724-112">Nombre de clase CIM encapsulada</span><span class="sxs-lookup"><span data-stu-id="a0724-112">Encapsulated CIM class name</span></span> | <span data-ttu-id="a0724-113">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="a0724-113">"SNMP\_"</span></span><br/> <span data-ttu-id="a0724-114">Nombre de identidad del módulo MIB</span><span class="sxs-lookup"><span data-stu-id="a0724-114">MIB module identity name</span></span><br/> <span data-ttu-id="a0724-115">carácter de subrayado ( \_ )</span><span class="sxs-lookup"><span data-stu-id="a0724-115">underscore (\_)</span></span><br/> <span data-ttu-id="a0724-116">descriptor de objeto</span><span class="sxs-lookup"><span data-stu-id="a0724-116">object descriptor</span></span><br/> <span data-ttu-id="a0724-117">" \_ Notificación"</span><span class="sxs-lookup"><span data-stu-id="a0724-117">"\_Notification"</span></span><br/> <span data-ttu-id="a0724-118">Ejemplo: la notificación de **vtpServerDisabled** de **Cisco-VTP-MIB** se asigna a la **\_ notificación SNMP Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_**.</span><span class="sxs-lookup"><span data-stu-id="a0724-118">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_Notification**.</span></span><br/>                 |
| <span data-ttu-id="a0724-119">Nombre de clase CIM de referente</span><span class="sxs-lookup"><span data-stu-id="a0724-119">Referent CIM class name</span></span>     | <span data-ttu-id="a0724-120">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="a0724-120">"SNMP\_"</span></span><br/> <span data-ttu-id="a0724-121">Nombre de identidad del módulo MIB</span><span class="sxs-lookup"><span data-stu-id="a0724-121">MIB module identity name</span></span><br/> <span data-ttu-id="a0724-122">carácter de subrayado ( \_ )</span><span class="sxs-lookup"><span data-stu-id="a0724-122">underscore (\_)</span></span><br/> <span data-ttu-id="a0724-123">descriptor de objeto</span><span class="sxs-lookup"><span data-stu-id="a0724-123">object descriptor</span></span><br/> <span data-ttu-id="a0724-124">" \_ ExtendedNotification"</span><span class="sxs-lookup"><span data-stu-id="a0724-124">"\_ExtendedNotification"</span></span><br/> <span data-ttu-id="a0724-125">Ejemplo: la notificación de **vtpServerDisabled** de **Cisco-VTP-MIB** se asigna a **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.</span><span class="sxs-lookup"><span data-stu-id="a0724-125">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_ExtendedNotification**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a0724-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTs (cláusula)</span><span class="sxs-lookup"><span data-stu-id="a0724-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS clause</span></span>
</dt> <dd>

<span data-ttu-id="a0724-127">Enumera el conjunto de objetos asociados al objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="a0724-127">Enumerates the set of objects associated with the notification object.</span></span>

</dd> <dt>

<span data-ttu-id="a0724-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Cláusula REFERENCE</span><span class="sxs-lookup"><span data-stu-id="a0724-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="a0724-129">Hace referencia a otro documento que contiene más información sobre el objeto.</span><span class="sxs-lookup"><span data-stu-id="a0724-129">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="a0724-130">Se asigna a la **referencia** de calificador de clase CIM, que es de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="a0724-130">It maps to the CIM class qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="a0724-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Cláusula Description</span><span class="sxs-lookup"><span data-stu-id="a0724-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="a0724-132">Describe el objeto en cuestión.</span><span class="sxs-lookup"><span data-stu-id="a0724-132">Describes the object in question.</span></span> <span data-ttu-id="a0724-133">Se asigna a la **Descripción** del calificador de clase CIM, que es de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="a0724-133">It maps to the CIM class qualifier **Description**, which is of type string</span></span>

</dd> <dt>

<span data-ttu-id="a0724-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUs (cláusula)</span><span class="sxs-lookup"><span data-stu-id="a0724-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="a0724-135">Indica si se debe admitir el objeto.</span><span class="sxs-lookup"><span data-stu-id="a0724-135">Indicates whether the object must be supported.</span></span> <span data-ttu-id="a0724-136">Cuando el estado es **obsoleto** o en **desuso**, la notificación se descarta de la asignación.</span><span class="sxs-lookup"><span data-stu-id="a0724-136">When the status is either **obsolete** or **deprecated**, the notification is discarded from the mapping.</span></span> <span data-ttu-id="a0724-137">De lo contrario, esta cláusula se asigna al **Estado** del calificador de clase CIM, que es de tipo **cadena**.</span><span class="sxs-lookup"><span data-stu-id="a0724-137">Otherwise, this clause maps to the CIM class qualifier **Status**, which is of type **string**.</span></span>

<span data-ttu-id="a0724-138">Para SNMPv1, el valor preferido de **status** es **obligatorio** u **opcional**, pero el calificador puede contener algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="a0724-138">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="a0724-139">Para SNMPv2C, el valor preferido de **status** es **Current** u **deprecated**, pero el calificador puede contener algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="a0724-139">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0724-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0724-140">Remarks</span></span>

<span data-ttu-id="a0724-141">El proveedor SNMP asigna la macro **de tipo de notificación** a una definición de clase encapsulada o relacionada.</span><span class="sxs-lookup"><span data-stu-id="a0724-141">The SNMP provider maps the **NOTIFICATION-TYPE** macro to either an encapsulated or referent class definition.</span></span>

<span data-ttu-id="a0724-142">Una definición de clase encapsulada no expone la información de instancia asociada al objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="a0724-142">An encapsulated class definition does not expose the instance information associated with the MIB object.</span></span> <span data-ttu-id="a0724-143">En su lugar, la definición de clase codifica la cláusula OBJECTs como una serie de propiedades de la clase de eventos CIM.</span><span class="sxs-lookup"><span data-stu-id="a0724-143">Instead, the class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="a0724-144">Cada propiedad CIM refleja el nombre, el tipo y el valor del objeto MIB correspondiente en la cláusula OBJECTs.</span><span class="sxs-lookup"><span data-stu-id="a0724-144">Each CIM property reflects the name, type, and value of the corresponding MIB object in the OBJECTS clause.</span></span> <span data-ttu-id="a0724-145">Si necesita información de instancia, debe asignar a una clase referente.</span><span class="sxs-lookup"><span data-stu-id="a0724-145">If you require instance information, you must map to a referent class.</span></span> <span data-ttu-id="a0724-146">Una definición de clase encapsulada se asigna a la clase [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a0724-146">An encapsulated class definition maps to the [SnmpNotification](snmpnotification.md) class.</span></span>

<span data-ttu-id="a0724-147">Una clase referente define un objeto MIB y la información de instancia que se usa para obtener el objeto.</span><span class="sxs-lookup"><span data-stu-id="a0724-147">A referent class defines an MIB object and the instance information used to obtain the object.</span></span> <span data-ttu-id="a0724-148">La definición de clase codifica la cláusula OBJECTs como una serie de propiedades de la clase de eventos CIM.</span><span class="sxs-lookup"><span data-stu-id="a0724-148">The class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="a0724-149">Cada propiedad CIM refleja el nombre del objeto MIB correspondiente en la cláusula OBJECTs y el tipo como un objeto incrustado que refleja una instancia de la clase asociada a ese objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="a0724-149">Each CIM property reflects the name of the corresponding MIB object in the OBJECTS clause and the type as an embedded object that reflects an instance of the class associated with that MIB object.</span></span> <span data-ttu-id="a0724-150">A continuación, el proveedor genera una clase asociada con el objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="a0724-150">The provider then generates a class associated with the MIB object.</span></span> <span data-ttu-id="a0724-151">Por **ejemplo, el tipo de canal** se asigna a una clase incrustada denominada **SNMP \_ RFC1213 \_ MIB \_** de canalización.</span><span class="sxs-lookup"><span data-stu-id="a0724-151">For example, **ifIndex** maps to an embedded class named **SNMP\_RFC1213\_MIB\_ifIndex**.</span></span> <span data-ttu-id="a0724-152">Para obtener más información sobre este tipo de clase, vea [macro de tipo de objeto](object-type-macro.md).</span><span class="sxs-lookup"><span data-stu-id="a0724-152">For more information about this type of class, see [OBJECT-TYPE Macro](object-type-macro.md).</span></span>

 

 




