---
title: Novedades de la API de servidor HTTP versión 2.0
description: Las siguientes características están disponibles en la API del servidor HTTP versión 2.0.
ms.assetid: 236fdbb0-dead-4b73-9ef6-be2d502b5243
keywords:
- Novedades de la API del servidor HTTP versión 2.0
- API de servidor HTTP versión 2.0, Novedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a145d090add581809375528ad6f10ea08d5da16ee4aed4b8cc046ba9cbbbffd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812045"
---
# <a name="whats-new-for-http-server-version-20-api"></a>Novedades de la API de servidor HTTP versión 2.0

La API del servidor HTTP versión 2.0 agrega objetos de configuración de propiedades y administración avanzada de colas de solicitudes. Para obtener más información y una lista completa de las funciones, vea el tema Referencia de la [versión 2.0 del](http-server-api-version-2-0-reference.md) servidor HTTP. Las siguientes características están disponibles en la API del servidor HTTP versión 2.0.

## <a name="configuration-objects"></a>Objetos de configuración

La sesión del servidor y los objetos de configuración del grupo de direcciones URL permiten a las aplicaciones configurar el servicio HTTP. La sesión del servidor es el objeto de configuración de nivel superior que invalida la configuración predeterminada de la API del servidor HTTP para todos los grupos de direcciones URL creados en la sesión. El grupo de direcciones URL, creado en una sesión de servidor, mantiene un conjunto de direcciones URL que reciben los valores de configuración del grupo. Para obtener más información, vea el [tema Arquitectura de la versión 2.0 de HTTP.](http-version-2-0-architecture.md)

## <a name="property-configuration-in-version-20"></a>Configuración de propiedades en la versión 2.0

La configuración se realiza en la sesión del servidor o en los objetos de grupo de direcciones URL. Las configuraciones de todo el servidor se establecen en el objeto de configuración de sesión del servidor. Los grupos de direcciones URL, creados en la sesión del servidor, heredan las configuraciones de sesión del servidor. Las configuraciones establecidas en el grupo de direcciones URL invalidan las configuraciones de sesión del servidor. Las configuraciones que puede establecer la aplicación incluyen tiempos de espera de conexión, límites de conexiones, autenticación y registro. Para obtener más información, vea [el tema Configuring Properties in HTTP Version 2.0](configuring-properties-in-http-version-2-0.md) .

## <a name="process-isolation-on-request-queues"></a>Aislamiento de procesos en colas de solicitudes

La cola de solicitudes de la versión 2.0 admite el aislamiento de procesos, lo que permite que varios procesos de trabajo realicen E/S en la cola de solicitudes. Las propiedades de configuración establecidas en la cola de solicitudes permiten a las aplicaciones tener más control sobre el servicio. La característica cola de solicitudes con nombre permite a las aplicaciones crear colas de solicitudes y protegerlas con Access Control listas de solicitudes (ACL). Las aplicaciones que funcionan con cuentas de usuario que no sean la cuenta que creó la cola de solicitudes pueden abrir la cola de solicitudes, recibir solicitudes y enviar respuestas. Para obtener más información, vea el [tema Aislamiento de](process-isolation.md) procesos.

## <a name="full-kernel-mode-ssl"></a>SSL en modo kernel completo

La seguridad SSL del modo kernel está habilitada de forma predeterminada; también se admiten certificados de cliente para la autenticación mutua. El rendimiento aumenta al completar las operaciones SSL en modo kernel, lo que reduce las transiciones entre el modo de kernel y el modo de usuario. Para obtener más información, consulte el [tema SSL del modo kernel.](kernel-mode-ssl.md)

## <a name="kernel-mode-response-cache"></a>Caché de respuestas en modo kernel

Las respuestas con contenido estático se pueden almacenar en caché en modo kernel, lo que proporciona un mayor rendimiento sobre la caché del modo de usuario. La estructura de la directiva de caché se envía con la respuesta. Para obtener más información, vea el tema Caché en modo [kernel en HTTP 2.0.](kernel-mode-cache-in-http-2-0.md)

## <a name="authentication"></a>Authentication

