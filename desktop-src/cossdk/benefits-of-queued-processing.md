---
description: Ventajas del procesamiento en cola
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: Ventajas del procesamiento en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0d2068d70ecf611ec334632c8b8f819319ef3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550739"
---
# <a name="benefits-of-queued-processing"></a>Ventajas del procesamiento en cola

Al diseñar nuevas aplicaciones, los desarrolladores deben tener en cuenta las implicaciones de la codificación de componentes para el procesamiento en tiempo real (sincrónico) frente al procesamiento en cola (asincrónico). La elección depende de los requisitos de la aplicación específica según lo determinado por la lógica de negocios subyacente. Como directriz, el procesamiento en cola ofrece las siguientes ventajas con respecto al procesamiento en tiempo real:

-   Dependencia reducida en la disponibilidad de los componentes
-   Vigencia de los componentes más cortos
-   Productividad ininterrumpida al usar aplicaciones desconectadas
-   Confiabilidad de los mensajes
-   Programación de servidores eficaz

## <a name="component-availability"></a>Disponibilidad de componentes

En una aplicación de procesamiento en tiempo real, si solo hay un componente de la transacción disponible (quizás debido a problemas de red o de sobrecarga del servidor), todo el proceso está bloqueado y no se puede completar. Por el contrario, una aplicación que usa el servicio de componentes en cola de COM+ separa la transacción en actividades que se deben completar ahora y las que se pueden completar en un momento posterior. Por ejemplo, los mensajes se pueden poner en cola para su posterior procesamiento, de modo que el componente solicitante sea gratuito para otras tareas.

## <a name="component-lifetimes"></a>Vigencia de los componentes

Una aplicación que usa el servicio de componentes en cola permite que el componente de servidor opere independientemente del cliente. Como resultado, los componentes de servidor se pueden completar con mayor rapidez. En un sistema en tiempo real, el componente de servidor existe desde el momento en que se crea hasta que el objeto se libera finalmente. El servidor espera a que el cliente realice llamadas a métodos y se devuelvan los resultados, lo que niega el ciclo rápido de objetos de servidor y limita la escalabilidad del servidor.

## <a name="disconnected-applications"></a>Aplicaciones desconectadas

El creciente uso de portátiles, notebooks y equipos Palm ha creado una necesidad de aplicaciones que prestan servicio a clientes o usuarios móviles que se desconectan ocasionalmente. En un sistema en cola, estos usuarios pueden seguir trabajando en un escenario sin conexión o cuando no están conectados al servidor y, posteriormente, pueden conectarse a las bases de datos o servidores para procesar sus solicitudes. Por ejemplo, un vendedor puede tomar pedidos de clientes y, posteriormente, conectarse al Departamento de envíos para procesar dichos pedidos.

Si tiene un componente que se puede ejecutar con conexión o sin conexión, los mensajes se desplazan en una dirección y rara vez es necesario cambiar de un servidor a otro. Por ejemplo, en el escenario de realización de pedidos, el componente de envío recibe el mensaje y lo procesa. Puede generar otro componente para la facturación o la auditoría. El cliente se confirma antes de que el servidor se inicie jamás. El mensaje no se envía hasta que se confirma la aplicación.

En la ilustración siguiente se muestra el flujo de información en un escenario desconectado.

![Diagrama que muestra el flujo de información entre el cliente y el servidor.](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a>Confiabilidad de los mensajes

Message Queue Server es una herramienta eficaz que utiliza técnicas de base de datos para ayudar a proteger los datos de una manera robusta. En caso de que se produzca un error en el servidor, Message Queue Server garantiza que las transacciones se revierten para que los mensajes no se pierdan y los datos no estén dañados.

## <a name="server-scheduling"></a>Programación de servidores

Una aplicación que usa componentes en cola es adecuada para la ejecución de componentes desplazados por el tiempo, lo que aplaza el trabajo no crítico hasta un período de poca actividad. Este es el mismo concepto útil que se aplicó al procesamiento en modo por lotes tradicional. El servidor puede diferir las solicitudes similares para la ejecución contigua en lugar de requerir que el servidor reaccione inmediatamente a una gran variedad de solicitudes.

 

 



