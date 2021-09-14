---
description: El reciclaje de aplicaciones puede aumentar significativamente la estabilidad general de las aplicaciones COM+, ya que ofrece una solución rápida para problemas conocidos y ayuda a protegerse frente a problemas inesperados.
ms.assetid: bf98318b-4d87-44cc-85a1-68faf5547e06
title: Conceptos de reciclaje de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab37376ff3bc6d03f454f63822641ed69fad0b47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072999"
---
# <a name="com-application-recycling-concepts"></a>Conceptos de reciclaje de aplicaciones COM+

El reciclaje de aplicaciones puede aumentar significativamente la estabilidad general de las aplicaciones COM+, ya que ofrece una solución rápida para problemas conocidos y ayuda a protegerse frente a problemas inesperados. Por ejemplo, el rendimiento de la aplicación puede disminuir con el tiempo debido a problemas como pérdidas de memoria, uso de recursos nocalables y error de proceso. COM+ proporciona reciclaje de aplicaciones como solución a estos problemas. Puede usar el reciclaje de aplicaciones para apagar automáticamente un proceso y reiniciarlo, reiniciando así un proceso con errores y reasignando la memoria que usa.

El reciclaje de aplicaciones funciona mediante la creación de un duplicado del proceso dllhost asociado a una aplicación. Este proceso dllhost duplicado da servicio a todas las solicitudes de objeto futuras, lo que deja el dllhost antiguo para terminar de atender las solicitudes de objeto restantes. El proceso dllhost antiguo se cierra cuando detecta la liberación de todas las referencias externas a los objetos del proceso o cuando se alcanza el valor de tiempo de espera de expiración. Mediante este comportamiento, el reciclaje de aplicaciones garantiza que una aplicación cliente no experimente una interrupción del servicio.

> [!Note]  
> No se puede reciclar una aplicación COM+ que se haya configurado para ejecutarse como Windows servicio. Además, las aplicaciones de biblioteca tienen las propiedades de reciclaje y agrupación de su proceso de host.

 

Puede configurar el reciclaje de aplicaciones de forma administrativa, mediante la herramienta administrativa Servicios de componentes o mediante programación, a través del SDK administrativo de COM+. Puede reciclar procesos en función de varios criterios, determinados por las siguientes propiedades de un objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) en la [**colección Applications:**](applications.md)

-   **RecycleLifetimeLimit.** El número máximo de minutos que un proceso puede ejecutarse antes de reciclarse. El intervalo válido es de 0 a 30 240 minutos (21 días). El número predeterminado de minutos es 0, lo que indica que el proceso no reciclará al alcanzar un límite de duración.
-   **RecycleMemoryLimit.** Cantidad máxima de uso de memoria de proceso (en kilobytes) antes de reciclar el proceso. Si el uso de memoria del proceso supera el número especificado durante más de un minuto, el proceso se recicla. El intervalo válido es de 0 a 1.048.576 KB. La cantidad predeterminada de uso de memoria es de 0 KB, lo que indica que el proceso no reciclará al alcanzar un límite de memoria.
-   **RecycleCallLimit.** Número máximo de llamadas que los objetos de aplicación pueden aceptar antes de reciclar el proceso. El intervalo válido es de 0 a 1.048.576 llamadas. El número predeterminado de llamadas es 0, lo que indica que el proceso no reciclará al alcanzar un límite de llamadas.
-   **RecycleActivationLimit.** Número máximo de activaciones de objetos de aplicación que se aceptan antes de reciclar el proceso. El intervalo válido es de 0 a 1.048.576 activaciones. El número predeterminado de activaciones es 0, lo que indica que el proceso no reciclará al alcanzar un límite de activación.

Además, la propiedad RecycleExpirationTimeout del objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) se usa para forzar el cierre de un proceso reciclado. Indica el número de minutos que hay que esperar a que se liberen todas las referencias externas a los objetos del proceso reciclado antes de cerrar forzadamente el proceso. El intervalo válido es de 1 a 1440 minutos (24 horas) y el tiempo de espera de expiración predeterminado es de 15 minutos. Este valor sólo se usa cuando ya se ha determinado que un proceso se reciclará en función de otros criterios.

Puede seleccionar más de un criterio para reciclar una aplicación. COM+ recicla la aplicación después de que se cumpla el primero de los criterios. Puede establecer el valor de tiempo de espera de expiración para determinar cuánto tiempo puede dedicar un antiguo proceso de Dllhost a completar las solicitudes de servicio restantes antes de cerrarse forzadamente.

La [**colección ApplicationInstances**](applicationinstances.md) proporciona la propiedad HasRecycled, que proporciona una manera de determinar si la aplicación se ha reciclado alguna vez.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de reciclaje de aplicaciones COM+](com--application-recycling-tasks.md)
</dt> <dt>

[**RecycleSurrogate**](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)
</dt> </dl>

 

 



