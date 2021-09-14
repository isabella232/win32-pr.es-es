---
description: La macro NOTIFICATION-TYPE contiene los siguientes elementos.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: NOTIFICATION-TYPE (Macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172554"
---
# <a name="notification-type-macro"></a>NOTIFICATION-TYPE (Macro)

La macro NOTIFICATION-TYPE contiene los siguientes elementos.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

## <a name="components"></a>Componentes

<dl> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descriptor de objetos
</dt> <dd>

Asocia un nombre a un evento SNMP en una macro NOTIFICATION-TYPE. En la lista siguiente se enumeran las reglas para asignar el descriptor de objetos.



| Tipo                        | Concatenate                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de clase CIM encapsulada | \_"SNMP"<br/> Nombre de identidad del módulo MIB<br/> subrayado ( \_ )<br/> descriptor de objeto<br/> \_"Notificación"<br/> Ejemplo: la **notificación vtpServerDisabled** de **CISCO-VTP-MIB** se asigna a la notificación **\_ \_ \_ \_ vtpServerDisabled \_ de SNMP CISCO VTP MIB**.<br/>                 |
| Nombre de clase CIM de referencia     | \_"SNMP"<br/> Nombre de identidad del módulo MIB<br/> subrayado ( \_ )<br/> descriptor de objeto<br/> \_"ExtendedNotification"<br/> Ejemplo: la **notificación vtpServerDisabled** de **CISCO-VTP-MIB** se asigna a **SNMP CISCO \_ \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.<br/> |



 

</dd> <dt>

<span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Cláusula OBJECTS
</dt> <dd>

Enumera el conjunto de objetos asociados al objeto de notificación.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>CLÁUSULA REFERENCE
</dt> <dd>

Hace referencia a otro documento que contiene más información sobre el objeto . Se asigna al calificador de clase CIM **Reference**, que es de tipo cadena.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION (cláusula)
</dt> <dd>

Describe el objeto en cuestión. Se asigna al calificador de clase CIM **Description**, que es de tipo cadena.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Status (cláusula)
</dt> <dd>

Indica si el objeto debe ser compatible. Cuando el estado está obsoleto **o** en **desuso,** la notificación se descarta de la asignación. De lo contrario, esta cláusula se asigna al calificador de clase CIM **Status**, que es de tipo **cadena**.

Para SNMPv1, el valor preferido  de **Status** es obligatorio u **opcional,** pero el calificador puede contener algún otro valor. Para SNMPv2C, el valor preferido de **Status** es **actual** o está en desuso, pero el calificador puede contener algún otro valor. 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El proveedor SNMP asigna la macro **NOTIFICATION-TYPE** a una definición de clase encapsulada o de referencia.

Una definición de clase encapsulada no expone la información de instancia asociada al objeto MIB. En su lugar, la definición de clase codifica la cláusula OBJECTS como una serie de propiedades de la clase de eventos CIM. Cada propiedad CIM refleja el nombre, el tipo y el valor del objeto MIB correspondiente en la cláusula OBJECTS. Si necesita información de instancia, debe asignar a una clase de referencia. Una definición de clase encapsulada se asigna a [la clase SnmpNotification.](snmpnotification.md)

Una clase de referencia define un objeto MIB y la información de instancia utilizada para obtener el objeto. La definición de clase codifica la cláusula OBJECTS como una serie de propiedades de la clase de eventos CIM. Cada propiedad CIM refleja el nombre del objeto MIB correspondiente en la cláusula OBJECTS y el tipo como un objeto incrustado que refleja una instancia de la clase asociada a ese objeto MIB. A continuación, el proveedor genera una clase asociada al objeto MIB. Por ejemplo, **ifIndex se** asigna a una clase incrustada denominada **SNMP \_ RFC1213 \_ MIB \_ ifIndex**. Para obtener más información sobre este tipo de clase, vea [OBJECT-TYPE Macro](object-type-macro.md).

 

 




