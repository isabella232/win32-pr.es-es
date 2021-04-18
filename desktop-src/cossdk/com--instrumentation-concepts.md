---
description: El servicio Instrumental de COM+ le permite compilar sus propios programas de registro y administración de eventos COM+ cuando desee mostrar varias métricas de rendimiento para los componentes COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Conceptos de instrumentación de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714819"
---
# <a name="com-instrumentation-concepts"></a>Conceptos de instrumentación de COM+

El servicio Instrumental de COM+ le permite compilar sus propios programas de registro y administración de eventos COM+ cuando desee mostrar varias métricas de rendimiento para los componentes COM+. La instrumentación de COM+ también se puede utilizar para configurar eventos definidos por el usuario y convertir los eventos COM+ al formato de Visual Studio Analyzer (VSA) al actualizar paquetes MTS que reciben eventos MTS.

> [!Note]  
> A partir de Windows Server 2003, solo los administradores tienen privilegios de acceso de lectura a los registros de seguimiento de eventos del sistema.

 

Al suscribirse a los eventos publicados por el publicador de eventos del sistema, los clientes pueden implementar las [interfaces de instrumentación de com+](com--instrumentation-interfaces.md) para recibir notificaciones para una variedad de métricas de rendimiento de com+, como información sobre objetos com+ específicos, aplicaciones com+ y servicios com+. Las métricas se publican en el cliente mediante el [servicio de eventos com+](com--events.md), un sistema de eventos débilmente acoplados (LCE) que almacena información de eventos de distintos publicadores en un almacén de eventos del catálogo de com+.

> [!Note]  
> La instrumentación de COM+ no garantiza la entrega de un evento.

 

Cada métrica tiene una marca de tiempo que indica la hora a la que se generó la métrica, no el tiempo que se envió o recibió. El cliente puede correlacionar la marca de tiempo y averiguar el costo de ejecutar una aplicación COM+, el costo de una transacción ejecutada dentro de una aplicación COM+ o el costo de una llamada al método dentro de una aplicación COM+.

También puede usar el servicio de instrumentación de COM+ para filtrar la información de métricas de rendimiento específica que desee ver. Por ejemplo, al suscribirse a un método o una interfaz de instrumentación de COM+, puede especificar las propiedades de la suscripción en la estructura [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) , como el identificador de la aplicación (miembro **guidApp** ) o el identificador de proceso (miembro **dwPid** ).

Cuando se especifica el identificador de la aplicación, solo recibe las métricas de la aplicación especificada. Cuando se especifica el identificador de proceso, recibe métricas de la aplicación de servidor y las aplicaciones de biblioteca especificadas que se cargan en ese proceso. El usuario puede especificar el identificador de la aplicación y el identificador del proceso, pero el identificador de la aplicación debe ser el de la aplicación de servidor que se ejecuta en el proceso con el identificador de proceso especificado. Si no se especifica ninguno, el usuario recibe métricas de todas las aplicaciones de servidor y de biblioteca.

Las métricas de instrumentación de COM+ proporcionan información suficiente para que la aplicación de supervisión las correlacione con las métricas del sistema operativo para el análisis de rendimiento, el planeamiento de la capacidad y el modelado y la predicción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de instrumentación de COM+](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



