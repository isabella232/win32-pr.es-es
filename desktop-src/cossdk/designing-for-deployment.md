---
description: Diseñar para la implementación
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Diseñar para la implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496037"
---
# <a name="designing-for-deployment"></a>Diseñar para la implementación

Planear el ámbito de las aplicaciones COM+ es una tarea de diseño importante que debería tener en cuenta en un momento anterior. Los sistemas distribuidos que están pensados para ejecutarse con COM+ deben diseñarse para su implementación con la menor cantidad de configuración individual y para usar cada proceso de forma más eficaz. También se pueden usar técnicas que le permitirán obtener un rendimiento óptimo al implementar una aplicación COM+. (Para obtener más información, consulte [implementación de una comunicación más rápida](deploying-for-faster-communication.md)).

Cuando se ve con la herramienta administrativa Servicios de componentes, cada aplicación COM+ aparece como una carpeta en la que se agrupan lógicamente los conjuntos de componentes. Aunque puede desplazar componentes individuales entre carpetas de **componentes** de aplicaciones com+ (es decir, de una aplicación a otra), varios servicios establecidos en el nivel de aplicación com+, como la seguridad, pueden ser diferentes. Esta configuración del servicio puede afectar a la portabilidad.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Una aplicación de servidor COM+ define un límite de proceso

Al crear una nueva aplicación de servidor COM+, realmente está definiendo un nuevo límite de proceso. (Observe la excepción para las aplicaciones de biblioteca que se explican a continuación). Este proceso se convierte en la instancia de la aplicación de control de los componentes contenidos en la aplicación COM+. Todos estos componentes se ejecutan en proceso en una nueva instancia del programa ejecutable COM+ cada vez que un programa llama a una aplicación COM+ por primera vez. Esto significa que todos los componentes de una determinada carpeta de **componentes** de la aplicación com+ se ejecutan en un único espacio de proceso que actúa como servidor DCOM. Dentro de la aplicación COM+, COM+ administra la memoria, la coordinación con la Coordinador de transacciones distribuidas (DTC), la activación de la instancia del componente Just-in-Time, la detección y recuperación de bloqueos y la seguridad basada en roles.

## <a name="calling-across-com-application-boundaries"></a>Llamar a través de los límites de la aplicación COM+

Dado que cada aplicación COM+ se implementa normalmente como un ejecutable independiente, el efecto de dividir una aplicación distribuida en varias aplicaciones COM+ presenta llamadas COM fuera de proceso cuando los componentes de una aplicación COM+ llaman a los componentes de otra aplicación COM+. Esto introduce una degradación del rendimiento debido a la carga adicional de calcular las referencias de los parámetros COM entre los procesos.

> [!Note]  
> No hay nada inherentemente incurrido al incurrir en esta penalización de rendimiento. solo tiene que tener en cuenta que se va a producir. En función del tiempo de respuesta requerido, el número de usuarios que solicitarán simultáneamente los servicios empresariales y la carga de inicio agregada que cada componente agrega a cada aplicación COM+, es posible que el impacto de rendimiento atribuible a las llamadas entre aplicaciones sea aceptable.

 

Una posibilidad de eliminar la reducción del rendimiento de la llamada a través de los límites de la aplicación COM+ es marcar una aplicación COM+ determinada como aplicación de biblioteca. Una aplicación de biblioteca COM+ se ejecuta en el proceso del cliente que la crea. Por supuesto, ningún aumento de rendimiento tiene un costo de cero. En este caso, el equilibrio implica las limitaciones de las aplicaciones de biblioteca COM+. Aunque una aplicación de biblioteca puede utilizar la seguridad basada en roles, no admite componentes en cola ni acceso remoto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementación para una comunicación más rápida](deploying-for-faster-communication.md)
</dt> <dt>

[Diseño para disponibilidad](designing-for-availability.md)
</dt> <dt>

[Diseño para la escalabilidad](designing-for-scalability.md)
</dt> <dt>

[Diseñar para la seguridad](designing-for-security.md)
</dt> </dl>

 

 



