---
description: COM+ 1,5 incorpora la capacidad de usar servicios COM+ sin componentes.
ms.assetid: da93d164-234a-4d1e-b82c-f3f904bb8cb6
title: Conceptos de servicios COM+ sin componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d692657d33143b9437a9c8134260a8c32431cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907443"
---
# <a name="com-services-without-components-concepts"></a>Conceptos de servicios COM+ sin componentes

COM+ 1,5 incorpora la capacidad de usar servicios COM+ sin componentes. Esto reduce significativamente los costos de rendimiento cuando se usan los servicios COM+ desde un entorno que no usa componentes, y también elimina la complejidad del uso de estos servicios. A partir de IIS 6,0, IIS y ASP aprovechan el uso de servicios COM+ sin componentes.

Los servicios COM+ se diseñaron originalmente para usarse con componentes COM+. Sin embargo, algunos entornos de programación no están basados en componentes y, por lo tanto, requieren una sobrecarga importante para usar los servicios COM+. Por ejemplo, antes de la versión de COM+ 1,5, IIS tenía que crear objetos de correcciones de compatibilidad (shim) para poder usar los servicios de transacciones COM+ en páginas ASP. Los costos de rendimiento que provienen de la creación de esos objetos incluyen el almacenamiento de los datos de configuración en la metabase de IIS y en la base de datos de registro de COM+ (RegDB), así como la comunicación adicional entre la metabase de IIS y el RegDB de COM+ necesario para administrar de forma eficaz los datos de configuración.

Si IIS necesitaba usar un segundo servicio COM+, como la sincronización, tenía que crear un objeto Shim completamente diferente para hacerlo. Para usar las transacciones y la sincronización de COM+, sería necesario un tercer tipo de objeto de correcciones de compatibilidad (shim). La complejidad de este enfoque se escala como O (N2), lo que hace que la implementación de nuevos servicios sea muy difícil.

Con la introducción de los servicios COM+ sin componentes, los servicios que se necesitan se configuran mediante un objeto del que se crea una instancia de la clase. La clase [**CServiceConfig**](cserviceconfig.md) implementa las interfaces necesarias para configurar los distintos servicios, a la vez que proporciona la flexibilidad necesaria para admitir varios servicios al mismo tiempo y la capacidad de admitir nuevos servicios en el futuro.

Los servicios configurados se pueden usar a continuación a través de dos mecanismos diferentes: se pueden usar a través de la función [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) , que aplica los servicios a todo el trabajo enviado a través de la actividad creada por la función, y también se pueden usar mediante la incrustación del trabajo que usa los servicios entre las llamadas a las funciones [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) y [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) . Ninguna de estas funciones requiere la creación de los nuevos componentes para poder usar los servicios COM+. solo se necesita el objeto [**CServiceConfig**](cserviceconfig.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios COM+ sin tareas de componentes](com--services-without-components-tasks.md)
</dt> </dl>

 

 



