---
description: COM+ 1.5 presenta la capacidad de usar servicios COM+ sin componentes.
ms.assetid: da93d164-234a-4d1e-b82c-f3f904bb8cb6
title: Conceptos de servicios COM+ sin componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0491b4aac66db9cd8fcbe507f5b4e755b99e0b20c5466b52b3ddc4653604e92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917053"
---
# <a name="com-services-without-components-concepts"></a>Conceptos de servicios COM+ sin componentes

COM+ 1.5 presenta la capacidad de usar servicios COM+ sin componentes. Esto reduce significativamente los costos de rendimiento al usar servicios COM+ desde un entorno que no usa componentes y también elimina la complejidad de usar estos servicios. A partir de IIS 6.0, IIS y ASP aprovechan el uso de servicios COM+ sin componentes.

Los servicios COM+ se diseñaron originalmente para usarse con componentes COM+. Sin embargo, algunos entornos de programación no están basados en componentes y, por tanto, requieren una sobrecarga considerable para usar los servicios COM+. Por ejemplo, antes del lanzamiento de COM+ 1.5, IIS tenía que crear objetos shim únicamente para poder usar servicios de transacciones COM+ en páginas ASP. Los costos de rendimiento que provienen de la creación de esos objetos incluyen el almacenamiento de los datos de configuración en la metabase de IIS y la base de datos de registro de COM+ (RegDB), así como la comunicación adicional entre la metabase de IIS y la regDB com+ necesaria para administrar eficazmente los datos de configuración.

Si IIS necesita usar un segundo servicio COM+, como la sincronización, tenía que crear un objeto de corrección de compatibilidad (shim) completamente diferente para hacerlo. Para usar las transacciones COM+ y la sincronización, se necesita un tercer tipo de objeto shim. La complejidad de este enfoque se escala como O(n2), lo que dificulta enormemente la implementación de nuevos servicios.

Con la introducción de servicios COM+ sin componentes, los servicios necesarios se configuran a través de un objeto del que se crea una instancia desde la clase . La [**clase CServiceConfig**](cserviceconfig.md) implementa las interfaces necesarias para configurar los distintos servicios a la vez que proporciona la flexibilidad para admitir varios servicios al mismo tiempo y la capacidad de admitir nuevos servicios en el futuro.

Los servicios configurados se pueden usar a través de dos mecanismos diferentes: se pueden usar a través de la función [**CoCreateActivity,**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) que aplica los servicios a todo el trabajo enviado a través de la actividad creada por la función y también se pueden usar insertando el trabajo que usa los servicios entre las llamadas a las funciones [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) y [**CoLeaveServiceDomain.**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) Ninguna de estas funciones requiere la creación de nuevos componentes para poder usar los servicios COM+. solo se [**necesita el objeto CServiceConfig.**](cserviceconfig.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas servicios COM+ sin componentes](com--services-without-components-tasks.md)
</dt> </dl>

 

 



