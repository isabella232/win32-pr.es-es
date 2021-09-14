---
title: Estrategias de administración de la memoria
description: Un administrador de memoria para Direct3D 12 podría complicarse rápidamente con todos los distintos niveles de compatibilidad, para adaptadores UMA o discretos (no UMA) y con una gran variedad de diferencias de arquitectura entre los adaptadores de GPU. La estrategia recomendada para la administración de memoria de Direct3D 12, descrita en esta sección, es \ 0034;classify, budget and stream \ 0034;.
ms.assetid: BC9894F7-D496-46F2-A5C3-C7CA31FD4BA8
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dad04055a5acdeeeaead3a56f0bd04e64aa90fe0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072943"
---
# <a name="memory-management-strategies"></a>Estrategias de administración de la memoria

Un administrador de memoria para Direct3D 12 podría complicarse rápidamente con todos los distintos niveles de compatibilidad, para adaptadores UMA o discretos (no UMA) y con una gran variedad de diferencias de arquitectura entre los adaptadores de GPU.

La estrategia recomendada para la administración de memoria de Direct3D 12, descrita en esta sección, es "clasificar, presupuesto y flujo".

-   [Tipos de recursos](#resource-types)
-   [Presupuesto de memoria](#memory-budget)
-   [Estrategia de clasificación](#classification-strategy)
-   [Temas relacionados](#related-topics)

## <a name="resource-types"></a>Tipos de recursos

El concepto básico de un "recurso confirmado" (creación de espacios de direcciones virtuales y físicos inicializados en memoria física administrada) se ha producido desde Direct3D 9, aunque el direccionamiento virtual (VA) y el direccionamiento físico se pueden separar en Direct3D 12 para permitir que la aplicación administre cuidadosamente la memoria física.

Además de los recursos confirmados, la construcción del montón de Direct3D 12 permite otros dos tipos de recursos: "colocado" y "reservado". En Direct3D 11, un recurso "reservado" se conocía como "recurso en mosaico".

Los recursos reservados difieren de los recursos colocados en que los recursos reservados tienen su propio espacio de direcciones virtuales de GPU único. Esto permite una gran asignación de espacio de VA por adelantado y, a continuación, permite la asignación de páginas va a determinadas secciones del montón más adelante y la aplicación vuelve a configurar la organización sobre la marcha. El espacio va es contiguo y se puede asignar de forma dispersa.

El recurso reservado se puede hacer para hacer referencia a regiones del montón con llamadas API como [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) y la aplicación puede convertirla en residentes mediante la actualización de tablas de páginas sobre la marcha. Cuando un intervalo de VA se asigna a NULL o a un montón no residentes, esa parte del recurso se considera no residentes. Cuando un intervalo de VA se asigna a un montón de residentes, esa parte del recurso se considera residentes. Los montones residen en el momento de la creación.

Los recursos colocados son un diseño mucho más sencillo, ya que son simplemente un puntero a una determinada región de un montón (por ejemplo, una región de 1 Mb para una textura en un montón de 5 Mb). Las barreras de alias permiten el uso de recursos colocados superpuestos (consulte [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) y [**ResourceBarpong).**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Los recursos reservados no están disponibles en todo el hardware de Direct3D 12 y los recursos colocados son una reserva razonable, aunque los recursos colocados deben ser contiguos y no pueden ser parcialmente residentes.

## <a name="memory-budget"></a>Presupuesto de memoria

En Direct3D 12, al asignar un montón, está creando el aspecto de memoria física de un recurso confirmado. Hay una opción de segmento de memoria más explícita disponible en Direct3D 12 (elegir entre vídeo y memoria del sistema). Los adaptadores UMA solo tienen un único segmento de memoria, memoria del sistema.

Las GPU no admiten errores de página, por lo que los desarrolladores deben ser conscientes de que no se confirman en exceso, especialmente para los sistemas, por ejemplo, con solo 1 Gb de memoria del sistema. Si una aplicación realiza una confirmación en exceso, el sistema operativo usa una programación más general de los procesos por su demanda de memoria física. El programador inmovilizará los procesos en primer plano y, básicamente, paginará algunos de ellos, con el fin de paginar en un proceso en segundo plano que quiera ejecutarse. La memoria física disponible puede variar considerablemente en función de lo que haga el usuario en segundo plano (como ejecutar un explorador o ver un vídeo).

La API para el presupuesto de memoria [**es QueryVideoMemoryInfo.**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) Para los adaptadores discretos "local" es la memoria de vídeo, "no local" es la memoria del sistema. Para los adaptadores de UMA no locales siempre es cero. Una pregunta de diseño es si el motor administrará ambos presupuestos o solo el presupuesto local. Administrar solo el presupuesto local es más sencillo, pero tiene algunas advertencias. Por ejemplo, si hay un presupuesto local máximo de 1 Gb, todos los montones procederán de ese 1 Gb en un sistema UMA y no habrá ningún desbordamiento en la memoria del sistema (claramente, ya que no hay ninguno).

Puesto que la memoria administrada de Direct3D11 para las aplicaciones, los recursos no usados se paginarán básicamente.

Elija las dimensiones de recursos más adecuadas. Considere si el tamaño de un recurso es adecuado para la situación en la que se ejecuta realmente la aplicación. Algunos usuarios pueden ejecutar la aplicación en una ventana o con una resolución de pantalla de 800 x 600.

## <a name="classification-strategy"></a>Estrategia de clasificación

Para administrar los recursos de forma eficaz en escenarios enlazados a memoria, considere la posibilidad de clasificar los recursos en lo siguiente:



| clasificación      | Ejemplos                                                                                         | Objetos y características de API                                                                                           | Notas de administración                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crítico            | Interfaz de usuario del juego                                                                                          | Asignador de comandos, colas de comandos, montones de consultas, recursos y montones de recursos.                                      | Estos elementos deben ir en memoria no paginable o siempre confirmado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Escalado/Opcional    | Modelos y texturas específicos del nivel, cadenas de intercambio, cuadros de cielo, modelos de caracteres de jugador en primera persona | Recursos y montones. Los recursos confirmados, pero también los recursos reservados y colocados también pueden funcionar igual.          | Integre el presupuesto de residencia de memoria en los algoritmos de representación. Elija el nivel adecuado de detalle disponible y vuelva a evaluar menos de una vez por fotograma. Las técnicas incluyen el uso de recursos de tamaño variable y el escalado de la cadena de intercambio.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| Recursos usados de nuevo   | Búferes de sombra, recursos de representación diferida, recursos posteriores al procesamiento, memorias caché de datos de iluminación    | Recursos y montones. Recursos colocados superpuestos en montones y barreras de alias.                                  | Reutilizar recursos grandes o regiones de montón dentro de un marco para reducir los requisitos de todo el marco. Use la técnica de reutilización de memoria dentro de fotogramas. En Direct3D 11, las aplicaciones solo podían reutilizar recursos con el mismo tipo y dimensiones lo suficientemente grandes. Los montones de Direct3D 12 permiten la superposición de recursos para una reutilización mucho más sencilla y mayor.<br/>                                                                                                                                                                                                                              |
| Recursos de streaming | Terreno, texturas de mundo abierto y geometría                                                        | Recursos y montones. Creación de subprocesos libres, subprocesos de CPU en segundo plano y colas y listas de comandos de copia en segundo plano. | La residencia parcial, normalmente basada en la visibilidad (mediante la evaluación basada en la distancia o la vista) y la reevaluación de las necesidades de residencia en cada fotograma.<br/> La técnica de uso de una administración de residencia parcial por icono y la reutilización entre fotogramas está disponible cuando el adaptador de GPU admite recursos reservados dentro de montones.<br/> Mediante la técnica de uso de la nueva utilización de la memoria entre fotogramas, se puede lograr la residencia parcial de subrecursos, pero es menos óptima. Los recursos colocados con montones deben permitir un reciclaje más rápido, pero los recursos confirmados se pueden usar como reserva.<br/> |



 

Cuanto más aplicaciones se dedican a los recursos de streaming durante la mayor parte del trabajo, más aprovecharán los recursos reservados y colocados, lo que maximizará el uso de la memoria entre estas cuatro clasificaciones. Entre más aplicaciones se transmita, más presupuestan y priorizan el ancho de banda.

Normalmente, con los motores gráficos de Direct3D 12 es necesario respetar un presupuesto más diverso y dinámico, y hacerlo más estrictamente que en el pasado. Las mejores aplicaciones ubicarán las cuatro categorías en el presupuesto dado al proceso, escalando el juego de juego de aplicación móvil en segundo plano a presupuestos discretos a pantalla completa. Sin embargo, es probable que muchas aplicaciones se deba a que empiecen con demasiados tipos de categoría críticos de recursos. Direct3D 11 permitió que los recursos se crearan de forma anónima y ocuparan el estado crítico sin afectar al rendimiento. Sin embargo, para Direct3D 12, los desarrolladores deben buscar diligentemente los recursos creados aleatoriamente a lo largo de su motor y middleware y volver a asignarlos a una de las otras categorías.

Otras áreas problemáticas son los componentes de middleware, los controles de usuario y el streaming entre fotogramas. Es posible que los componentes de middleware no se exponán a un presupuesto ni tengan que trabajar estrechamente juntos. Es probable que los componentes de middleware puedan exponer características como técnicas de representación; y la aplicación podría basarse en la exposición de la configuración del middleware y del motor. Los desarrolladores podrían confiar en Direct3D 11 para realizar la paginación y lograr la velocidad de fotogramas adecuada. En algunos casos, es posible que las aplicaciones de Direct3D 11 hayan paginado el contenido de los recursos dentro y fuera de cada fotograma. y dio lugar a velocidades de fotogramas aceptables para el usuario. La mayoría de los motores solo transmite datos de recursos como una actividad en segundo plano, donde no tiene ninguna reserva correcta para el streaming dentro de fotogramas de alta prioridad. Al solicitar a los motores que implementen que se desasoyen algunas de las mejoras de sobrecarga de CPU que buscan, se pasará a Direct3D 12. Los desarrolladores de motor podrían considerar la posibilidad de analizar sus fotogramas en fases para proporcionar más oportunidades para los recursos que se pueden volver a usar. y probablemente trabajen con proveedores de middleware para admitir recursos y montones colocados para volver a usar la memoria dentro de fotogramas.

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

 

