---
title: Estrategias de administración de memoria
description: Un administrador de memoria para Direct3D 12 podría resultar muy complicado rápidamente con los distintos niveles de compatibilidad, para los adaptadores de UMA o discretos (no UMA), y con una gran variedad de diferencias de arquitectura entre los adaptadores de GPU. La estrategia recomendada para la administración de memoria de Direct3D 12, que se describe en esta sección, es \ 0034; clasificación, presupuesto y flujo \ 0034;.
ms.assetid: BC9894F7-D496-46F2-A5C3-C7CA31FD4BA8
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dad04055a5acdeeeaead3a56f0bd04e64aa90fe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549125"
---
# <a name="memory-management-strategies"></a>Estrategias de administración de memoria

Un administrador de memoria para Direct3D 12 podría resultar muy complicado rápidamente con los distintos niveles de compatibilidad, para los adaptadores de UMA o discretos (no UMA), y con una gran variedad de diferencias de arquitectura entre los adaptadores de GPU.

La estrategia recomendada para la administración de memoria de Direct3D 12, que se describe en esta sección, es "clasificación, presupuesto y flujo".

-   [Tipos de recursos](#resource-types)
-   [Presupuesto de memoria](#memory-budget)
-   [Estrategia de clasificación](#classification-strategy)
-   [Temas relacionados](#related-topics)

## <a name="resource-types"></a>Tipos de recursos

El concepto básico de un "recurso confirmado" (la creación de espacios de direcciones virtuales y físicos inicializados en la memoria física administrada) ha sido el mismo que el de Direct3D 9, aunque el direccionamiento virtual (VA) y el direccionamiento físico se pueden desplazar en Direct3D 12 para permitir que la aplicación administre cuidadosamente la memoria física.

Además de los recursos confirmados, la construcción del montón de Direct3D 12 habilita otros dos tipos de recursos: "colocated" y "Reserved". En Direct3D 11, un recurso "reservado" se conocía como "recurso en mosaico".

Los recursos reservados se diferencian de los recursos colocados en que los recursos reservados tienen su propio espacio de direcciones virtuales de GPU único. Esto permite una gran asignación de espacio de VA por adelantado y, a continuación, habilita la asignación de páginas VA a determinadas secciones del montón más adelante, y la aplicación vuelve a configurar la organización sobre la marcha. El espacio VA es contiguo y se puede asignar de forma dispersa a.

El recurso reservado se puede hacer para hacer referencia a las regiones del montón con llamadas API como [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) y se pueden hacer residentes en la aplicación actualizando las tablas de página sobre la marcha. Cuando un intervalo de VA se asigna a un valor NULL o un montón no residente, esa parte del recurso se considera no residente. Cuando se asigna un intervalo de VA a un montón residente, esa parte del recurso se considera residente. Los montones están residentes durante la creación.

Los recursos colocados son un diseño mucho más sencillo, que es simplemente un puntero a una región determinada de un montón (por ejemplo, una región de 1 MB para una textura en un montón de 5 MB). Las barreras de alias permiten el uso de recursos colocados superpuestos (consulte [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) y [**ResourceBarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)).

Los recursos reservados no están disponibles en todo el hardware de Direct3D 12 y los recursos colocados son una reserva razonable, aunque los recursos colocados deben ser contiguos y no pueden ser residentes parcialmente.

## <a name="memory-budget"></a>Presupuesto de memoria

En Direct3D 12, cuando se asigna un montón, se crea el aspecto de la memoria física de un recurso confirmado. La opción de segmento de memoria más explícita está disponible en Direct3D 12 (elegir entre el vídeo y la memoria del sistema). Los adaptadores de UMA solo tienen un único segmento de memoria, la memoria del sistema.

Las GPU no admiten errores de página, por lo que los desarrolladores deben ser conscientes de que no se confirman, especialmente en los sistemas con solo 1 GB de memoria del sistema. Si una aplicación realiza una confirmación, el sistema operativo usa la programación general de los procesos por su demanda en la memoria física. Scheduler inmovilizará los procesos en primer plano y, en esencia, paginará algunas de ellos, con el fin de paginar en un proceso en segundo plano que quiere ejecutar. La memoria física disponible puede variar considerablemente en función de lo que el usuario esté realizando en segundo plano (como ejecutar un explorador o ver un vídeo).

La API para el presupuesto de memoria es [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo). En el caso de los adaptadores discretos, "local" es la memoria de vídeo, "no local", es la memoria del sistema. En el caso de los adaptadores de UMA que no son locales, siempre es cero. Una pregunta de diseño es si el motor va a administrar tanto presupuestos como solo el presupuesto local. Administrar solo el presupuesto local es más sencillo, pero tiene algunas salvedades; por ejemplo, supongamos que hay un presupuesto local máximo de 1 GB y, a continuación, todos los montones procederán de ese 1 GB en un sistema UMA y no habrá desbordamiento en la memoria del sistema (evidentemente, como no hay ninguno).

Dado que la memoria administrada de Direct3D 11 para las aplicaciones, los recursos no utilizados se paginarían en la página.

Elija las dimensiones de recursos más adecuadas. Considere si el tamaño de un recurso es adecuado para la situación en la que se ejecuta realmente la aplicación. Algunos usuarios pueden ejecutar la aplicación en una ventana de o con una resolución de pantalla de 800x600.

## <a name="classification-strategy"></a>Estrategia de clasificación

Con el fin de administrar los recursos de forma eficaz en escenarios enlazados a memoria, considere la posibilidad de clasificar los recursos en lo siguiente:



| clasificación      | Ejemplos                                                                                         | Objetos y características de API                                                                                           | Notas de administración                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crítico            | Interfaz de usuario del juego                                                                                          | Asignador de comandos, colas de comandos, montones de consulta, recursos y montones de recursos.                                      | Estos elementos deben ir en memoria no paginable o siempre confirmada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Escalado/opcional    | Modelos y texturas específicos de nivel, cadenas de intercambio, cuadros de cielo, modelos de caracteres del jugador de primera persona | Recursos y montones. Los recursos confirmados, pero también los recursos colocados y reservados también podrían funcionar correctamente.          | Integre la presupuestación de la residencia de memoria en los algoritmos de representación. Elija el nivel de detalle disponible adecuado y vuelva a evaluarlo menos de una vez por fotograma. Las técnicas incluyen el uso de recursos de tamaño variable y el escalado de la cadena de intercambio.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| Recursos que se han vuelto a usar   | Búferes de sombra, recursos de representación aplazados, recursos de procesamiento posterior, memorias caché de datos de iluminación    | Recursos y montones. La superposición de recursos colocados en montones y barreras de alias.                                  | Reutilizar recursos grandes o regiones del montón dentro de un marco para reducir los requisitos de todo el marco. Use la técnica de reutilización de memoria dentro del marco. En Direct3D 11, las aplicaciones solo podían volver a usar recursos con el mismo tipo y dimensiones suficientemente grandes. Los montones de Direct3D 12 permiten la superposición de recursos para una reutilización mucho más sencilla y mayor.<br/>                                                                                                                                                                                                                              |
| Recursos de streaming | Terreno, texturas y geometría de mundo abierto                                                        | Recursos y montones. Creación de subprocesos libres, subprocesos de CPU en segundo plano y listas y colas de comandos de copia en segundo plano. | La residencia parcial, que suele basarse en la visibilidad (con el frustum de vista o evaluación basada en la distancia) y volver a evaluar la residencia necesita cada fotograma.<br/> La técnica de usar una administración de residencia parcial por icono y la reutilización entre fotogramas está disponible cuando el adaptador de GPU admite recursos reservados en montones.<br/> Mediante la técnica de uso de la reutilización de memoria entre fotogramas, se puede llevar a cabo la residencia parcial de Subrecursos, pero es menos óptima. Los recursos colocados con montones deben permitir un reciclaje más rápido, pero los recursos confirmados se pueden usar como reserva.<br/> |



 

Cuanto más aplicaciones Gravitate a los recursos de streaming para la mayor parte del trabajo, más aprovecharán los recursos colocados y reservados, lo que aumentará la reutilización de la memoria entre estas cuatro clasificaciones. Cuanto mayor sea el flujo de aplicaciones, más se presupuestan y priorizan el ancho de banda.

Normalmente, con los motores gráficos de Direct3D 12 es necesario respetar un presupuesto más diverso y dinámico, y hacer que sea más estricto que en el pasado. Las mejores aplicaciones buscarán las cuatro categorías en el presupuesto dado al proceso, escalando la reproducción de juego desde la aplicación móvil en segundo plano a los presupuestos discretos de pantalla completa. Pero es probable que muchas aplicaciones produzcan problemas al empezar con demasiados tipos de categoría críticos de recursos. Los recursos habilitados para Direct3D 11 se crean de forma anónima y ocupan el estado crítico sin afectar al rendimiento. Sin embargo, para Direct3D 12, los desarrolladores deben buscar diligentemente los recursos creados aleatoriamente a lo largo de su motor y middleware y volver a asignarlos a una de las otras categorías.

Otras áreas problemáticas son componentes de middleware, controles de usuario y streaming dentro del marco. Es posible que los componentes de middleware no se expongan a un presupuesto, ni que funcionen estrechamente juntos. Es posible que los componentes de middleware expongan características como técnicas de representación; y la aplicación podría basarse en la exposición de la configuración del middleware y del motor. Los desarrolladores podrían confiar en Direct3D 11 para realizar la paginación y alcanzar la velocidad de fotogramas correcta. En algunos casos, es posible que las aplicaciones de Direct3D 11 hayan paginado el contenido de los recursos hacia y hacia fuera cada fotograma; y resultó en una velocidad de fotogramas aceptable para el usuario. La mayoría de los motores solo transmiten los datos de recursos como una actividad en segundo plano, donde no tiene una reserva estable para el streaming intra-Frame de alta prioridad. Pedir a los motores que implementen esto deteriorará algunas de las ventajas de sobrecarga de CPU que buscan al pasar a Direct3D 12. Los desarrolladores de motores pueden considerar el paso de sus fotogramas en fases para proporcionar más oportunidades para los recursos que se pueden volver a usar. y es probable que funcione con los proveedores de middleware para admitir los recursos y montones colocados para la reutilización de la memoria dentro del marco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
</dt> <dt>

[**CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)
</dt> <dt>

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Administración de memoria](memory-management.md)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

