---
title: Descripción de las funciones de administración de enrutadores
description: En las secciones siguientes se describen los diferentes tipos de funciones de administración de enrutadores y lo que debe saber para usarlos de forma eficaz.
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b1891bc55b80a18a6d0dd928044da1e0e9709
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676463"
---
# <a name="understanding-router-management-functions"></a>Descripción de las funciones de administración de enrutadores

En las secciones siguientes se describen los diferentes tipos de funciones de administración de enrutadores y lo que debe saber para usarlos de forma eficaz.

Todas las funciones de administración del enrutador requieren privilegios de administrador. Un usuario del grupo usuarios avanzados no tiene privilegios suficientes para usar las funciones de administración del enrutador.

## <a name="the-different-classes-of-router-management-functions"></a>Las distintas clases de funciones de administración del enrutador

Las funciones de administración del enrutador se pueden dividir en las funciones de administración y en las funciones de configuración. Las [funciones de administración](router-administration-functions.md) tienen un prefijo de MprAdmin y las [funciones de configuración](router-configuration-functions.md) tienen un prefijo de MprConfig. A pesar de la denominación, ambos conjuntos de funciones se usan para la administración de enrutadores. Las funciones de MprAdmin funcionan directamente en el enrutador en ejecución. Las funciones MprConfig tienen una funcionalidad similar, pero operan en la configuración del enrutador almacenada en el registro. Ambos tipos de funciones pasan [bloques de información](router-information-functions.md).

Las funciones de administración del enrutador también se pueden dividir en función de los componentes del enrutador que administren: interfaces, administradores de enrutadores o clientes del administrador de enrutadores.

Las [funciones de interfaz de enrutador](router-interface-functions.md) tienen un prefijo de MprAdminInterface o MprConfigInterface. Use estas funciones para tener acceso a las interfaces. Las [funciones del administrador de enrutadores](router-manager-transport-functions.md) tienen un prefijo de MprAdminTransport o MprConfigTransport. Use estas funciones para tener acceso a los administradores del enrutador. Por último, las [funciones de cliente del administrador de enrutador](router-manager-client-interfacetransport-functions.md) tienen un prefijo de MprAdminInterfaceTransport o MprConfigInterfaceTransport. Use estas funciones para tener acceso a los clientes que se ejecutan en el enrutador.

Un subconjunto de las funciones de MprAdmin son las [funciones MprAdminMib](/windows/desktop/RRAS/about-router-management-with-mib). También funcionan solo en la ruta en ejecución. Sin embargo, estas funciones no pasan bloques de información. Estas funciones proporcionan una mayor flexibilidad al diseñador de protocolos, especialmente para recuperar información que no sea de configuración, como las estadísticas.

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>Asegurarse de que los cambios se producen inmediatamente y son persistentes

Un programador puede realizar cambios en la configuración del enrutador directamente mediante las [funciones de configuración del enrutador](router-configuration-functions.md). Sin embargo, los cambios que se realicen en la configuración no surtirán efecto hasta que se reinicie el enrutador, ya que es el único momento en que la DIM lee la configuración del registro.

Un desarrollador puede realizar cambios en el enrutador en ejecución mediante las [funciones de administración del enrutador](router-administration-functions.md). Sin embargo, estos cambios no son persistentes: dado que no se han escrito en el registro, se pierden si el enrutador se reinicia.

Para realizar cambios que son inmediatos y persistentes, un desarrollador necesita usar las funciones de configuración de enrutador y de administración del enrutador. Si el enrutador no se está ejecutando, el desarrollador solo necesita llamar a las funciones de configuración de enrutador adecuadas.

Para consultar información del enrutador en ejecución, use las funciones de administración del enrutador. Si el enrutador no se está ejecutando, consulte la información con las funciones de configuración del enrutador.

Las funciones [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) y [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) admiten la estructura de la [**interfaz de MPR \_ \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2) . Sin embargo, [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) y [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) no lo hacen. Para crear una interfaz de marcado a petición que sea persistente después de reiniciar, llame a **MprAdminInterfaceCreate** con la **interfaz de MPR \_ \_ 2** y, a continuación, llame a **MprConfigInterfaceCreate** con la interfaz de [**MPR \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) o la [**interfaz de MPR \_ \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1). Del mismo modo, para realizar cambios persistentes en una interfaz de marcado a petición, llame a **MprAdminInterfaceSetInfo** con la **interfaz de MPR \_ \_ 2** y, a continuación, llame a **MprConfigInterfaceSetInfo** con la interfaz de **MPR \_ \_ 0** o la **interfaz de MPR \_ \_ 1**.

## <a name="using-router-administration-and-configuration-functions-remotely"></a>Usar funciones de configuración y administración de enrutadores de forma remota

La mayoría de las funciones de configuración y administración del enrutador se pueden llamar en un equipo distinto del que se está administrando. Estas funciones toman como parámetro un identificador del servicio de enrutador o la configuración que se va a administrar. Las funciones de administración utilizan RPC (llamada a procedimiento remoto) para comunicarse con el servicio de enrutamiento especificado por el identificador. Las funciones de configuración escriben y leen en el registro del equipo especificado por el identificador.

Para administrar el servicio de enrutamiento en un equipo remoto, llame primero a [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) para comprobar que el servicio se está ejecutando. A continuación, llame a [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) para obtener el identificador. Si el servicio de enrutador no se está ejecutando en el equipo remoto, se producirá un error en todas las llamadas de administración del enrutador (MprAdmin).

Para realizar cambios en la configuración del enrutador de un equipo remoto, obtenga un identificador mediante una llamada a la función [**MprConfigServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect) .

 

 