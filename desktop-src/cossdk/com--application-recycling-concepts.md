---
description: El reciclaje de aplicaciones puede aumentar significativamente la estabilidad general de las aplicaciones COM+ al ofrecer una corrección rápida para los problemas conocidos y ayudar a protegerse frente a las inesperadas.
ms.assetid: bf98318b-4d87-44cc-85a1-68faf5547e06
title: Conceptos de reciclaje de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab37376ff3bc6d03f454f63822641ed69fad0b47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423287"
---
# <a name="com-application-recycling-concepts"></a>Conceptos de reciclaje de aplicaciones COM+

El reciclaje de aplicaciones puede aumentar significativamente la estabilidad general de las aplicaciones COM+ al ofrecer una corrección rápida para los problemas conocidos y ayudar a protegerse frente a las inesperadas. Por ejemplo, el rendimiento de la aplicación puede reducirse con el tiempo debido a problemas como pérdidas de memoria, uso de recursos no escalables y errores de proceso. COM+ proporciona reciclaje de aplicaciones como una solución para estos problemas. Puede usar el reciclaje de aplicaciones para apagar automáticamente un proceso y reiniciarlo, con lo que se reinicializa un proceso con errores y se reasigna la memoria que usa.

El reciclaje de aplicaciones funciona creando un duplicado del proceso Dllhost asociado a una aplicación. Este proceso Dllhost duplicado atiende todas las solicitudes de objeto futuras, lo que deja que el Dllhost antiguo termine de atender las solicitudes de objeto restantes. El proceso Dllhost anterior se cierra cuando detecta el lanzamiento de todas las referencias externas a los objetos del proceso o cuando se alcanza el valor de tiempo de espera de expiración. A través de este comportamiento, el reciclaje de aplicaciones garantiza que una aplicación cliente no experimenta una interrupción del servicio.

> [!Note]  
> No se puede reciclar una aplicación COM+ que se ha configurado para ejecutarse como un servicio de Windows. Además, las aplicaciones de biblioteca tienen las propiedades de reciclaje y agrupación de su proceso de host.

 

Puede configurar el reciclaje de aplicaciones administrativamente, mediante la herramienta administrativa Servicios de componentes o mediante programación, a través del SDK administrativo de COM+. Puede reciclar los procesos en función de varios criterios, determinados por las siguientes propiedades de un objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) en la colección de [**aplicaciones**](applications.md) :

-   **RecycleLifetimeLimit.** Número máximo de minutos que puede ejecutarse un proceso antes de que se recicle. El intervalo válido es de 0 a 30.240 minutos (21 días). El número predeterminado de minutos es 0, lo que indica que el proceso no se reciclará para alcanzar un límite de duración.
-   **RecycleMemoryLimit.** Cantidad máxima de uso de memoria de proceso (en kilobytes) antes de reciclar el proceso. Si el uso de memoria del proceso supera el número especificado durante más de un minuto, el proceso se recicla. El intervalo válido es de 0 a 1.048.576 KB. El uso de memoria predeterminado es 0 KB, lo que indica que el proceso no se reciclará para alcanzar un límite de memoria.
-   **RecycleCallLimit.** Número máximo de llamadas que los objetos de aplicación pueden aceptar antes de reciclar el proceso. El intervalo válido es de 0 a 1.048.576 llamadas. El número predeterminado de llamadas es 0, lo que indica que el proceso no se reciclará al alcanzar un límite de llamadas.
-   **RecycleActivationLimit.** Número máximo de activaciones de objetos de aplicación que se aceptan antes de reciclar el proceso. El intervalo válido es de 0 a 1.048.576 activaciones. El número predeterminado de activaciones es 0, lo que indica que el proceso no se reciclará para alcanzar un límite de activación.

Además, la propiedad RecycleExpirationTimeout del objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) se usa para forzar el cierre de un proceso reciclado. Indica el número de minutos que se esperará a que se liberen todas las referencias externas a los objetos del proceso reciclado antes de que se apague el proceso. El intervalo válido es de 1 a 1440 minutos (24 horas) y el tiempo de espera de expiración predeterminado es 15 minutos. Este valor sólo se usa cuando ya se ha determinado que un proceso se reciclará en función de otros criterios.

Puede seleccionar más de un criterio para reciclar una aplicación. COM+ recicla la aplicación después de que se cumple el primer conjunto de criterios. Puede establecer el valor de tiempo de espera de expiración para determinar cuánto tiempo un proceso Dllhost antiguo puede gastar en completar las solicitudes de servicio restantes antes de que se apague la fuerza.

La colección [**ApplicationInstances**](applicationinstances.md) proporciona la propiedad HasRecycled, que proporciona una manera de determinar si la aplicación se ha reciclado alguna vez.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de reciclaje de aplicaciones COM+](com--application-recycling-tasks.md)
</dt> <dt>

[**RecycleSurrogate**](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)
</dt> </dl>

 

 



