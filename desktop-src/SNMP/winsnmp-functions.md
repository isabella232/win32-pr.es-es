---
title: Funciones WinSNMP
description: Las funciones que se usan con WinSNMP se encuentran en las siguientes agrupaciones funcionales. A continuación se muestra una lista alfabética.
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c5ebb49e8ec56c0d0b1174fd667d847c09d3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149424"
---
# <a name="winsnmp-functions"></a>Funciones WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Las funciones que se usan con WinSNMP se encuentran en las siguientes agrupaciones funcionales. A continuación se muestra una lista alfabética.

-   [Funciones de comunicaciones](#winsnmp-communications-functions)
-   [Funciones de entidad y de contexto](#winsnmp-entity-and-context-functions)
-   [Funciones de base de datos](#winsnmp-database-functions)
-   [Funciones PDU](#winsnmp-pdu-functions)
-   [Funciones de la utilidad](#winsnmp-utility-functions)
-   [Funciones de enlace de variables](#winsnmp-variable-binding-functions)
-   [Lista alfabética de funciones WinSNMP](/windows)

## <a name="winsnmp-communications-functions"></a>Funciones de comunicaciones de WinSNMP

Las funciones de comunicaciones de WinSNMP proporcionan una interfaz entre la aplicación que llama a WinSNMP y la implementación de Microsoft WinSNMP. La implementación controla la comunicación entre la aplicación y otras entidades de administración.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>SnmpCancelMsg</strong></a></td>
<td>Solicita que la implementación de Microsoft WinSNMP cancele los intentos de retransmisión y las notificaciones de tiempo de espera de un mensaje de solicitud SNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a></td>
<td>Informa a la implementación de que una aplicación se está desconectando y ya no requiere recursos asignados.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>SnmpCleanupEx</strong></a></td>
<td>Realiza la limpieza cuando no hay llamadas correctas pendientes a <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> o <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> dentro de una aplicación WinSNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a></td>
<td>Habilita la implementación de para desasignar recursos asociados a una sesión y para cerrar mecanismos de comunicaciones.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a></td>
<td>Solicita la implementación de para abrir una sesión WinSNMP y asignar recursos y mecanismos de comunicaciones. Al desarrollar nuevas aplicaciones WinSNMP, se recomienda llamar a la función <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> para abrir una sesión de WinSNMP en lugar de llamar a la función <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>SnmpListen</strong></a></td>
<td>Registra o anula el registro de una aplicación WinSNMP como agente SNMP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a></td>
<td>Solicita la implementación de para abrir una sesión WinSNMP y asignar recursos y mecanismos de comunicaciones. Al desarrollar nuevas aplicaciones WinSNMP, se recomienda llamar a la función <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> para abrir una sesión de WinSNMP en lugar de llamar a la función <strong>SnmpOpen</strong> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a></td>
<td>Devuelve mensajes SNMP y datos de captura y notificaciones pendientes.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a></td>
<td>Informa a la implementación de que la aplicación necesita registrarse o anular el registro para las capturas y notificaciones.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a></td>
<td>Solicita que la implementación transmita una unidad de datos de protocolo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a></td>
<td>Notifica a la implementación que realice los procedimientos de inicialización de la aplicación. Una aplicación debe llamar correctamente a la función <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> antes de llamar a cualquier otra función WinSNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a></td>
<td>Notifica a la implementación de Microsoft WinSNMP que la aplicación WinSNMP requiere los servicios de la implementación. <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> habilita la compatibilidad con varios módulos de software independientes que usan WinSNMP dentro de la misma aplicación.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a></td>
<td>Notifica a una sesión WinSNMP que un mensaje SNMP o un evento asincrónico está disponible.
<blockquote>
[!Note]<br />
Esta función de devolución de llamada solo se aplica a las sesiones abiertas como resultado de una llamada a la función <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="winsnmp-entity-and-context-functions"></a>Entidades WinSNMP y funciones de contexto

La entidad WinSNMP y las funciones de contexto permiten a una aplicación WinSNMP especificar nombres descriptivos para entidades y contextos SNMP. La implementación de Microsoft WinSNMP traduce el nombre a sus componentes SNMPv1 o SNMPv2C mediante la base de datos de la implementación.



| Función                                     | Descripción                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | Devuelve una cadena que identifica un contexto SNMP (un conjunto de recursos de objetos administrados).                                  |
| [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | Devuelve una cadena que identifica una entidad de administración de SNMP.                                                            |
| [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | Libera los recursos asignados por la función [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) para un contexto SNMP.         |
| [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | Libera los recursos asignados por la función [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) para una entidad de administración de SNMP. |
| [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | Cambia el puerto asignado a una entidad de destino SNMP.                                                               |
| [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | Devuelve un identificador para la información de contexto de SNMP que es específica de la implementación de.                                   |
| [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | Devuelve un identificador para la información de la entidad de administración de SNMP específica de la implementación.                         |



 

## <a name="winsnmp-database-functions"></a>Funciones de base de datos WinSNMP

Las funciones de base de datos WinSNMP proporcionan a una aplicación WinSNMP acceso a la configuración actual del almacén de información administrativa de la implementación de Microsoft WinSNMP. Estas funciones permiten cambiar el modo de retransmisión y el modo de traducción de entidades y contextos. Las funciones de base de datos también proporcionan a la aplicación la capacidad de manipular los valores de recuento de reintentos y de tiempo de espera.



| Función                                               | Descripción                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | Devuelve la configuración actual del modo de retransmisión.                                               |
| [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | Devuelve el valor de número de reintentos, en unidades, para la retransmisión de solicitudes de mensajes SNMP.             |
| [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | Devuelve el valor de tiempo de espera, en centésimas de segundo, para la transmisión de solicitudes de mensajes SNMP. |
| [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | Devuelve la configuración actual de la entidad y el modo de traducción del contexto.                               |
| [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | Recupera información que identifica al proveedor WinSNMP.                                             |
| [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | Cambia el modo de retransmisión.                                                                      |
| [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | Cambia el valor de número de reintentos para la retransmisión de solicitudes de mensajes SNMP.                        |
| [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | Cambia el valor de tiempo de espera para la transmisión de solicitudes de mensajes SNMP.                             |
| [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | Cambia la entidad y el modo de traducción de contexto.                                                      |



 

## <a name="winsnmp-pdu-functions"></a>Funciones de PDU WinSNMP

Las funciones de PDU WinSNMP permiten a las aplicaciones WinSNMP extraer y actualizar los elementos de datos (o campos) de una PDU. Esto incluye las PDU devueltas por una llamada a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) o la función [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) . Las funciones PDU también crean PDU para su uso en las funciones [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) y [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .



| Función                                     | Descripción                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | Crea e inicializa una unidad de datos de protocolo SNMP.                                                                                                                               |
| [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | Duplica una unidad de datos de protocolo SNMP.                                                                                                                                            |
| [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | Libera los recursos asociados a una unidad de datos de protocolo SNMP creada por [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o la función [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) . |
| [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | Devuelve los elementos de datos seleccionados de una unidad de datos de protocolo SNMP especificada.                                                                                                          |
| [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | Actualiza los elementos de datos seleccionados en una unidad de datos de protocolo SNMP especificada.                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a>Funciones de la utilidad WinSNMP

Las funciones de utilidad WinSNMP permiten a una aplicación WinSNMP administrar objetos y mensajes SNMP a través de la interfaz WinSNMP.



| Función                                         | Descripción                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | Descodifica un mensaje SNMP codificado o serializado en sus componentes constituyentes.                                      |
| [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | Crea un mensaje SNMP codificado.                                                                                    |
| [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | Señala a la implementación de Microsoft WinSNMP que debe liberar la memoria asignada para un descriptor específico. |
| [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | Devuelve el último valor de código de error de la última operación SNMP.                                                      |
| [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | Compara dos identificadores de objeto SNMP.                                                                               |
| [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | Copia un identificador de objeto SNMP.                                                                                   |
| [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | Convierte la representación binaria interna de un identificador de objeto SNMP en el formato de cadena numérica con puntos.       |
| [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | Convierte el formato de cadena numérica con puntos de un identificador de objeto SNMP en su representación binaria interna.       |



 

## <a name="winsnmp-variable-binding-functions"></a>Funciones de enlace de variables WinSNMP

Las funciones de enlace de variables WinSNMP permiten a las aplicaciones WinSNMP construir y manipular listas de enlaces de variables, e incluirlas en PDU.



| Función                                     | Descripción                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | Enumera las entradas de enlace de variables en una lista de enlaces de variables especificada.                                                                                                   |
| [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | Crea una nueva lista de enlaces de variables.                                                                                                                                            |
| [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | Quita una entrada de enlace de variables de una lista de enlaces de variables.                                                                                                                  |
| [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | Copia una lista de enlaces de variables.                                                                                                                                                 |
| [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | Libera los recursos para una lista de enlaces de variables asignada previamente por [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) o la función [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . |
| [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | Recupera información de una entrada de enlace de variable especificada.                                                                                                                  |
| [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | Cambia las entradas de enlace de variables en una lista de enlaces de variables. anexa nuevas entradas de enlace de variables a una lista de enlaces de variables existente.                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a>Lista alfabética de funciones WinSNMP

-   [**\_devolución de llamada snmpapi**](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
-   [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)
-   [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)
-   [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)
-   [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)
-   [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)
-   [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)
-   [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)
-   [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)
-   [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)
-   [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)
-   [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)
-   [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)
-   [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)
-   [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)
-   [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)
-   [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)
-   [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)
-   [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)
-   [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)
-   [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)
-   [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)
-   [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode)
-   [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)
-   [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)
-   [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)
-   [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)
-   [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)
-   [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten)
-   [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)
-   [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)
-   [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)
-   [**SnmpOpen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen)
-   [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)
-   [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)
-   [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)
-   [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)
-   [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)
-   [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)
-   [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)
-   [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)
-   [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)
-   [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)
-   [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)
-   [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)
-   [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)
-   [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

 

