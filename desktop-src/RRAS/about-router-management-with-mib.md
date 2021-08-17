---
title: Acerca de la administración de enrutadores con MIB
description: Las API de Base de información de administración (MIB) para la administración de enrutadores permite consultar y establecer los valores de las variables de MIB exportadas por uno de los administradores de enrutadores o cualquiera de los protocolos de enrutamiento que el servicio de administradores de enrutadores.
ms.assetid: d0fafd82-e7cb-4524-a499-d14830f02b21
keywords:
- Enrutamiento, base de información de administración
- Enrutamiento, base de información de administración, descrito
- RRAS de base de información de administración
- MIB
- MIB, consulte Base de información de administración
- RRAS de base de información de administración
- RRAS de base de información de administración, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a867d903e0fb79f9360dc5f1cb485040ed4489b328365bc2daa063a35fbe27d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792200"
---
# <a name="about-router-management-with-mib"></a>Acerca de la administración de enrutadores con MIB

Las API de Base de información de administración (MIB) para la administración de enrutadores permite consultar y establecer los valores de las variables de MIB exportadas por uno de los administradores de enrutadores o cualquiera de los protocolos de enrutamiento que el servicio de administradores de enrutadores. Mediante esta API, el enrutador admite el Protocolo simple de administración de redes (SNMP).

En el marco SNMP, cada uno de los objetos administrables del enrutador se representa mediante una variable que tiene un identificador de objeto (OID) único. Correspondiente a cada OID es un valor que representa el estado actual del objeto. La colección de ID y valores se conoce como Base de información de administración (MIB). Las llamadas a MprAdminMib permiten a un desarrollador especificar un objeto por su OID y consultar o escribir ("Set") en el valor del objeto.

Para consultar y establecer variables de MIB, el módulo que abate las llamadas debe definir un conjunto de estructuras de datos. Estas estructuras de datos incluyen estructuras que se usarán como identificadores de objeto y estructuras que incluyen los valores de las variables de MIB a las que se tiene acceso. Estas estructuras de datos son opacas para todos, menos para el llamador de la función MIB y el módulo que da servicio a la llamada.

El módulo que da servicio a la llamada MIB es un administrador de enrutadores o uno de los protocolos de enrutamiento. El autor de la llamada debe especificar un administrador de enrutadores incluso si la llamada se controla mediante uno de los protocolos de enrutamiento. En tal caso, el autor de la llamada debe especificar el administrador de enrutadores que corresponde a la familia de protocolos para ese protocolo de enrutamiento. Por ejemplo, si el protocolo de enrutamiento Open Shortest Path First (OSPF) controle la llamada MIB, el autor de la llamada tendría que especificar el Administrador de enrutadores IP, ya que OSPF pertenece a la familia de protocolos IP. En cada una de las funciones de MIB, el parámetro *dwTransportId* especifica un administrador de enrutadores y el parámetro *RoutingPid* especifica el protocolo de enrutamiento. El administrador de enrutadores también tiene un *RoutingPid* único, ya que el propio administrador de enrutadores puede controlar algunas de las variables de MIB.

Se puede llamar a las funciones MprAdminMib en un equipo distinto del que se administra. Las funciones mprAdminMIB que consultan o escriben valores toman como parámetro un identificador para el equipo que se debe administrar. Use la [**función MprAdminMIBServerConnect para**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverconnect) establecer la conexión con el equipo remoto y obtener este identificador. Después de llamar a las funciones de MprAdminMIB necesarias para realizar una tarea administrativa determinada, llame a la función [**MprAdminMIBServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverdisconnect) para finalizar la conexión al equipo remoto.

Las [**funciones MprAdminMIBEntryCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrycreate) y [**MprAdminMIBEntrySet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryset) toman como parámetros un OID y un búfer que contiene el nuevo valor del objeto.

Las funciones [**MprAdminMIBEntryGet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget), [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) y [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) toman como parámetros un OID y la dirección de una variable de puntero. Si la devolución es correcta, la variable de puntero apunta a un búfer que contiene el valor del objeto. El autor de la llamada debe liberar la memoria de este búfer mediante una llamada a la [**función MprAdminMIBBufferFree.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibbufferfree)

Las [**funciones MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) y [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) permiten a un desarrollador realizar un *recorrido de SNMP.* Dado que los OID están ordenados, cada OID y, por tanto, cada objeto administrable tiene un *OID* siguiente. Un recorrido de SNMP hace referencia a recorrer una parte del MIB mediante la lectura o escritura de una secuencia de ID.

Todas las llamadas a MprAdminMib pasan a través del Administrador de interfaces dinámicas (DIM). En función del OID, DIM pasa la llamada a uno de los administradores de enrutadores. (TANTO IP como IPX admiten SNMP). De nuevo, dependiendo del OID, el administrador de enrutadores puede controlar la propia llamada o pasar la llamada a uno de sus clientes. Todos los clientes de enrutador deben implementar y exportar las siguientes funciones que se corresponden con las funciones mprAdminMIB denominadas de forma similar:

-   [**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)
-   [**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)
-   [**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)
-   [**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)
-   [**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)
-   [**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)
-   [**MibGetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)
-   [**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

 

 