Las estructuras HTTP \_ RESPONSE y HTTP REQUEST se actualizan para incluir información de \_ autenticación. La autenticación del lado servidor se admite para los siguientes esquemas: Negotiate, NTLM, Basic e Digest. Las aplicaciones pueden especificar los esquemas de autenticación admitidos y establecer el orden de preferencia para esos esquemas.

## <a name="object-scoped-versioning"></a>Control de versiones con ámbito de objeto

La API del servidor HTTP versión 1.0 pasó información de versión en la llamada a HTTPInitialize. La versión se estableció globalmente para todas las aplicaciones en el mismo proceso. En la API del servidor HTTP versión 2.0, la información de versión se proporciona cuando se crea el objeto. Para obtener más información, vea [Control de versiones en la API de servidor HTTP versión 2.0.](versioning-in-http-2-0.md)

## <a name="logging"></a>Registro

A partir de la versión 2.0, el registro se puede configurar mediante la API del servidor HTTP. El registro habilitado en una sesión de servidor actúa como forma centralizada de registro para el servicio. El registro también se puede habilitar en un grupo de direcciones URL para archivos de registro individualizados. La aplicación especifica el formato de los archivos de registro, así como los campos que se registran en busca de errores y transacciones correctas.

## <a name="graceful-request-queue-shutdown"></a>Cierre de cola de solicitudes correctas

Las aplicaciones pueden apagar la cola de solicitudes y controlar correctamente las solicitudes pendientes en la cola antes de finalizar el proceso de la cola de solicitudes. Cuando se cierra la cola de solicitudes, la API del servidor HTTP deja de poner en cola las solicitudes y vuelve a enrutar las solicitudes pendientes en la cola de solicitudes.

## <a name="demand-start-on-a-request-queue"></a>Inicio de la demanda en una cola de solicitudes

La característica de inicio de la demanda en la cola de solicitudes permite que la aplicación del controlador retrase la creación de instancias del proceso de trabajo hasta que la primera solicitud llegue a la cola de solicitudes. Por lo tanto, las aplicaciones pueden evitar el consumo de recursos hasta que se requieran. Para obtener más información, vea el [tema Demand Start on Version 2.0 Request Queues](demand-start-on-version-2-0-request-queues.md) (Inicio de la demanda en las colas de solicitudes de la versión 2.0).

## <a name="port-sharing"></a>Uso compartido de puertos

Las aplicaciones basadas en API de servidor HTTP comparten automáticamente el espacio de escucha ip con otras aplicaciones no basadas en API de servidor HTTP en el equipo; la lista de escucha de IP ya no es necesaria. Cuando la aplicación registra una dirección URL, la API del servidor HTTP solo escucha en la dirección IP y el par de puertos especificados.

## <a name="etw-support"></a>Compatibilidad con ETW

El seguimiento avanzado mediante el seguimiento de eventos para Windows (ETW) permite a las aplicaciones mayores capacidades de diagnóstico. El seguimiento de eventos está disponible para registros y reservas de direcciones URL, configuración de propiedades, eventos de caché, autenticación y registro por nombrar algunos.

## <a name="performance-counters"></a>Contadores de rendimiento

La herramienta de contador de rendimiento permite a las aplicaciones recuperar contadores de servicio y diagnosticar el rendimiento del servicio. Los contadores globales hacen un seguimiento del rendimiento del servicio, los contadores de sitio hacen un seguimiento del rendimiento del grupo de direcciones URL y los contadores de cola de solicitudes hacen un seguimiento del rendimiento de la cola de solicitudes.

## <a name="international-domain-names-idn"></a>Nombres de dominio internacionales (IDN)

Las partes de host y ruta de acceso internacionalizadas de la dirección URL permiten el registro de rutas de acceso y nombres de dominio no ASCII. La API del servidor HTTP procesa direcciones URL Unicode para cumplir con los estándares de IDN.

## <a name="netsh-extensions"></a>Extensiones netSH

La utilidad netsh reemplaza la herramienta HttpCfg.exe disponible en Windows Server 2003 y Windows XP por Service Pack 2 (SP2). La extensión netsh proporciona un medio para administrar, diagnosticar y configurar el servicio HTTP. Los administradores pueden consultar y configurar opciones para todo el servidor, como registros de espacios de nombres y certificados SSL.

 

 




