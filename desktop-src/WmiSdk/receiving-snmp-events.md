---
description: Los proveedores de eventos SNMP admiten capturas SNMPv1 y notificaciones SNMPv2.
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: Recepción de eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf09e32ec05d42adcc60891cd369cde1f3f078541416ce1a492484de024744bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996025"
---
# <a name="receiving-snmp-events"></a>Recepción de eventos SNMP

Los proveedores de eventos SNMP admiten capturas SNMPv1 y notificaciones SNMPv2.

Se admiten los tres tipos siguientes de capturas de SNMPv1 y notificaciones SNMPv2:

-   Genérico

    Las capturas y notificaciones genéricas corresponden a eventos con nombre, como el vínculo hacia arriba y el arranque en frío. Las capturas y notificaciones genéricas se representan mediante clases, como **SnmpLinkUpNotification** y **SnmpWarmStartExtendedNotification,** que contienen el nombre de la captura en el nombre de clase. Estas clases son subclases de [SnmpNotification](snmpnotification.md) y [SnmpExtendedNotification.](snmpextendednotification.md)

-   Enterprise específicos

    Enterprise notificaciones y capturas específicas corresponden a eventos representados por una clase WMI que no es una subclase de [SnmpNotification](snmpnotification.md) y [SnmpExtendedNotification](snmpextendednotification.md). Para admitir notificaciones y capturas específicas de la empresa, un consumidor debe definir clases mediante la compilación de definiciones de MIB mediante el compilador MIB snmp.

-   Enterprise no específico

    Las capturas y notificaciones no específicas de la empresa no se corresponden con ninguno de los tipos de eventos genéricos o los tipos de eventos específicos de la empresa. Las capturas y notificaciones no específicas de los clientes no tienen sus definiciones de MIB compiladas en el SMIR. Se representan mediante las clases [SnmpNotification](snmpnotification.md), **SnmpV2Notification**, **SnmpV1ExtendedNotification** y **SnmpV2ExtendedNotification** derivadas de SnmpNotification y [SnmpExtendedNotification.](snmpextendednotification.md)

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configurar el entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

En este tema se de abordan las siguientes secciones:

