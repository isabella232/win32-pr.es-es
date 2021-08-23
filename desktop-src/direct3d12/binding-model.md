---
title: Diferencias en el modelo de enlace de Direct3D 11
description: Una de las principales decisiones de diseño detrás del enlace de DirectX12 es separarlo de otras tareas de administración. Esto coloca algunos requisitos en la aplicación para administrar determinados riesgos potenciales.
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a625bd1b79766990658feba9bf18ddf7f46c3788ca20aea1de0b4ab80ae0a71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632536"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a>Diferencias en el modelo de enlace de Direct3D 11

Una de las principales decisiones de diseño detrás del enlace de DirectX12 es separarlo de otras tareas de administración. Esto coloca algunos requisitos en la aplicación para administrar determinados riesgos potenciales.

La principal ventaja del modelo de enlace D3D12 es que permite a las aplicaciones cambiar los enlaces de textura con frecuencia, sin un gran costo de rendimiento de la CPU. Otras ventajas son que los sombreadores tienen acceso a un gran número de recursos, los sombreadores no necesitan saber de antemano cuántos recursos se enlazarán y que se puede usar un modelo de enlace de recursos unificado independientemente del hardware o el flujo de contenido de las aplicaciones.

Para mejorar el rendimiento, el modelo de enlace no requiere que el sistema realice un seguimiento de los enlaces que una aplicación ha solicitado que use la GPU, y hay una integración limpia entre el enlace y las listas de comandos multiproceso.

En las secciones siguientes se enumera algunos de los cambios realizados en el modelo de enlace de recursos desde D3D11.

-   [Administración de residencia de memoria separada del enlace](#memory-residency-management-separated-from-binding)
-   [Administración de la duración de objetos separada del enlace](#object-lifetime-management-separated-from-binding)
-   [Seguimiento del estado de los recursos de controlador separados del enlace](#driver-resource-state-tracking-separated-from-binding)
-   [Sincronización de memoria asignada por GPU de CPU separada del enlace](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [Temas relacionados](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a>Administración de residencia de memoria separada del enlace

Las aplicaciones tienen un control explícito sobre qué superficies deben estar disponibles para que la GPU la use directamente (lo que se denomina "residentes"). Por el contrario, pueden aplicar otros estados en recursos como hacer que no residen explícitamente o dejar que el sistema operativo elija para determinadas clases de aplicaciones que requieren una superficie de memoria mínima. Lo importante aquí es que la administración de la aplicación de lo que es residentes está completamente desacoplada de la forma en que proporciona acceso a los recursos a los sombreadores.

El desacobamiento de la administración de residencias del mecanismo para dar a los sombreadores acceso a los recursos reduce el costo del sistema o hardware para la representación, ya que el sistema operativo no tiene que inspeccionar constantemente el estado de enlace local para saber qué hacer para que resida. Además, los sombreadores ya no tienen que saber a qué superficies exactas es necesario hacer referencia, siempre y cuando todo el conjunto de recursos posiblemente accesibles se haya convertido en residentes con antelación.

## <a name="object-lifetime-management-separated-from-binding"></a>Administración de la duración de objetos separada del enlace

A diferencia de las API anteriores, el sistema ya no realiza el seguimiento de los enlaces de recursos a la canalización. Esto se usa para permitir que el sistema mantenga activo los recursos que la aplicación ha publicado porque todavía se hace referencia a ellos mediante un trabajo de GPU pendiente.

Antes de liberar cualquier recurso, como una textura, las aplicaciones ahora deben asegurarse de que la GPU ha terminado de hacer referencia a él. Esto significa que antes de que una aplicación pueda liberar de forma segura un recurso, la GPU debe haber completado la ejecución de la lista de comandos que hace referencia al recurso.

## <a name="driver-resource-state-tracking-separated-from-binding"></a>Seguimiento del estado de los recursos de controlador separados del enlace

El sistema ya no inspecciona los enlaces de recursos para comprender cuándo se han producido las transiciones de recursos que requieren trabajo adicional de controlador o GPU. Un ejemplo común para muchas GPU y controladores es tener que saber cuándo una superficie pasa de usarse como vista de destino de representación (RTV) a sombreador Vista de recursos (SRV). Ahora, las propias aplicaciones deben identificar cuándo se están produciendo las transiciones de recursos que puedan interesar al sistema a través de API dedicadas.

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a>Sincronización de memoria asignada por GPU de CPU separada del enlace

El sistema ya no inspecciona los enlaces de recursos para saber si es necesario retrasar la representación porque depende de un recurso que se ha asignado para el acceso a la CPU, pero que aún no se ha desasignado. Las aplicaciones ahora tienen la responsabilidad de sincronizar los accesos a memoria de CPU y GPU. Para ayudar con esto, el sistema proporciona mecanismos para que la aplicación solicite que un subproceso de CPU esté en modo de inmoción hasta que se complete el trabajo. También se puede realizar el sondeo, pero puede ser menos eficaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

 




