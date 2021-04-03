---
title: Novedades de la versión 2,0 de la API del servidor HTTP
description: Las siguientes características están disponibles en la API del servidor HTTP versión 2,0.
ms.assetid: 236fdbb0-dead-4b73-9ef6-be2d502b5243
keywords:
- Novedades de la versión 2,0 de la API del servidor HTTP
- HTTP Server versión 2,0 API, novedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 932a27a45768d0cb00cde4cb89fc4e5d424d1f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075339"
---
# <a name="whats-new-for-http-server-version-20-api"></a>Novedades de la versión 2,0 de la API del servidor HTTP

La API del servidor HTTP versión 2,0 agrega objetos de configuración de propiedades y administración avanzada de colas de solicitudes. Para obtener más información y una lista completa de funciones, vea el tema de referencia de la [versión 2,0 del servidor http](http-server-api-version-2-0-reference.md) . Las siguientes características están disponibles en la API del servidor HTTP versión 2,0.

## <a name="configuration-objects"></a>Objetos de configuración

Los objetos de configuración de sesión de servidor y de grupo de URL permiten a las aplicaciones configurar el servicio HTTP. La sesión del servidor es el objeto de configuración de nivel superior que invalida la configuración predeterminada de la API del servidor HTTP para todos los grupos de direcciones URL creados en la sesión. El grupo de direcciones URL, creado en una sesión de servidor, mantiene un conjunto de direcciones URL que reciben los valores de configuración del grupo. Para obtener más información, vea el tema [http versión 2,0](http-version-2-0-architecture.md) de la arquitectura.

## <a name="property-configuration-in-version-20"></a>Configuración de propiedades en la versión 2,0

La configuración se realiza en la sesión de servidor o en los objetos de grupo de direcciones URL. Las configuraciones de todo el servidor se establecen en el objeto de configuración de sesión de servidor. Los grupos de direcciones URL, creados en la sesión de servidor, heredan las configuraciones de sesión de servidor. Las configuraciones establecidas en el grupo de direcciones URL invalidan las configuraciones de sesión de servidor. Entre las configuraciones que puede establecer la aplicación se incluyen los tiempos de espera de conexión, los límites de conexiones, la autenticación y el registro. Para obtener más información, vea el tema [Configuring Properties in http Version 2,0](configuring-properties-in-http-version-2-0.md) .

## <a name="process-isolation-on-request-queues"></a>Aislamiento de procesos en las colas de solicitudes

La cola de solicitudes de la versión 2,0 admite el aislamiento de procesos, lo que permite que varios procesos de trabajo realicen la e/s en la cola de solicitudes. Las propiedades de configuración establecidas en la cola de solicitudes permiten a las aplicaciones tener más control sobre el servicio. La característica de cola de solicitudes con nombre permite a las aplicaciones crear colas de solicitudes y protegerlas con listas de Access Control (ACL). Las aplicaciones que funcionan con cuentas de usuario distintas de la cuenta que creó la cola de solicitudes pueden abrir la cola de solicitudes, recibir solicitudes y enviar respuestas. Para obtener más información, consulte el tema [aislamiento de procesos](process-isolation.md) .

## <a name="full-kernel-mode-ssl"></a>SSL de modo kernel completo

La seguridad SSL de modo kernel está habilitada de forma predeterminada; también se admiten certificados de cliente para la autenticación mutua. El rendimiento aumenta al completar las operaciones SSL en modo kernel, lo que reduce las transiciones entre el modo de usuario y el kernel. Para obtener más información, vea el tema [SSL en modo kernel](kernel-mode-ssl.md) .

## <a name="kernel-mode-response-cache"></a>Caché de respuesta de modo kernel

Las respuestas con contenido estático se pueden almacenar en caché en modo kernel, lo que proporciona un mayor rendimiento a través de la memoria caché del modo de usuario. La estructura de la Directiva de caché se envía con la respuesta. Para obtener más información, consulte el tema [caché de modo kernel en HTTP 2,0](kernel-mode-cache-in-http-2-0.md) .

## <a name="authentication"></a>Autenticación