-   [Recepción de eventos SNMP genéricos](#receiving-generic-snmp-events)
-   [Recepción de Enterprise-Specific eventos](#receiving-enterprise-specific-events)
-   [Recepción de Enterprise-Nonspecific eventos](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>Recepción de eventos SNMP genéricos

SeeP y SREP admiten todos los tipos de capturas SNMPv1 genéricas y notificaciones SNMPv2. Los eventos SNMP genéricos se representan mediante subclases de las clases [SnmpNotification](snmpnotification.md) y [SnmpExtendedNotification.](snmpextendednotification.md)

Cada tipo de evento se representa mediante una clase SEEP y una clase SREP. Las clases SEEP derivan de [SnmpNotification](snmpnotification.md); las clases SREP derivan de [SnmpExtendedNotification.](snmpextendednotification.md) Los proveedores de eventos requieren clases diferentes porque usan mecanismos diferentes en la presentación de los datos de eventos SNMP.

El SEEP convierte los datos de eventos SNMP directamente en propiedades de clase WMI, mientras que el SREP no. El SREP agrega un nivel de direccionamiento indirecto a la interpretación necesaria para usar las propiedades wmi. Las propiedades de las subclases [SREP SnmpExtendedNotification](snmpextendednotification.md) son instancias de clases SNMP; Las propiedades de las subclases [SNMPNotification](snmpnotification.md) de SEEP son enteros y cadenas.

En la tabla siguiente se enumeran los tipos de eventos SNMP genéricos y las clases de eventos asociadas.



| Evento de SNMP                                    | SEEP (clase)                                | SREP (clase)                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| Error de autenticación                        | **SnmpAuthenticationFailureNotification** | **SnmpAuthenticationFailureExtendedNotification** |
| Pérdida de vecino del Protocolo de puerta de enlace exterior (EGP) | **SnmpEGPNeighborLossNotification**       | **SnmpEGPNeighborLossExtendedNotification**       |
| Arranque en frío                                    | **SnmpColdStartNotification**             | **SnmpColdStartExtendedNotification**             |
| Inicio en caliente                                    | **SnmpWarmStartNotification**             | **SnmpWarmStartExtendedNotification**             |
| Vinculación                                       | **SnmpLinkUpNotification**                | **SnmpLinkUpExtendedNotification**                |
| Vincular hacia abajo                                     | **SnmpLinkDownNotification**              | **SnmpLinkDownExtendedNotification**              |



 

Por ejemplo, las **clases SnmpLinkUpNotification** y **SnmpLinkUpExtendedNotification** describen el evento de vinculación. Ambas clases incluyen las **propiedades ifIndex**, **ifAdminStatus** y **ifOperStatus,** pero tienen tipos muy diferentes. Las propiedades de la **clase SnmpLinkUpNotification** son de tipo SINT32 y STRING. Las propiedades de la **clase SnmpLinkUpExtendedNotification** son el tipo de objeto incrustado IETF \_ SNMP \_ RFC1213 \_ MIB \_ ifTable.

## <a name="receiving-enterprise-specific-events"></a>Recepción de Enterprise-Specific eventos

SeeP y SREP admiten las capturas y notificaciones específicas de la empresa que haya compilado en SMIRA.

En el procedimiento siguiente se describe cómo recibir eventos específicos de la empresa.

**Para recibir eventos específicos de la empresa**

1.  Compile las definiciones de MIB desde el dispositivo responsable de generar el evento.

    Puede compilar las definiciones de MIB mediante el compilador DE MIB SNMP. Para obtener más información, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

2.  Determine qué tipos de clases desea asignar a los eventos.

    Al compilar la definición de MIB para un evento específico de la empresa, puede determinar qué tipo de clase genera el compilador. En concreto, puede indicar al compilador que cree una de las siguientes opciones:

    -   [Subclases SnmpNotification](snmpnotification.md) de las definiciones.
    -   [Subclases SnmpExtendedNotification](snmpextendednotification.md) de las definiciones.
    -   [Subclases SnmpNotification](snmpnotification.md) [y SnmpExtendedNotification](snmpextendednotification.md) de las definiciones.

    Para obtener más información, [vea Compilar archivos MOF](compiling-mof-files.md).

Si los proveedores de eventos SNMP reciben una captura o notificación específica para la que no hay ninguna clase, los proveedores generan un evento no específico de la entidad de seguridad. Para obtener más información, [vea Receiving Enterprise Nonspecific Events](#receiving-enterprise-nonspecific-events).

## <a name="receiving-enterprise-nonspecific-events"></a>Recepción de Enterprise-Nonspecific eventos

Un evento no específico de la empresa es un evento que no se asigna desde una captura de SNMPv1 o una notificación SNMPv2 a ninguna de las subclases [de SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) ni a ninguna clase que represente un evento empresarial.

SEEP usa las **clases SNMPV1Notification** o **SNMPV2Notification** para eventos no específicos, mientras que SREP usa las clases **SNMPv1ExtendedNotification** y **SNMPV2ExtendedNotification.**

Las cuatro clases empresariales no concretas derivan de las clases [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) y tienen el mismo formato. Ambas clases tienen la propiedad **única VarBindList**. **VarBindList es** una matriz de instancias de la **clase SnmpVarBind.** **SnmpVarBind es** una clase base compatible con los proveedores de eventos SNMP para representar una instancia de un enlace de variable SNMP. En la tabla siguiente se enumeran las propiedades **de SnmpVarBind.**



| Propiedad         | Descripción                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| Encoding         | Cadena que indica el tipo de notación de sintaxis abstracta One (ASN.1) de la variable en la **propiedad Value.** |
| ObjectIdentifier | Cadena que identifica la variable en la **propiedad Value.**                                                 |
| Value            | Datos sin procesar en octetos.                                                                                            |



 

En las **clases SnmpV1Notification** y **SnmpV2Notification,** el orden de enlace de variables del evento SNMP se ha conservado, excepto para los dos primeros enlaces de variables, TimeStamp y SnmpTrapOID. Estos enlaces se han quitado y se almacenan en las propiedades **TimeStamp** e **Identification** de la clase primaria [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification.](snmpextendednotification.md)

 

 



