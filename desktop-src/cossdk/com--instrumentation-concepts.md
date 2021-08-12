---
description: El servicio de instrumentación COM+ le permite crear sus propios programas de registro y administración de eventos COM+ cuando quiera mostrar varias métricas de rendimiento para los componentes de COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Conceptos de instrumentación de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a546c07ea4204f1f4da3ba4c56c76a6eed6b52a8d397d470d0bc34b76adc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549513"
---
# <a name="com-instrumentation-concepts"></a>Conceptos de instrumentación de COM+

El servicio de instrumentación COM+ le permite crear sus propios programas de registro y administración de eventos COM+ cuando quiera mostrar varias métricas de rendimiento para los componentes de COM+. La instrumentación com+ también se puede usar para configurar eventos definidos por el usuario y para convertir eventos COM+ al formato Visual Studio Analyzer (VSA) al actualizar paquetes MTS que reciben eventos MTS.

> [!Note]  
> A partir Windows Server 2003, solo los administradores tienen privilegios de acceso de lectura a los registros de seguimiento de eventos del sistema.

 

Al suscribirse a los eventos publicados por el publicador de eventos del sistema, los clientes pueden implementar las interfaces de instrumentación de COM+ para recibir notificaciones de una variedad de métricas de rendimiento de COM+, como información sobre objetos COM+ [específicos,](com--instrumentation-interfaces.md) aplicaciones COM+ y servicios COM+. Las métricas se publican en el cliente mediante el servicio de eventos [COM+,](com--events.md)un sistema de eventos de acoplamiento flexible (LCE) que almacena información de eventos de distintos publicadores en un almacén de eventos en el catálogo de COM+.

> [!Note]  
> La instrumentación de COM+ no garantiza la entrega de un evento.

 

Cada métrica tiene una marca de tiempo que indica la hora a la que se generó la métrica, no la hora a la que se envió o recibió. El cliente puede correlacionar la marca de tiempo y averiguar el costo de ejecutar una aplicación COM+, el costo de una transacción ejecutada dentro de una aplicación COM+ o el costo de una llamada de método dentro de una aplicación COM+.

También puede usar el servicio de instrumentación COM+ para filtrar por la información de métricas de rendimiento específica que desea ver. Por ejemplo, cuando se suscribe a un método o interfaz de instrumentación com+, puede especificar propiedades para la suscripción en la estructura [**COMSVCSEVENTINFO,**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) como el identificador de aplicación **(miembro guidApp)** o el identificador de proceso **(miembro dwPid).**

Cuando se especifica el identificador de aplicación, solo se reciben las métricas de la aplicación especificada. Cuando se especifica el identificador de proceso, se reciben métricas de la aplicación de servidor y las aplicaciones de biblioteca especificadas que se cargan en ese proceso. El usuario puede especificar el identificador de aplicación y el identificador de proceso, pero el identificador de la aplicación debe ser el de la aplicación de servidor que se ejecuta en el proceso con el identificador de proceso especificado. Si no se especifica ninguno, el usuario recibe métricas de todas las aplicaciones de servidor y biblioteca.

Las métricas de instrumentación com+ proporcionan suficiente información para que la aplicación de supervisión las correlaciona con las métricas del sistema operativo para el análisis de rendimiento, el planeamiento de la capacidad y para el modelado y la predicción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de instrumentación com+](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



