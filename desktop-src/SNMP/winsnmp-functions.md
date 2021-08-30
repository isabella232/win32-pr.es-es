---
title: Funciones de WinSNMP
description: Las funciones usadas con WinSNMP se agrupan en las siguientes agrupaciones funcionales. A continuación se muestra una lista alfabética.
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c355cb8da6a892614e7729d1db75ded3c3fb9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476961"
---
# <a name="winsnmp-functions"></a>Funciones de WinSNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

Las funciones usadas con WinSNMP se agrupan en las siguientes agrupaciones funcionales. A continuación se muestra una lista alfabética.

-   [Funciones de comunicaciones](#winsnmp-communications-functions)
-   [Funciones de entidad y contexto](#winsnmp-entity-and-context-functions)
-   [Funciones de base de datos](#winsnmp-database-functions)
-   [Funciones PDU](#winsnmp-pdu-functions)
-   [Funciones de la utilidad](#winsnmp-utility-functions)
-   [Funciones de enlace de variables](#winsnmp-variable-binding-functions)
-   [Lista alfabética de funciones winSNMP](/windows)

## <a name="winsnmp-communications-functions"></a>Funciones de comunicaciones de WinSNMP

Las funciones de comunicaciones de WinSNMP proporcionan una interfaz entre la aplicación WinSNMP que realiza la llamada y la implementación de Microsoft WinSNMP. La implementación controla la comunicación entre la aplicación y otras entidades de administración.




| Función | Descripción | 
|----------|-------------|
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>SnmpCancelMsg</strong></a> | Solicita que la implementación de Microsoft WinSNMP cancele los intentos de retransmisión y las notificaciones de tiempo de espera para un mensaje de solicitud SNMP. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a> | Informa a la implementación de que una aplicación se está desconectando y ya no requiere recursos asignados. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>SnmpCleanupEx</strong></a> | Realiza la limpieza cuando no hay llamadas correctas pendientes a <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> o <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> dentro de una aplicación WinSNMP. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a> | Permite que la implementación desasigne los recursos asociados a una sesión y cierre los mecanismos de comunicación. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> | Solicita la implementación para abrir una sesión de WinSNMP y asignar recursos y mecanismos de comunicaciones. Al desarrollar nuevas aplicaciones WinSNMP, se recomienda llamar a la función <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> para abrir una sesión winSNMP en lugar de llamar a <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>la función SnmpOpen.</strong></a> | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>SnmpListen</strong></a> | Registra o anula el registro de una aplicación WinSNMP como agente SNMP. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a> | Solicita la implementación para abrir una sesión de WinSNMP y asignar recursos y mecanismos de comunicaciones. Al desarrollar nuevas aplicaciones WinSNMP, se recomienda llamar a la función <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> para abrir una sesión winSNMP en lugar de llamar a <strong>la función SnmpOpen.</strong> | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a> | Devuelve mensajes SNMP y notificaciones y datos de captura pendientes. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a> | Informa a la implementación de que la aplicación debe registrar o anular el registro de capturas y notificaciones. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a> | Solicita que la implementación transmita una unidad de datos de protocolo. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> | Notifica a la implementación que realice procedimientos de inicialización para la aplicación. Una aplicación debe llamar correctamente <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>a la función SnmpStartup</strong></a> antes de llamar a cualquier otra función WinSNMP. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> | Notifica a la implementación de Microsoft WinSNMP que la aplicación WinSNMP requiere los servicios de la implementación. <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx habilita la</strong></a> compatibilidad con varios módulos de software independientes que usan WinSNMP dentro de la misma aplicación. | 
| <a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a> | Notifica a una sesión de WinSNMP que hay disponible un mensaje SNMP o un evento asincrónico.<blockquote>[!Note]<br />Esta función de devolución de llamada solo se aplica a las sesiones abiertas como resultado de una llamada a la <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>función SnmpCreateSession.</strong></a></blockquote><br /> | 




 

## <a name="winsnmp-entity-and-context-functions"></a>Funciones de entidad y contexto de WinSNMP

Las funciones de entidad y contexto WinSNMP permiten a una aplicación WinSNMP especificar nombres descriptivos para entidades y contextos SNMP. La implementación de Microsoft WinSNMP traduce el nombre a sus componentes SNMPv1 o SNMPv2C mediante la base de datos de la implementación.



| Función                                     | Descripción                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | Devuelve una cadena que identifica un contexto SNMP (un conjunto de recursos de objetos administrados).                                  |
| [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | Devuelve una cadena que identifica una entidad de administración SNMP.                                                            |
| [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | Libera los recursos asignados por la [**función SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) para un contexto SNMP.         |
| [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | Libera los recursos asignados por la [**función SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) para una entidad de administración SNMP. |
| [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | Cambia el puerto asignado a una entidad de destino SNMP.                                                               |
| [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | Devuelve un identificador a la información de contexto de SNMP que es específica de la implementación.                                   |
| [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | Devuelve un identificador a la información de la entidad de administración SNMP que es específica de la implementación.                         |



 

## <a name="winsnmp-database-functions"></a>Funciones de base de datos WinSNMP

Las funciones de base de datos winSNMP proporcionan una aplicación WinSNMP con acceso a la configuración actual en el almacén de información administrativa de la implementación de Microsoft WinSNMP. Estas funciones permiten cambiar el modo de retransmisión y el modo de traducción de entidades y contexto. Las funciones de base de datos también proporcionan a la aplicación la capacidad de manipular los valores de tiempo de espera y recuento de reintentos.



| Función                                               | Descripción                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | Devuelve la configuración actual del modo de retransmisión.                                               |
| [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | Devuelve el valor de recuento de reintentos, en unidades, para la retransmisión de solicitudes de mensajes SNMP.             |
| [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | Devuelve el valor de tiempo de espera, en centésimas de segundo, para la transmisión de solicitudes de mensajes SNMP. |
| [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | Devuelve la configuración actual del modo de traducción de entidades y contexto.                               |
| [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | Recupera información que identifica al proveedor de WinSNMP.                                             |
| [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | Cambia el modo de retransmisión.                                                                      |
| [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | Cambia el valor de recuento de reintentos para la retransmisión de solicitudes de mensajes SNMP.                        |
| [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | Cambia el valor de tiempo de espera para la transmisión de solicitudes de mensajes SNMP.                             |
| [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | Cambia el modo de traducción de entidades y contexto.                                                      |



 

## <a name="winsnmp-pdu-functions"></a>Funciones de PDU de WinSNMP

Las funciones de PDU de WinSNMP permiten a las aplicaciones WinSNMP extraer y actualizar los elementos de datos (o campos) de una PDU. Esto incluye las PDU devueltas por una llamada a la [**función SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) o [**a la función SnmpDecodeMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) Las funciones PDU también construyen PDU para su uso en las [**funciones SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) y [**SnmpEncodeMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)



| Función                                     | Descripción                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | Crea e inicializa una unidad de datos del protocolo SNMP.                                                                                                                               |
| [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | Duplica una unidad de datos del protocolo SNMP.                                                                                                                                            |
| [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | Libera recursos asociados a una unidad de datos del protocolo SNMP creada por [**la función SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o [**SnmpDuplicatePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) |
| [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | Devuelve los elementos de datos seleccionados de una unidad de datos del protocolo SNMP especificada.                                                                                                          |
| [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | Actualiza los elementos de datos seleccionados en una unidad de datos del protocolo SNMP especificada.                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a>Funciones de la utilidad WinSNMP

Las funciones de la utilidad WinSNMP permiten a una aplicación WinSNMP administrar objetos y mensajes SNMP a través de la interfaz WinSNMP.



| Función                                         | Descripción                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | Descodifica un mensaje SNMP codificado o serializado en sus componentes constituyentes.                                      |
| [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | Crea un mensaje SNMP codificado.                                                                                    |
| [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | Indica a la implementación de Microsoft WinSNMP que debe liberar la memoria que asignó para un descriptor específico. |
| [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | Devuelve el último valor de código de error de la última operación SNMP.                                                      |
| [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | Compara dos identificadores de objeto SNMP.                                                                               |
| [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | Copia un identificador de objeto SNMP.                                                                                   |
| [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | Convierte la representación binaria interna de un identificador de objeto SNMP a su formato de cadena numérica de puntos.       |
| [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | Convierte el formato de cadena numérica de puntos de un identificador de objeto SNMP en su representación binaria interna.       |



 

## <a name="winsnmp-variable-binding-functions"></a>Funciones de enlace de variables de WinSNMP

Las funciones de enlace de variables winSNMP permiten a las aplicaciones WinSNMP construir y manipular listas de enlaces de variables e incluirlas en PDU.



| Función                                     | Descripción                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | Enumera las entradas de enlace de variables en una lista de enlaces de variables especificada.                                                                                                   |
| [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | Crea una nueva lista de enlaces de variables.                                                                                                                                            |
| [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | Quita una entrada de enlace de variable de una lista de enlaces de variables.                                                                                                                  |
| [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | Copia una lista de enlaces de variables.                                                                                                                                                 |
| [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | Libera los recursos de una lista de enlaces de variables asignada previamente por [**la función SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) o [**SnmpDuplicateVbl.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) |
| [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | Recupera información de una entrada de enlace de variable especificada.                                                                                                                  |
| [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | Cambia las entradas de enlace de variables en una lista de enlaces de variables; anexa nuevas entradas de enlace de variables a una lista de enlaces de variables existente.                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a>Lista alfabética de funciones winSNMP

-   [**DEVOLUCIÓN DE LLAMADA \_ DE SNMPAPI**](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
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

 

