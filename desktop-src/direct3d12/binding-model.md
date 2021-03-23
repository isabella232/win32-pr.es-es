---
title: Diferencias en el modelo de enlace de Direct3D 11
description: Una de las decisiones de diseño principales detrás del enlace de DirectX12 es separarlo de otras tareas de administración. Esto pone algunos requisitos en la aplicación para administrar ciertos peligros potenciales.
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2785da6497fd4e775d9f88847928e7c4c08e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103845"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a>Diferencias en el modelo de enlace de Direct3D 11

Una de las decisiones de diseño principales detrás del enlace de DirectX12 es separarlo de otras tareas de administración. Esto pone algunos requisitos en la aplicación para administrar ciertos peligros potenciales.

La principal ventaja del modelo de enlace D3D12 es que permite que las aplicaciones cambien los enlaces de textura con frecuencia, sin un costo de rendimiento de CPU elevado. Otras ventajas son que los sombreadores tienen acceso a un gran número de recursos, los sombreadores no necesitan conocer de antemano cuántos recursos se enlazarán y que se puede usar un modelo de enlace de recursos unificado independientemente del hardware o el flujo de contenido de aplicaciones.

Para mejorar el rendimiento, el modelo de enlace no requiere que el sistema realice un seguimiento de los enlaces que una aplicación ha solicitado que use la GPU y existe una integración limpia entre las listas de comandos de enlace y multiproceso.

En las secciones siguientes se enumeran algunos de los cambios en el modelo de enlace de recursos desde D3D11.

-   [Administración de la residencia de memoria separada del enlace](#memory-residency-management-separated-from-binding)
-   [Administración de la duración de los objetos separados del enlace](#object-lifetime-management-separated-from-binding)
-   [Seguimiento de estado de recursos de controlador separado del enlace](#driver-resource-state-tracking-separated-from-binding)
-   [Sincronización de memoria asignada de GPU de CPU separada del enlace](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [Temas relacionados](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a>Administración de la residencia de memoria separada del enlace

Las aplicaciones tienen un control explícito sobre qué superficies deben estar disponibles para que la GPU pueda usarlos directamente (denominados "residentes"). Por el contrario, pueden aplicar otros Estados en recursos, como dejarlos de forma explícita o dejar que el sistema operativo elija determinadas clases de aplicaciones que requieren una superficie de memoria mínima. Lo importante aquí es que la administración de la aplicación de lo que reside está totalmente desacoplada de la forma en que proporciona acceso a los recursos a los sombreadores.

La desasociación de la administración de la residencia del mecanismo para dar acceso a los sombreadores reduce el costo del sistema o del hardware para la representación, ya que el sistema operativo no tiene que inspeccionar constantemente el estado de enlace local para saber qué debe hacer residente. Además, ya no es necesario que los sombreadores sepan a qué superficies exactas deben hacer referencia, siempre que el conjunto completo de recursos posiblemente accesibles se haya puesto a fin de antemano.

## <a name="object-lifetime-management-separated-from-binding"></a>Administración de la duración de los objetos separados del enlace

A diferencia de las API anteriores, el sistema ya no realiza un seguimiento de los enlaces de recursos a la canalización. Esto se usa para permitir que el sistema mantenga activos los recursos que la aplicación ha liberado porque todavía se hace referencia a ellos mediante el trabajo de GPU pendiente.

Antes de liberar cualquier recurso, como una textura, las aplicaciones deben asegurarse de que la GPU ha completado la referencia. Esto significa que antes de que una aplicación pueda liberar de forma segura un recurso, la GPU debe haber completado la ejecución de la lista de comandos que hace referencia al recurso.

## <a name="driver-resource-state-tracking-separated-from-binding"></a>Seguimiento de estado de recursos de controlador separado del enlace

El sistema ya no inspecciona los enlaces de recursos para comprender cuándo se han producido transiciones de recursos que requieren un controlador o trabajo de GPU adicional. Un ejemplo común para muchas GPU y controladores es tener que saber cuándo una superficie realiza una transición de usarse como vista de destino de representación (RTV) al sombreador Vista de recursos (SRV). Las propias aplicaciones deben identificar ahora Cuándo se están produciendo las transiciones de recursos que el sistema puede interesar a través de API dedicadas.

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a>Sincronización de memoria asignada de GPU de CPU separada del enlace

El sistema ya no inspecciona los enlaces de recursos para saber si es necesario retrasar la representación porque depende de un recurso que se ha asignado para el acceso a la CPU, pero que aún no se ha desasignado. Las aplicaciones ahora tienen la responsabilidad de sincronizar los accesos de memoria de la GPU y la CPU. Para ayudar con esto, el sistema proporciona mecanismos para que la aplicación solicite la suspensión de un subproceso de CPU hasta que el trabajo se complete. El sondeo también podría realizarse, pero puede ser menos eficaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

 




