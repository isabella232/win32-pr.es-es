---
title: Controles de Windows
description: Un control es una ventana secundaria que una aplicación usa junto con otra ventana para habilitar la interacción con el usuario.
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bf14f3c93f6f38ba787cba463977a4dca9eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075327"
---
# <a name="windows-controls"></a>Controles de Windows

## <a name="purpose"></a>Propósito

Un control es una ventana secundaria que una aplicación usa junto con otra ventana para habilitar la interacción con el usuario. Los controles se usan con mayor frecuencia en los cuadros de diálogo, pero también se pueden usar en otras ventanas. Los controles de los cuadros de diálogo proporcionan al usuario una manera de escribir texto, elegir opciones e iniciar acciones. Los controles de otras ventanas proporcionan una variedad de servicios, como permitir al usuario elegir comandos, ver el estado y ver y editar texto. En esta documentación se describen los controles proporcionados por Windows y los elementos de programación que se usan para crearlos y manipularlos.

Para obtener una lista de todos los controles de Windows, incluido un vínculo a información general completa e información de referencia de cada control, vea [biblioteca de controles](individual-control-info.md).

## <a name="developer-audience"></a>Audiencia de desarrolladores

Los controles están diseñados para que los usen los desarrolladores de C/C++ y los diseñadores de la interfaz de usuario. En general, los desarrolladores necesitan un nivel moderado de comprensión sobre los conceptos de programación de la interfaz de usuario, la programación de la API de Windows y Unicode.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

User32.dll y Comctl32.dll proporcionan compatibilidad con los controles. Para obtener más información, vea [versiones de control comunes](common-control-versions.md).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                             | Descripción                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles comunes](common-controls-intro.md)<br/>                     | Proporciona información general que es común a todos los controles que son compatibles con Comctl32.dll.<br/>                                      |
| [Mensajes de control](control-messages.md)<br/>                               | Explica cómo se usan los mensajes de Windows para comunicarse con los controles.<br/>                                                                 |
| [Controles personalizados](user-controls-intro.md)<br/>                             | Describe varias maneras de crear controles personalizados. <br/>                                                                                 |
| [Subclase de controles](subclassing-overview.md)<br/>                       | Describe una manera de personalizar un control cambiando sus características o agregando nuevos. <br/>                                                 |
| [Dibujo personalizado](custom-draw.md)<br/>                                         | Describe un servicio, proporcionado por algunos controles, que las aplicaciones pueden utilizar para personalizar distintos aspectos de la apariencia del control. <br/> |
| [Consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md)<br/> | Proporciona información sobre las consideraciones de seguridad relacionadas con los controles de Windows. <br/>                                                 |
| [Biblioteca de controles](individual-control-info.md)<br/>                         | Proporciona información general e información de referencia sobre cada control admitido por User32.dll y Comctl32.dll.<br/>                            |
| [Referencia de control general](common-control-reference.md)<br/>              | Proporciona información de referencia sobre los elementos de programación que se aplican a varios controles, no solo a un control concreto.<br/>           |
| [Controlar Spy v 2.0](control-spy.md)<br/>                                    | Describe el control Spy, una herramienta que ayuda a los desarrolladores a comprender los controles comunes. <br/>                                                     |
| [Estilos visuales](themes-overview.md)<br/>                                   | Describe cómo puede cambiar la apariencia de los controles según el estilo visual elegido por el usuario. <br/>                               |
| [Formato de archivo de tema](themesfileformat-overview.md)<br/>                     | Describe el formato de los archivos de tema (. theme) utilizados en Windows 7 y Windows Vista.<br/>                                                    |



 

 

 





