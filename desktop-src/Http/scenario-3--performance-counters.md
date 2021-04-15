---
title: Contadores de rendimiento de escenario 3
description: Los contadores de rendimiento miden cantidades de información o datos, según el número, el tamaño, la duración y la velocidad de los datos que se solicitan o reciben.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/27/2020
ms.locfileid: "105665887"
---
# <a name="scenario-3-performance-counters"></a>Escenario 3: contadores de rendimiento

Los contadores de rendimiento miden cantidades de información o datos, según el número, el tamaño, la duración y la velocidad de los datos que se solicitan o reciben. No debería esperar obtener una lista de detalles de un contador, como una lista de mensajes de error. En su lugar, utilice los contadores de rendimiento para obtener cantidades, como el número de mensajes de error desde el inicio o la velocidad a la que se generan los mensajes de error.

## <a name="performance-counters-for-httpsys"></a>Contadores de rendimiento para HTTP.sys

A partir de Windows Vista y Windows Server 2008, HTTP.sys tiene los siguientes contadores de métricas de rendimiento para ayudarle con la supervisión, el diagnóstico y la planificación de capacidad para los servidores Web: el componente API de servidor HTTP tiene los siguientes contadores de rendimiento para ayudarle con la supervisión, el diagnóstico y el planeamiento de capacidad para servidores Web:

- Contadores de servicios HTTP:
  - Número de URI en la memoria caché, agregados desde el inicio, eliminados desde el inicio y número de vaciados de caché
  - Aciertos de caché/segundo y errores de caché por segundo
- Grupos de direcciones URL del servicio HTTP:
  - Velocidad de envío de datos, velocidad de recepción de datos, bytes transferidos (enviados y recibidos)
  - Número máximo de conexiones, frecuencia de intentos de conexión, velocidad para solicitudes GET y HEAD y número total de solicitudes
- Colas de solicitudes de servicio HTTP:
  - Número de solicitudes en cola, antigüedad de las solicitudes más antiguas en la cola (antigüedad de la última solicitud en la cola)
  - Velocidad de llegada de la solicitud a la cola, tasa de rechazo, número total de solicitudes rechazadas, tasa de aciertos de caché

**Obtener acceso a los contadores de rendimiento**

1.  Escriba **Perfmon** en el símbolo del sistema para iniciar la consola de diagnóstico de rendimiento.
2.  Seleccione **monitor de rendimiento** en el control de árbol y, a continuación, Abra **Agregar contadores** haciendo clic en **+** .
3.  En **Agregar contadores** , seleccione entre los tres conjuntos de contadores de rendimiento: **servicio http**, **colas de solicitudes de servicio http** o **grupos de direcciones URL de servicio http**.
4.  Para ver los contadores de los conjuntos de contadores **colas de solicitudes de servicio http** y **grupos de direcciones URL de servicio http** , seleccione **instancias** , haga clic en **Agregar** y, a continuación, haga clic en **Aceptar**. Para ver los contadores de servicio HTTP, seleccione el conjunto de contadores en el panel izquierdo y haga clic en **Agregar**.

> [!Note]  
> Solo existe una instancia de los contadores de API del servidor HTTP por equipo, ya que estos contadores representan el estado de todo el componente. Con instancias de contadores de rendimiento de grupo de direcciones URL, el ID. de instancia (para el contador de rendimiento) coincidirá con el identificador de grupo de URL. El identificador de grupo de URL se puede ver ejecutando **netsh http show servicestate**. Con instancias de contadores de rendimiento de colas de solicitudes, el nombre de instancia corresponde al nombre de la cola de solicitudes. El nombre de la cola de solicitudes (si existe) se puede mostrar en el mismo **netsh http show servicestate**. Sin embargo, algunas aplicaciones de servidor pueden tener colas de solicitudes sin nombre que no se puedan asociar a un identificador de instancia de contador de rendimiento.

 

 

 




