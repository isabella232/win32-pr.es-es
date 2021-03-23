---
title: Envío de trabajo en Direct3D 12
description: Para mejorar la eficacia de la CPU de las aplicaciones Direct3D, Direct3D 12 ya no admite un contexto inmediato asociado a un dispositivo.
ms.assetid: BE2F46EA-D4A9-47F7-A2D1-6A486DD4DC1A
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: aa852fc82280b14b0270a7c4a4c40cfe441803b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104512"
---
# <a name="work-submission-in-direct3d-12"></a>Envío de trabajo en Direct3D 12

Para mejorar la eficacia de la CPU de las aplicaciones de Direct3D, a partir de la versión 12, Direct3D ya no admite un contexto inmediato asociado a un dispositivo. En su lugar, la aplicación registra y envía *listas de comandos*, que contienen llamadas de administración de dibujos y recursos. Puede enviar estas listas de comandos desde varios subprocesos a una o varias colas de comandos, que administran la ejecución de los comandos. Este cambio fundamental aumenta la eficacia de un solo subproceso, ya que permite que la aplicación procese previamente el trabajo de representación para su reutilización posterior y aprovecha los sistemas de varios núcleos mediante la propagación del trabajo de representación entre varios subprocesos.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Diseño de la filosofía de las colas de comandos y listas de comandos](design-philosophy-of-command-queues-and-command-lists.md) | Los objetivos de habilitar la reutilización del trabajo de representación y del escalado multiproceso requieren cambios fundamentales en el modo en que las aplicaciones de Direct3D envían el trabajo de representación a la GPU. |
| [Creación y grabación de listas de comandos y agrupaciones](recording-command-lists-and-bundles.md) | En este tema se describe la grabación de listas de comandos y agrupaciones en aplicaciones de Direct3D 12. Las listas de comandos y las agrupaciones permiten a las aplicaciones grabar llamadas de dibujo o cambio de estado para su ejecución posterior en la unidad de procesamiento de gráficos (GPU). |
| [Ejecutar y sincronizar listas de comandos](executing-and-synchronizing-command-lists.md) | En Microsoft Direct3D 12, el modo inmediato de versiones anteriores ya no está presente. En su lugar, las aplicaciones crean listas y agrupaciones de comandos y, a continuación, registran conjuntos de comandos de GPU. Las colas de comandos se usan para enviar listas de comandos que se van a ejecutar. Este modelo permite a los desarrolladores tener más control sobre el uso eficaz de la GPU y la CPU. |
| [Administrar el estado de canalización de gráficos en Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md) | En este tema se describe cómo se establece el estado de canalización de gráficos en Direct3D 12. |
| [Usar barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md) | Para reducir el uso general de la CPU y habilitar el procesamiento previo y multithreading del controlador, Direct3D 12 mueve la responsabilidad de la administración de Estados por recurso del controlador de gráficos a la aplicación. |
| [Canalizaciones y sombreadores con Direct3D 12](pipelines-and-shaders-with-directx-12.md) | La canalización programable de Direct3D 12 aumenta considerablemente el rendimiento de la representación en comparación con las interfaces de programación de gráficos de generación anterior. |
| [Sombreado de velocidad variable (VRS)](vrs.md) | El sombreado de velocidad variable &mdash; o el sombreado de píxeles gruesos &mdash; es un mecanismo que permite asignar potencia y rendimiento de la representación que varían en la imagen representada. |
| [Fases de representación](direct3d-12-render-passes.md) | La característica de pasos de representación ayuda al representador a mejorar la eficacia de la GPU al reducir el tráfico de memoria hacia y desde la memoria fuera del chip; para ello, permite a la aplicación identificar mejor los requisitos de orden de representación de recursos y las dependencias de datos. |

## <a name="related-topics"></a>Temas relacionados

* [Guía de programación de Direct3D 12](directx-12-programming-guide.md)
