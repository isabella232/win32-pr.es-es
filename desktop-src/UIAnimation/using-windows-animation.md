---
title: Tareas de animación de Windows
description: En los temas incluidos en esta sección se describen las tareas básicas necesarias para las aplicaciones que utilizan el administrador de animaciones de Windows.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Animación de Windows animación de Windows, tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695436"
---
# <a name="windows-animation-tasks"></a>Tareas de animación de Windows

En los temas incluidos en esta sección se describen las tareas básicas necesarias para las aplicaciones que utilizan el administrador de animaciones de Windows.

Estas tareas, en orden, incluyen:

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                | Descripción                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Crear los objetos de animación principales](adding-animation-to-an-application.md)<br/>               | Para usar la animación de Windows en la aplicación, el primer paso es crear un pequeño conjunto de objetos de animación principales.<br/>                                                                                                                                                                           |
| [Crear variables de animación](create-animation-variables.md)<br/>                              | Una aplicación debe crear una variable de animación para cada característica de visual que se va a animar mediante la animación de Windows.<br/>                                                                                                                                                            |
| [Actualizar el administrador de animaciones y dibujar marcos](introducing-windows-animation-manager.md)<br/> | Cada vez que una aplicación programa un guion gráfico, la aplicación debe proporcionar la hora actual al administrador de animaciones. También se requiere la hora actual al dirigir el administrador de animaciones para actualizar su estado y establecer todas las variables de animación en los valores interpolados adecuados.<br/> |
| [Leer los valores de las variables de animación](updating---application-driven-animation.md)<br/>         | Cada vez que la aplicación pinta, debe leer los valores actuales de las variables de animación que representan las características visuales que se van a animar.<br/>                                                                                                                                  |
| [Crear un guion gráfico y agregar transiciones](updating---timer-driven-animation.md)<br/>          | Para crear una animación, una aplicación debe construir un guion gráfico.<br/>                                                                                                                                                                                                                        |
| [Programar un guion gráfico](scheduling-a-storyboard.md)<br/>                                      | Una vez creado un guion gráfico, lo programa el administrador de animaciones.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre animaciones de Windows](scenic-animation-api-overview.md)
</dt> <dt>

[Referencia de animación de Windows](windows-animation-reference.md)
</dt> <dt>

[Ejemplos de animación de Windows](windows-animation-samples.md)
</dt> </dl>

 

 





