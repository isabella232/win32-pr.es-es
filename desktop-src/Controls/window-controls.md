---
title: Windows Controles
description: Un control es una ventana secundaria que una aplicación usa junto con otra ventana para habilitar la interacción del usuario.
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bf14f3c93f6f38ba787cba463977a4dca9eda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165254"
---
# <a name="windows-controls"></a>Windows Controles

## <a name="purpose"></a>Propósito

Un control es una ventana secundaria que una aplicación usa junto con otra ventana para habilitar la interacción del usuario. Los controles se usan con más frecuencia dentro de los cuadros de diálogo, pero también se pueden usar en otras ventanas. Los controles de los cuadros de diálogo proporcionan al usuario una manera de escribir texto, elegir opciones e iniciar acciones. Los controles de otras ventanas proporcionan una variedad de servicios, como permitir al usuario elegir comandos, ver el estado y ver y editar texto. En esta documentación se describen los controles proporcionados por Windows y los elementos de programación utilizados para crearlos y manipularlos.

Para obtener una lista de todos los Windows controles, incluido un vínculo a información general completa e información de referencia para cada control, vea [Biblioteca de controles](individual-control-info.md).

## <a name="developer-audience"></a>Audiencia de desarrolladores

Los controles están diseñados para su uso por parte de desarrolladores de C/C++ y diseñadores de interfaz de usuario. En general, los desarrolladores necesitan un nivel moderado de comprensión sobre los conceptos de programación de la interfaz de usuario, Windows programación de API y Unicode.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La compatibilidad con los controles se proporciona User32.dll y Comctl32.dll. Para obtener más información, vea [Versiones de control comunes](common-control-versions.md).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                             | Descripción                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles comunes](common-controls-intro.md)<br/>                     | Proporciona información general que es común a todos los controles admitidos por Comctl32.dll.<br/>                                      |
| [Mensajes de control](control-messages.md)<br/>                               | Explica cómo Windows mensajes se usan para comunicarse con controles.<br/>                                                                 |
| [Controles personalizados](user-controls-intro.md)<br/>                             | Describe varias maneras de crear controles personalizados. <br/>                                                                                 |
| [Controles de subclases](subclassing-overview.md)<br/>                       | Describe una manera de personalizar un control cambiando sus características o agregando otras nuevas. <br/>                                                 |
| [Dibujo personalizado](custom-draw.md)<br/>                                         | Describe un servicio, proporcionado por algunos controles, que las aplicaciones pueden usar para personalizar varios aspectos de la apariencia del control. <br/> |
| [Consideraciones de seguridad: Controles de Windows Microsoft](sec-comctls.md)<br/> | Proporciona información sobre las consideraciones de seguridad relacionadas con los Windows controles. <br/>                                                 |
| [Biblioteca de controles](individual-control-info.md)<br/>                         | Proporciona información general e información de referencia sobre cada control admitido por User32.dll y Comctl32.dll.<br/>                            |
| [Referencia general de control](common-control-reference.md)<br/>              | Proporciona información de referencia sobre los elementos de programación que se aplican a varios controles, no solo a un control específico.<br/>           |
| [Control Spy v2.0](control-spy.md)<br/>                                    | Describe Control Spy, una herramienta que ayuda a los desarrolladores a comprender los controles comunes. <br/>                                                     |
| [Estilos visuales](themes-overview.md)<br/>                                   | Describe cómo puede cambiar la apariencia de los controles en función del estilo visual elegido por el usuario. <br/>                               |
| [Formato de archivo de tema](themesfileformat-overview.md)<br/>                     | Describe el formato de los archivos theme (.theme) usados en Windows 7 y Windows Vista.<br/>                                                    |



 

 

 





