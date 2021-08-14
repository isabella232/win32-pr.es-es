---
description: Diseño para la implementación
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Diseño para la implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a755132f1be35ecb6913b7690bce11e342fceb957e63607ee4e9b579bcc758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307320"
---
# <a name="designing-for-deployment"></a>Diseño para la implementación

Planear el ámbito de las aplicaciones COM+ es una tarea de diseño importante que debe tener en cuenta al principio. Los sistemas distribuidos diseñados para ejecutarse con COM+ deben diseñarse para la implementación con la menor cantidad de configuración individual y para usar de forma más eficaz cada proceso. También hay técnicas que puede usar que le permitirán lograr un rendimiento óptimo al implementar una aplicación COM+. (Para obtener más información, vea [Implementación para una comunicación más rápida).](deploying-for-faster-communication.md)

Cuando se ve con la herramienta administrativa Servicios de componentes, cada aplicación COM+ aparece como una carpeta dentro de la cual los conjuntos de componentes se agrupan lógicamente. Aunque puede mover componentes individuales  entre carpetas de componentes de aplicación COM+ (es decir, de una aplicación a otra), varios servicios establecidos en el nivel de aplicación COM+, como la seguridad, pueden diferir. Esta configuración de servicio puede afectar a la portabilidad.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Una aplicación de servidor COM+ define un límite de proceso

Cuando se crea una nueva aplicación de servidor COM+, realmente se define un nuevo límite de proceso. (Observe la excepción para las aplicaciones de biblioteca que se explica a continuación). Este proceso se convierte en la instancia de aplicación de control para los componentes contenidos en la aplicación COM+. Todos estos componentes se ejecutan en proceso en una nueva instancia del programa ejecutable COM+ cada vez que un programa llama a una aplicación COM+ por primera vez. Esto significa que todos los componentes de la carpeta **Components** de una aplicación COM+ determinada se ejecutan en un único espacio de proceso que actúa como servidor DCOM. Dentro de la aplicación COM+, COM+ administra la memoria, la coordinación con Coordinador de transacciones distribuidas (DTC), la activación de instancias de componentes Just-In-Time, la detección y recuperación de bloqueos y la seguridad basada en roles.

## <a name="calling-across-com-application-boundaries"></a>Llamar a través de los límites de la aplicación COM+

Dado que cada aplicación COM+ normalmente se implementa como un ejecutable independiente, el efecto de dividir una aplicación distribuida entre varias aplicaciones COM+ introduce llamadas COM fuera de proceso cuando los componentes de una aplicación COM+ llaman a los componentes de otra aplicación COM+. Esto introduce una degradación del rendimiento debido a la carga adicional que impone la serialización de parámetros COM entre procesos.

> [!Note]  
> No hay nada inherentemente incorrecto al incurrir en esta penalización de rendimiento. Solo tiene que tener en cuenta que se va a producir. Según el tiempo de respuesta necesario, el número de usuarios que solicitarán simultáneamente servicios empresariales y la carga de inicio agregada que cada componente agrega a cada aplicación COM+, es posible que el rendimiento atribuible a las llamadas entre aplicaciones sea aceptable.

 

Una posibilidad que elimina la penalización del rendimiento de llamar a través de los límites de la aplicación COM+ es marcar una aplicación COM+ determinada como una aplicación de biblioteca. Una aplicación de biblioteca COM+ se ejecuta en el proceso del cliente que la crea. Por supuesto, ninguna ganancia de rendimiento tiene un costo cero. En este caso, el intercambio implica las limitaciones de las aplicaciones de biblioteca COM+. Aunque una aplicación de biblioteca puede usar la seguridad basada en roles, no puede admitir componentes en cola ni acceso remoto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementación para una comunicación más rápida](deploying-for-faster-communication.md)
</dt> <dt>

[Diseño para disponibilidad](designing-for-availability.md)
</dt> <dt>

[Diseño para escalabilidad](designing-for-scalability.md)
</dt> <dt>

[Diseño para la seguridad](designing-for-security.md)
</dt> </dl>

 

 



