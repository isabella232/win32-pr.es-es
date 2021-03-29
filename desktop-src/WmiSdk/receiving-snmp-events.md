---
description: Los proveedores de eventos SNMP admiten las capturas de SNMPv1 y las notificaciones de SNMPv2.
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: Recibir eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f718d2bcea85d0ee942050108f337f8ecb78e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648497"
---
# <a name="receiving-snmp-events"></a>Recibir eventos SNMP

Los proveedores de eventos SNMP admiten las capturas de SNMPv1 y las notificaciones de SNMPv2.

Se admiten los tres tipos siguientes de capturas de SNMPv1 y notificaciones de SNMPv2:

-   Genérico

    Las capturas y notificaciones genéricas se corresponden con eventos con nombre como el inicio en frío y el vínculo. Las capturas y notificaciones genéricas se representan mediante clases, como **SnmpLinkUpNotification** y **SnmpWarmStartExtendedNotification**, que contienen el nombre de la captura en el nombre de clase. Estas clases son subclases de [SnmpNotification](snmpnotification.md) y [SnmpExtendedNotification](snmpextendednotification.md).

-   Específico de la empresa

    Las capturas y notificaciones específicas de la empresa corresponden a eventos representados por una clase WMI que no es una subclase de [SnmpNotification](snmpnotification.md) y [SnmpExtendedNotification](snmpextendednotification.md). Para admitir las notificaciones y capturas específicas de la empresa, un consumidor debe definir las clases mediante la compilación de definiciones MIB mediante el compilador SNMP MIB.

-   No específicas de la empresa

    Las capturas y notificaciones no específicas de la empresa no corresponden a ninguno de los tipos de eventos genéricos ni a los tipos de eventos específicos de la empresa. Las capturas y notificaciones no específicas de la empresa no han compilado sus definiciones MIB en el SMIR. Se representan mediante las clases [SnmpNotification](snmpnotification.md), **SnmpV2Notification**, **SnmpV1ExtendedNotification** y **SnmpV2ExtendedNotification** derivadas de SnmpNotification y [SnmpExtendedNotification](snmpextendednotification.md).

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

En este tema se describen las siguientes secciones:

