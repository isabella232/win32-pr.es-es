---
title: Descripción de las funciones de administración de enrutadores
description: En las secciones siguientes se deberán analizar los distintos tipos de funciones de administración de enrutadores y lo que debe saber para usarlas de forma eficaz.
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85aac5cc2ec0167527f07c04459ec0aed7dbc248bed727fb4a949765c2fdcc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025405"
---
# <a name="understanding-router-management-functions"></a>Descripción de las funciones de administración de enrutadores

En las secciones siguientes se deberán analizar los distintos tipos de funciones de administración de enrutadores y lo que debe saber para usarlas de forma eficaz.

Todas las funciones de administración de enrutadores requieren privilegios de administrador. Un usuario del grupo Power User no tiene privilegios suficientes para usar las funciones de administración del enrutador.

## <a name="the-different-classes-of-router-management-functions"></a>Las distintas clases de funciones de administración de enrutadores

Las funciones de administración del enrutador se pueden dividir en las funciones de administración y las funciones de configuración. Las [funciones de administración](router-administration-functions.md) tienen un prefijo mprAdmin y las funciones [de](router-configuration-functions.md) configuración tienen un prefijo mprConfig. A pesar de la nomenclatura, ambos conjuntos de funciones se usan para la administración de enrutadores. Las funciones MprAdmin funcionan directamente en el enrutador en ejecución. Las funciones mprConfig tienen una funcionalidad similar, pero funcionan en la configuración del enrutador almacenada en el registro. Ambos tipos de funciones pasan [bloques de información](router-information-functions.md).

Las funciones de administración del enrutador también se pueden dividir en función de los componentes del enrutador que administran: interfaces, administradores de enrutadores o clientes del administrador de enrutadores.

Las [funciones de interfaz de enrutador](router-interface-functions.md) tienen un prefijo de MprAdminInterface o MprConfigInterface. Use estas funciones para acceder a las interfaces. Las [funciones del administrador de enrutadores](router-manager-transport-functions.md) tienen un prefijo mprAdminTransport o MprConfigTransport. Use estas funciones para acceder a los administradores de enrutadores. Por último, las [funciones de cliente del administrador de enrutadores](router-manager-client-interfacetransport-functions.md) tienen un prefijo mprAdminInterfaceTransport o MprConfigInterfaceTransport. Use estas funciones para acceder a los clientes que se ejecutan en el enrutador.

Un subconjunto de funciones MprAdmin son las [funciones MprAdminMib](/windows/desktop/RRAS/about-router-management-with-mib). También funcionan solo en la ruta en ejecución. Sin embargo, estas funciones no pasan bloques de información. Estas funciones proporcionan flexibilidad adicional al diseñador de protocolos, especialmente para recuperar información que no es de configuración, como estadísticas.

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>Asegurarse de que los cambios se producen inmediatamente y son persistentes

Un desarrollador puede realizar cambios en la configuración del enrutador directamente mediante las [funciones de configuración del enrutador](router-configuration-functions.md). Sin embargo, los cambios realizados en la configuración no tienen efecto hasta que se reinicia el enrutador, ya que esta es la única vez que DIM lee la configuración del Registro.

Un desarrollador puede realizar cambios en el enrutador en ejecución mediante las funciones [de administración del enrutador](router-administration-functions.md). Sin embargo, estos cambios no son persistentes: como no se han escrito en el registro, se pierden si se reinicia el enrutador.

Para realizar cambios inmediatos y persistentes, un desarrollador debe usar la administración del enrutador y las funciones de configuración del enrutador. Si el enrutador no se está ejecutando, el desarrollador solo necesita llamar a las funciones de configuración de enrutador adecuadas.

Para consultar información del enrutador en ejecución, use las funciones de administración del enrutador. Si el enrutador no se está ejecutando, consulte la información mediante las funciones de configuración del enrutador.

Las [**funciones MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) y [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) admiten la estructura [**\_ MPR INTERFACE \_ 2.**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2) Sin embargo, [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) [**y MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) no lo hacen. Para crear una interfaz de marcado a petición que sea persistente después de un reinicio, llame a **MprAdminInterfaceCreate** con **MPR \_ INTERFACE \_ 2** y, a continuación, llame a **MprConfigInterfaceCreate** con [**MPR \_ INTERFACE \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) o [**MPR INTERFACE \_ \_ 1.**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1) De forma similar, para realizar cambios persistentes en una interfaz de marcado a petición, llame a **MprAdminInterfaceSetInfo** con **MPR \_ INTERFACE \_ 2** y, a continuación, llame a **MprConfigInterfaceSetInfo** con **MPR \_ INTERFACE \_ 0** o **MPR INTERFACE \_ \_ 1.**

## <a name="using-router-administration-and-configuration-functions-remotely"></a>Uso remoto de funciones de configuración y administración de enrutadores

Se puede llamar a la mayoría de las funciones de configuración y administración del enrutador en un equipo que no sea el que se administra. Estas funciones toman como parámetro, un identificador para el servicio de enrutador o la configuración que se debe administrar. Las funciones de administración usan RPC (llamada a procedimiento remoto) para comunicarse con el servicio de enrutamiento especificado por el identificador. Las funciones de configuración escriben y leen en el Registro del equipo especificado por el identificador.

Para administrar el servicio de enrutamiento en un equipo remoto, llame primero a [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) para comprobar que el servicio se está ejecutando. A [**continuación, llame a MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) para obtener el identificador. Si el servicio de enrutador no se ejecuta en el equipo remoto, se producirá un error en todas las llamadas de administración de enrutadores (MprAdmin).

Para realizar cambios en la configuración del enrutador en un equipo remoto, obtenga un identificador mediante una llamada a la [**función MprConfigServerConnect.**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect)

 

 