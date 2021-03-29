---
title: Acerca de la administración de enrutadores con MIB
description: Las API de base de información de administración (MIB) para la administración de enrutadores permiten consultar y establecer los valores de las variables MIB exportadas por uno de los administradores de enrutadores o cualquiera de los protocolos de enrutamiento que el servicio de administradores de enrutadores.
ms.assetid: d0fafd82-e7cb-4524-a499-d14830f02b21
keywords:
- Enrutamiento, base de información de administración
- Enrutamiento, base de información de administración, descripción
- RRAS base de información de administración
- MIB
- MIB, consulte base de información de administración
- RRAS base de información de administración
- Base de información de administración RRAS, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e015dacc0b36a00ab62d42c710551aa368aa59e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776741"
---
# <a name="about-router-management-with-mib"></a>Acerca de la administración de enrutadores con MIB

Las API de base de información de administración (MIB) para la administración de enrutadores permiten consultar y establecer los valores de las variables MIB exportadas por uno de los administradores de enrutadores o cualquiera de los protocolos de enrutamiento que el servicio de administradores de enrutadores. Mediante esta API, el enrutador es compatible con el Protocolo simple de administración de redes (SNMP).

En el marco SNMP, cada uno de los objetos que se administran en el enrutador se representa mediante una variable que tiene un identificador de objeto único (OID). Correspondiente a cada OID es un valor que representa el estado actual del objeto. La colección de OID y valores se conoce como base de datos de información de administración (MIB). Las llamadas MprAdminMib permiten a los desarrolladores especificar un objeto por su OID y consulta o escritura ("SET") el valor del objeto.

Para consultar y establecer variables MIB, el módulo que renueva las llamadas debe definir un conjunto de estructuras de datos. Estas estructuras de datos incluyen estructuras que se usan como identificadores de objeto y estructuras que contienen los valores de las variables MIB a las que se tiene acceso. Estas estructuras de datos son opacas para todo excepto el autor de la llamada de la función MIB y el módulo que atiende la llamada.

El módulo que atiende la llamada MIB es un administrador de enrutador o uno de los protocolos de enrutamiento. El autor de la llamada debe especificar un administrador de enrutadores aunque la llamada sea administrada por uno de los protocolos de enrutamiento. En tal caso, el autor de la llamada debe especificar el administrador del enrutador que corresponde a la familia de protocolos para ese protocolo de enrutamiento. Por ejemplo, si el protocolo de enrutamiento abrir primero la ruta de acceso más corta (OSPF) estaba controlando la llamada MIB, el autor de la llamada tendría que especificar el administrador del enrutador IP, ya que OSPF pertenece a la familia del protocolo IP. En cada una de las funciones MIB, el parámetro *dwTransportId* especifica un administrador de enrutadores y el parámetro *RoutingPid* especifica el protocolo de enrutamiento. El administrador de enrutadores también tiene un *RoutingPid* único, ya que algunas de las variables MIB pueden ser controladas por el propio administrador de enrutador.

Se puede llamar a las funciones MprAdminMib en un equipo que no sea el que se está administrando. Las funciones MprAdminMIB que consultan o escriben valores, toman como parámetro un identificador para el equipo que se va a administrar. Utilice la función [**MprAdminMIBServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverconnect) para establecer la conexión con el equipo remoto y obtener este identificador. Después de llamar a las funciones de MprAdminMIB necesarias para realizar una tarea administrativa determinada, llame a la función [**MprAdminMIBServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverdisconnect) para finalizar la conexión al equipo remoto.

Las funciones [**MprAdminMIBEntryCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrycreate) y [**MprAdminMIBEntrySet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryset) toman como parámetros un OID y un búfer que contiene el nuevo valor para el objeto.

Las funciones [**MprAdminMIBEntryGet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget), [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) y [**MPRADMINMIBENTRYGETNEXT**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) toman como parámetros un OID y la dirección de una variable de puntero. Si la devolución es correcta, la variable de puntero señala a un búfer que contiene el valor del objeto. El llamador debe liberar la memoria para este búfer mediante una llamada a la función [**MprAdminMIBBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibbufferfree) .

Las funciones [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) y [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) permiten a los desarrolladores realizar un *recorrido de SNMP*. Dado que los OID están ordenados, cada OID y, por tanto, cada objeto administrable tiene un OID *siguiente* . Un recorrido de SNMP hace referencia al recorrido de una parte de la MIB mediante la lectura o escritura de una secuencia de OID.

Todas las llamadas a MprAdminMib pasan a través del administrador de interfaz dinámica (DIM). Dependiendo del OID, DIM pasa la llamada a uno de los administradores de enrutadores. (Tanto IP como IPX admiten SNMP). De nuevo, dependiendo del OID, el administrador de enrutador puede controlar la propia llamada o pasar la llamada a uno de sus clientes. Todos los clientes de enrutador deben implementar y exportar las funciones siguientes, que corresponden a las funciones de MprAdminMIB con el mismo nombre:

-   [**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)
-   [**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)
-   [**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)
-   [**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)
-   [**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)
-   [**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)
-   [**MibGetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)
-   [**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

 

 