-   [Recepción de eventos SNMP genéricos](#receiving-generic-snmp-events)
-   [Recibir eventos de Enterprise-Specific](#receiving-enterprise-specific-events)
-   [Recibir eventos de Enterprise-Nonspecific](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>Recepción de eventos SNMP genéricos

SEEP y SREP admiten todos los tipos de capturas de SNMPv1 genéricas y notificaciones de SNMPv2. Los eventos SNMP genéricos se representan mediante subclases de las clases [SnmpNotification](snmpnotification.md) y [SnmpExtendedNotification](snmpextendednotification.md) .

Cada tipo de evento se representa mediante una clase SEEP y una clase SREP. Las clases SEEP derivan de [SnmpNotification](snmpnotification.md); las clases SREP derivan de [SnmpExtendedNotification](snmpextendednotification.md). Los proveedores de eventos requieren clases diferentes porque usan mecanismos diferentes en la presentación de los datos de eventos SNMP.

SEEP convierte los datos de eventos SNMP directamente en propiedades de clase WMI, mientras que SREP no lo hace. SREP agrega un nivel de direccionamiento indirecto a la interpretación necesaria para utilizar las propiedades WMI. Las propiedades de las subclases de SREP [SnmpExtendedNotification](snmpextendednotification.md) son instancias de clases SNMP; las propiedades de las subclases de SEEP [SnmpNotification](snmpnotification.md) son enteros y cadenas.

En la tabla siguiente se enumeran los tipos de eventos SNMP genéricos y las clases de eventos asociadas.



| Evento de SNMP                                    | Clase SEEP                                | Clase SREP                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| Error de autenticación                        | **SnmpAuthenticationFailureNotification** | **SnmpAuthenticationFailureExtendedNotification** |
| Pérdida de vecino del Protocolo de puerta de enlace exterior (EGP) | **SnmpEGPNeighborLossNotification**       | **SnmpEGPNeighborLossExtendedNotification**       |
| Inicio en frío                                    | **SnmpColdStartNotification**             | **SnmpColdStartExtendedNotification**             |
| Inicio en caliente                                    | **SnmpWarmStartNotification**             | **SnmpWarmStartExtendedNotification**             |
| Vincular                                       | **SnmpLinkUpNotification**                | **SnmpLinkUpExtendedNotification**                |
| Vincular hacia abajo                                     | **SnmpLinkDownNotification**              | **SnmpLinkDownExtendedNotification**              |



 

Por ejemplo, las clases **SnmpLinkUpNotification** y **SnmpLinkUpExtendedNotification** describen el evento de vínculo. Ambas clases **incluyen las propiedades de tipo de propiedad**, **ifAdminStatus** y **ifOperStatus** , pero tienen tipos muy diferentes. Las propiedades de la clase **SnmpLinkUpNotification** son de tipo SINT32 y String. Las propiedades de la clase **SnmpLinkUpExtendedNotification** son el tipo de objeto incrustado IETF \_ SNMP \_ RFC1213 \_ MIB \_ ifTable.

## <a name="receiving-enterprise-specific-events"></a>Recibir eventos de Enterprise-Specific

SEEP y SREP admiten las capturas y notificaciones específicas de la empresa que haya compilado en el SMIR.

En el procedimiento siguiente se describe cómo recibir eventos específicos de la empresa.

**Para recibir eventos específicos de la empresa**

1.  Compile las definiciones de MIB desde el dispositivo responsable de generar el evento.

    Puede compilar las definiciones de MIB mediante el compilador SNMP MIB. Para obtener más información, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

2.  Determine los tipos de clases que desea asignar a los eventos.

    Al compilar la definición de la MIB para un evento específico de la empresa, puede determinar qué tipo de clase genera el compilador. En concreto, puede indicar al compilador que cree una de las siguientes opciones:

    -   [SnmpNotification](snmpnotification.md) subclases de las definiciones.
    -   [SnmpExtendedNotification](snmpextendednotification.md) subclases de las definiciones.
    -   Las subclases [SnmpNotification](snmpnotification.md) y [SnmpExtendedNotification](snmpextendednotification.md) de las definiciones.

    Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

Si los proveedores de eventos SNMP reciben una notificación o captura específica para la que no hay ninguna clase, los proveedores generan un evento no específico de la empresa. Para obtener más información, consulte [recibir eventos no específicos](#receiving-enterprise-nonspecific-events)de la empresa.

## <a name="receiving-enterprise-nonspecific-events"></a>Recibir eventos de Enterprise-Nonspecific

Un evento no específico de la empresa es un evento que no se asigna desde una captura de SNMPv1 o una notificación de SNMPv2 a cualquiera de las subclases de [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) o a cualquier clase que represente un evento de empresa.

SEEP usa las clases **SNMPV1Notification** o **SNMPV2Notification** para eventos no específicos, mientras que SREP utiliza las clases **SNMPv1ExtendedNotification** y **SNMPV2ExtendedNotification** .

Las cuatro clases no específicas de la empresa derivan de las clases [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) y tienen el mismo formato. Ambas clases tienen la propiedad única **VarBindList**. **VarBindList** es una matriz de instancias de la clase **SnmpVarBind** . **SnmpVarBind** es una clase base admitida por los proveedores de eventos SNMP para representar una instancia de un enlace de variable SNMP. En la tabla siguiente se enumeran las propiedades de **SnmpVarBind**.



| Propiedad         | Descripción                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| Encoding         | Cadena que indica el tipo de notación de sintaxis abstracta uno (ASN. 1) de la variable en la propiedad **Value** . |
| ObjectIdentifier | Cadena que identifica la variable en la propiedad **Value** .                                                 |
| Value            | Datos sin procesar en octetos.                                                                                            |



 

En las clases **SnmpV1Notification** y **SnmpV2Notification** , se ha conservado el orden de enlace de variables del evento SNMP, excepto los dos primeros enlaces de variables, TIMESTAMP y SnmpTrapOID. Estos enlaces se han quitado y se almacenan en las propiedades de **marca** de tiempo e **identificación** de la clase primaria [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) .

 

 



