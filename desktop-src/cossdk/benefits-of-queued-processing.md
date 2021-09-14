---
description: Ventajas del procesamiento en cola
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: Ventajas del procesamiento en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0d2068d70ecf611ec334632c8b8f819319ef3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073010"
---
# <a name="benefits-of-queued-processing"></a>Ventajas del procesamiento en cola

Al diseñar nuevas aplicaciones, los desarrolladores deben tener en cuenta las implicaciones de codificar componentes para el procesamiento en tiempo real (sincrónico) frente al procesamiento en cola (asincrónico). La elección depende de los requisitos de la aplicación específica según lo determinado por la lógica de negocios subyacente. Como guía, el procesamiento en cola ofrece las siguientes ventajas con respecto al procesamiento en tiempo real:

-   Dependencia reducida de la disponibilidad de componentes
-   Duraciones de componentes más cortas
-   Productividad ininterrumpida al usar aplicaciones desconectadas
-   Confiabilidad de mensajes
-   Programación eficaz del servidor

## <a name="component-availability"></a>Disponibilidad de componentes

En una aplicación de procesamiento en tiempo real, si solo un componente de la transacción no está disponible (quizás debido a problemas de red o sobrecarga del servidor), todo el proceso se bloquea y no se puede completar. Por el contrario, una aplicación que usa el servicio de componentes en cola de COM+ separa la transacción en actividades que deben completarse ahora y las que se pueden completar más adelante. Por ejemplo, los mensajes se pueden poner en cola para su posterior procesamiento para que el componente solicitante sea gratuito para otras tareas.

## <a name="component-lifetimes"></a>Duraciones de los componentes

Una aplicación que usa el servicio de componentes en cola permite que el componente de servidor funcione independientemente del cliente. Como resultado, los componentes del servidor se pueden completar más rápidamente. En un sistema en tiempo real, el componente de servidor existe desde el momento en que se crea hasta que el objeto se libera finalmente. El servidor espera a que el cliente realice llamadas a métodos y que se devuelvan resultados, lo que niega el ciclo rápido de objetos de servidor y limita la escalabilidad del servidor.

## <a name="disconnected-applications"></a>Aplicaciones desconectadas

El uso creciente de equipos portátiles, cuadernos y equipos de mano ha creado una necesidad de aplicaciones que a veces abate a clientes o usuarios móviles desconectados. En un sistema en cola, estos usuarios pueden seguir trabajando en un escenario desconectado o cuando no están conectados al servidor y, posteriormente, pueden conectarse a las bases de datos o servidores para procesar sus solicitudes. Por ejemplo, un vendedor puede tomar pedidos de los clientes y, posteriormente, conectarse al departamento de envío para procesar esos pedidos.

Si tiene un componente que se puede ejecutar conectado o desconectado, los mensajes viajan en una dirección y rara vez es necesario cambiar de un lado a otro. Por ejemplo, en el escenario de toma de pedidos, el componente de envío recibe el mensaje y lo procesa. Puede generar otro componente para facturación o auditoría. El cliente se confirma antes de que se inicie el servidor. El mensaje no se envía hasta que se confirma la aplicación.

En la ilustración siguiente se muestra el flujo de información en un escenario desconectado.

![Diagrama que muestra el flujo de información entre el cliente y el servidor.](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a>Confiabilidad de mensajes

Message Queuing es una herramienta eficaz que usa técnicas de base de datos para ayudar a proteger los datos de una manera sólida. En caso de error del servidor, Message Queuing garantiza que las transacciones se revierte para que los mensajes no se pierdan y los datos no estén dañados.

## <a name="server-scheduling"></a>Programación de servidores

Una aplicación que usa componentes en cola es adecuada para la ejecución de componentes con desplazamiento de tiempo, lo que aplaza el trabajo no crítico a un período de poco actividad. Este es el mismo concepto útil que se aplicó al procesamiento en modo por lotes tradicional. El servidor puede aplazar solicitudes similares para su ejecución contigua en lugar de requerir que el servidor reaccione inmediatamente a una amplia variedad de solicitudes.

 

 