Las \_ estructuras de solicitud HTTP y respuesta HTTP \_ se actualizan para incluir información de autenticación. La autenticación del lado servidor es compatible con los siguientes esquemas: Negotiate, NTLM, Basic y Digest. Las aplicaciones pueden especificar los esquemas de autenticación admitidos y establecer el orden de preferencia para esos esquemas.

## <a name="object-scoped-versioning"></a>Control de versiones con ámbito de objeto

La versión 1,0 de la API del servidor HTTP pasó la información de versión en la llamada a HTTPInitialize. La versión se estableció globalmente para todas las aplicaciones en el mismo proceso. En la API del servidor HTTP versión 2,0, se proporciona la información de versión cuando se crea el objeto. Para obtener más información, vea [control de versiones en la API del servidor http versión 2,0](versioning-in-http-2-0.md).

## <a name="logging"></a>Registro

A partir de la versión 2,0, el registro se puede configurar a través de la API del servidor HTTP. El registro habilitado en una sesión de servidor sirve como forma centralizada de registro para el servicio. También se puede habilitar el registro en un grupo de direcciones URL para los archivos de registro individuales. La aplicación especifica el formato de los archivos de registro, así como los campos en los que se han registrado errores y transacciones correctas.

## <a name="graceful-request-queue-shutdown"></a>Cierre de la cola de solicitudes correcta

Las aplicaciones pueden cerrar la cola de solicitudes y controlar correctamente las solicitudes pendientes en la cola antes de finalizar el proceso de cola de solicitudes. Cuando se cierra la cola de solicitudes, la API del servidor HTTP detiene las solicitudes de puesta en cola y vuelve a enrutar las solicitudes pendientes en la cola de solicitudes.

## <a name="demand-start-on-a-request-queue"></a>Inicio de la demanda en una cola de solicitudes

La característica de inicio de la demanda en la cola de solicitudes permite que la aplicación de controlador retrase la creación de instancias del proceso de trabajo hasta que la primera solicitud llegue a la cola de solicitudes. Por lo tanto, las aplicaciones pueden evitar el consumo de recursos hasta que sean necesarios. Para obtener más información, consulte el tema [Inicio de la demanda en las colas de solicitudes de la versión 2,0](demand-start-on-version-2-0-request-queues.md) .

## <a name="port-sharing"></a>Uso compartido de puertos

Las aplicaciones basadas en la API del servidor HTTP comparten automáticamente el espacio de escucha de IP con otras aplicaciones basadas en la API del servidor no HTTP en el equipo; ya no se necesita la lista de escucha de IP. Cuando la aplicación registra una dirección URL, la API del servidor HTTP solo escucha en la dirección IP y el par de puertos especificados.

## <a name="etw-support"></a>Compatibilidad con ETW

El seguimiento avanzado mediante el seguimiento de eventos para Windows (ETW) permite que las aplicaciones tengan una mayor capacidad de diagnóstico. El seguimiento de eventos está disponible para los registros y reservas de direcciones URL, la configuración de propiedades, los eventos de caché, la autenticación y el registro por nombrar algunos.

## <a name="performance-counters"></a>Contadores de rendimiento

La herramienta contador de rendimiento permite que las aplicaciones recuperen contadores de servicio y diagnostiquen el rendimiento del servicio. Los contadores globales realizan un seguimiento del rendimiento del servicio, los contadores del sitio de seguimiento del rendimiento del grupo de direcciones URL y los contadores de la cola de solicitudes hacen un seguimiento del rendimiento de la cola de solicitudes.

## <a name="international-domain-names-idn"></a>Nombres de dominio internacionales (IDN)

Las partes de la ruta de acceso y el host internacionalizado de la dirección URL permiten el registro de nombres de dominio y rutas no ASCII. La API del servidor HTTP procesa las direcciones URL de Unicode para cumplir con los estándares IDN.

## <a name="netsh-extensions"></a>Extensiones NetSH

La utilidad Netsh reemplaza a la herramienta HttpCfg.exe disponible en Windows Server 2003 y Windows XP con Service Pack 2 (SP2). La extensión netsh proporciona un medio para administrar, diagnosticar y configurar el servicio HTTP. Los administradores pueden consultar y configurar opciones para todo el servidor, como registros de espacios de nombres y certificados SSL.

 

 




