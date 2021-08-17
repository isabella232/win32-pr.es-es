---
title: Windows Tareas de animación
description: Los temas contenidos en esta sección describen las tareas básicas necesarias para las aplicaciones que usan Windows Animation Manager.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Windows Animation Windows Animation ,tasks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8f5116a6e36697e649ad81bfbad883c57aee50440c3ba80734419ce2fb372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058153"
---
# <a name="windows-animation-tasks"></a>Windows Tareas de animación

Los temas contenidos en esta sección describen las tareas básicas necesarias para las aplicaciones que usan Windows Animation Manager.

Estas tareas, en orden, incluyen:

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                | Descripción                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Crear los objetos de animación principales](adding-animation-to-an-application.md)<br/>               | Para usar Windows animation en la aplicación, el primer paso es crear un pequeño conjunto de objetos de animación principales.<br/>                                                                                                                                                                           |
| [Crear variables de animación](create-animation-variables.md)<br/>                              | Una aplicación debe crear una variable de animación para cada característica visual que se va a animar mediante Windows animación.<br/>                                                                                                                                                            |
| [Actualizar el Administrador de animaciones y dibujar fotogramas](introducing-windows-animation-manager.md)<br/> | Cada vez que una aplicación programa un guión gráfico, la aplicación debe proporcionar la hora actual al administrador de animaciones. La hora actual también es necesaria al dirigir al administrador de animaciones para que actualice su estado y establezca todas las variables de animación en los valores interpolados adecuados.<br/> |
| [Leer los valores de las variables de animación](updating---application-driven-animation.md)<br/>         | Cada vez que la aplicación pinta, debe leer los valores actuales de las variables de animación que representan las características visuales que se animarán.<br/>                                                                                                                                  |
| [Crear un guión gráfico y agregar transiciones](updating---timer-driven-animation.md)<br/>          | Para crear una animación, una aplicación debe construir un guión gráfico.<br/>                                                                                                                                                                                                                        |
| [Programar un guión gráfico](scheduling-a-storyboard.md)<br/>                                      | Una vez creado un guión gráfico, lo programa el administrador de animaciones.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Información general sobre animaciones](scenic-animation-api-overview.md)
</dt> <dt>

[Windows Referencia de animación](windows-animation-reference.md)
</dt> <dt>

[Windows Ejemplos de animación](windows-animation-samples.md)
</dt> </dl>

 

 





