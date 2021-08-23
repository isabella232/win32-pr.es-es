---
title: Contadores de rendimiento del escenario 3
description: Los contadores de rendimiento miden cantidades de información o datos, según el número, el tamaño, la duración y la tasa de datos que se solicitan o reciben.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92afacf959c72735adea25c3ace60c8ae032da66394dda6731fdab913407e21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950724"
---
# <a name="scenario-3-performance-counters"></a>Escenario 3: Contadores de rendimiento

Los contadores de rendimiento miden cantidades de información o datos, según el número, el tamaño, la duración y la tasa de datos que se solicitan o reciben. No debería esperar obtener una lista de detalles de un contador, como una lista de mensajes de error. En su lugar, use contadores de rendimiento para obtener cantidades, como el número de mensajes de error desde el inicio o la velocidad a la que se generan los mensajes de error.

## <a name="performance-counters-for-httpsys"></a>Contadores de rendimiento para HTTP.sys

A partir de Windows Vista y Windows Server 2008, HTTP.sys tiene los siguientes contadores de métricas de rendimiento para ayudarle con la supervisión, el diagnóstico y el planeamiento de la capacidad de los servidores web: el componente DE API del servidor HTTP tiene los siguientes contadores de rendimiento para ayudarle a supervisar, diagnosticar y planear la capacidad de los servidores web:

- Contadores de servicio HTTP:
  - Número de URI de la memoria caché, agregados desde el inicio, eliminados desde el inicio y número de vaciados de caché
  - Aciertos de caché/segundo y pérdidas de caché/segundo
- Grupos de direcciones URL del servicio HTTP:
  - Velocidad de envío de datos, tasa de recepción de datos, bytes transferidos (enviados y recibidos)
  - Número máximo de conexiones, velocidad de intentos de conexión, tasa de solicitudes GET y HEAD y número total de solicitudes
- Colas de solicitud de servicio HTTP:
  - Número de solicitudes en cola, antigüedad de las solicitudes más antiguas en cola (antigüedad de la última solicitud de la cola)
  - Tasa de llegadas de solicitudes a la cola, tasa de rechazo, número total de solicitudes rechazadas, tasa de aciertos de caché

**Obtener acceso a los contadores de rendimiento**

1.  Escriba **perfmon en** el símbolo del sistema para iniciar la consola de diagnóstico de rendimiento.
2.  Seleccione **Monitor de rendimiento** en el control de árbol y, a continuación, abra **agregar contadores** haciendo clic en **+** .
3.  En **Agregar contadores,** seleccione entre los tres conjuntos de contadores de rendimiento: **Servicio HTTP,** Colas de solicitud de **servicio HTTP** o Grupos de direcciones URL de **servicio HTTP.**
4.  Para ver los contadores de los conjuntos de contadores  Colas de solicitud de servicio **HTTP** y Grupos de direcciones URL de servicio **HTTP,** seleccione instancias y haga clic en Agregar **y,** a continuación, haga clic **en Aceptar.** Para ver los contadores del servicio HTTP, seleccione el conjunto de contadores en el panel izquierdo y haga clic **en Agregar**.

> [!Note]  
> Solo existe una instancia de los contadores de LA API del servidor HTTP por equipo, ya que estos contadores representan el estado de todo el componente. Con las instancias de contadores de rendimiento del grupo de direcciones URL, el identificador de instancia (para el contador de rendimiento) coincidirá con el identificador de grupo de direcciones URL. El identificador del grupo de direcciones URL se puede ver mediante la ejecución **de netsh http show servicestate**. Con las instancias de contadores de rendimiento de las colas de solicitudes, el nombre de instancia corresponde al nombre de la cola de solicitudes. El mismo **netsh http show servicestate** puede mostrar el nombre de la cola de solicitudes (si existe). Sin embargo, algunas aplicaciones de servidor pueden tener colas de solicitudes sin nombre que no pueden coincidir con un identificador de instancia de contador de rendimiento.

 

 

 




