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
# <a name="notification-type-macro"></a>NOTIFICATION-TYPE (macro)

La macro NOTIFICATION-TYPE contiene los siguientes elementos.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Componentes

<dl> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descriptor de objeto
</dt> <dd>

Adjunta un nombre a un evento SNMP en una macro de tipo de notificación. En la lista siguiente se enumeran las reglas para asignar el descriptor de objeto.



| Tipo                        | Concatenate                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de clase CIM encapsulada | "SNMP \_ "<br/> Nombre de identidad del módulo MIB<br/> carácter de subrayado ( \_ )<br/> descriptor de objeto<br/> " \_ Notificación"<br/> Ejemplo: la notificación de **vtpServerDisabled** de **Cisco-VTP-MIB** se asigna a la **\_ notificación SNMP Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_**.<br/>                 |
| Nombre de clase CIM de referente     | "SNMP \_ "<br/> Nombre de identidad del módulo MIB<br/> carácter de subrayado ( \_ )<br/> descriptor de objeto<br/> " \_ ExtendedNotification"<br/> Ejemplo: la notificación de **vtpServerDisabled** de **Cisco-VTP-MIB** se asigna a **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.<br/> |



 

</dd> <dt>

<span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTs (cláusula)
</dt> <dd>

Enumera el conjunto de objetos asociados al objeto de notificación.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Cláusula REFERENCE
</dt> <dd>

Hace referencia a otro documento que contiene más información sobre el objeto. Se asigna a la **referencia** de calificador de clase CIM, que es de tipo cadena.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Cláusula Description
</dt> <dd>

Describe el objeto en cuestión. Se asigna a la **Descripción** del calificador de clase CIM, que es de tipo cadena.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUs (cláusula)
</dt> <dd>

Indica si se debe admitir el objeto. Cuando el estado es **obsoleto** o en **desuso**, la notificación se descarta de la asignación. De lo contrario, esta cláusula se asigna al **Estado** del calificador de clase CIM, que es de tipo **cadena**.

Para SNMPv1, el valor preferido de **status** es **obligatorio** u **opcional**, pero el calificador puede contener algún otro valor. Para SNMPv2C, el valor preferido de **status** es **Current** u **deprecated**, pero el calificador puede contener algún otro valor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El proveedor SNMP asigna la macro **de tipo de notificación** a una definición de clase encapsulada o relacionada.

Una definición de clase encapsulada no expone la información de instancia asociada al objeto MIB. En su lugar, la definición de clase codifica la cláusula OBJECTs como una serie de propiedades de la clase de eventos CIM. Cada propiedad CIM refleja el nombre, el tipo y el valor del objeto MIB correspondiente en la cláusula OBJECTs. Si necesita información de instancia, debe asignar a una clase referente. Una definición de clase encapsulada se asigna a la clase [SnmpNotification](snmpnotification.md) .

Una clase referente define un objeto MIB y la información de instancia que se usa para obtener el objeto. La definición de clase codifica la cláusula OBJECTs como una serie de propiedades de la clase de eventos CIM. Cada propiedad CIM refleja el nombre del objeto MIB correspondiente en la cláusula OBJECTs y el tipo como un objeto incrustado que refleja una instancia de la clase asociada a ese objeto MIB. A continuación, el proveedor genera una clase asociada con el objeto MIB. Por **ejemplo, el tipo de canal** se asigna a una clase incrustada denominada **SNMP \_ RFC1213 \_ MIB \_** de canalización. Para obtener más información sobre este tipo de clase, vea [macro de tipo de objeto](object-type-macro.md).

 

 




