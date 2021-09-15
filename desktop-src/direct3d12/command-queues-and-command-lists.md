---
title: Envío de trabajo en Direct3D 12
description: Para mejorar la eficacia de la CPU de las aplicaciones de Direct3D, Direct3D 12 ya no admite un contexto inmediato asociado a un dispositivo.
ms.assetid: BE2F46EA-D4A9-47F7-A2D1-6A486DD4DC1A
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: aa852fc82280b14b0270a7c4a4c40cfe441803b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570916"
---
# <a name="work-submission-in-direct3d-12"></a>Envío de trabajo en Direct3D 12

Para mejorar la eficacia de la CPU de las aplicaciones de Direct3D, a partir de la versión 12, Direct3D ya no admite un contexto inmediato asociado a un dispositivo. En su lugar, la aplicación registra y, a continuación, envía listas *de comandos*, que contienen llamadas de administración de recursos y dibujos. Puede enviar estas listas de comandos de varios subprocesos a una o varias colas de comandos, que administran la ejecución de los comandos. Este cambio fundamental aumenta la eficacia de un solo subproceso al permitir que la aplicación preprocese el trabajo de representación para su posterior uso, y aprovecha las ventajas de los sistemas de varios núcleos al distribuir el trabajo de representación entre varios subprocesos.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Filosofía de diseño de colas de comandos y listas de comandos](design-philosophy-of-command-queues-and-command-lists.md) | Los objetivos de habilitar la reutilización del trabajo de representación y del escalado multiproceso requerían cambios fundamentales en la forma en que las aplicaciones de Direct3D envían el trabajo de representación a la GPU. |
| [Creación y grabación de listas de comandos y agrupaciones](recording-command-lists-and-bundles.md) | En este tema se describen las listas y agrupaciones de comandos de grabación en aplicaciones de Direct3D 12. Tanto las listas de comandos como los paquetes permiten a las aplicaciones registrar llamadas de dibujo o de cambio de estado para su posterior ejecución en la unidad de procesamiento de gráficos (GPU). |
| [Ejecución y sincronización de listas de comandos](executing-and-synchronizing-command-lists.md) | En Microsoft Direct3D 12, el modo inmediato de las versiones anteriores ya no está presente. En su lugar, las aplicaciones crean listas de comandos y agrupan y, a continuación, registran conjuntos de comandos de GPU. Las colas de comandos se usan para enviar listas de comandos que se van a ejecutar. Este modelo permite a los desarrolladores tener más control sobre el uso eficaz de GPU y CPU. |
| [Administración del estado de canalización de gráficos en Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md) | En este tema se describe cómo se establece el estado de canalización de gráficos en Direct3D 12. |
| [Uso de barreras de recursos para sincronizar estados de recursos en Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md) | Para reducir el uso general de la CPU y habilitar el multiproceso y el procesamiento previo del controlador, Direct3D 12 traslada la responsabilidad de la administración del estado por recurso del controlador de gráficos a la aplicación. |
| [Pipelines y sombreadores con Direct3D 12](pipelines-and-shaders-with-directx-12.md) | La canalización programable direct3D 12 aumenta significativamente el rendimiento de representación en comparación con las interfaces de programación de gráficos de generación anterior. |
| [Sombreado de velocidad variable (VRS)](vrs.md) | El sombreado de velocidad variable o el sombreado de píxeles general es un mecanismo que le permite asignar rendimiento o potencia de representación a velocidades que varían en la &mdash; &mdash; imagen representada. |
| [Fases de representación](direct3d-12-render-passes.md) | La característica de pases de representación ayuda al representador a mejorar la eficacia de GPU al reducir el tráfico de memoria hacia y desde la memoria fuera del chip. para ello, permite a la aplicación identificar mejor los requisitos de ordenación de la representación de recursos y las dependencias de datos. |

## <a name="related-topics"></a>Temas relacionados

* [Guía de programación de Direct3D 12](directx-12-programming-guide.md)
