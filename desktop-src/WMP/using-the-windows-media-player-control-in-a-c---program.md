---
title: Usar el control Media Player de Windows en un programa de C++
description: Usar el control Media Player de Windows en un programa de C++
ms.assetid: 2531ac25-5e9d-462e-a06a-6f81bf4ca33d
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, C++
- Modelo de objetos de Windows Media Player, C++
- modelo de objetos, C++
- Windows Media Player Mobile, C++
- Control ActiveX de Windows Media Player, C++
- Control ActiveX móvil de Windows Media Player, C++
- Control ActiveX, C++
- Incrustación de programas de C++
- incrustación, programas de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02430dbdaba3bb2e8ea3ca6e46b202a289a096f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269074"
---
# <a name="using-the-windows-media-player-control-in-a-c-program"></a>Usar el control Media Player de Windows en un programa de C++

> [!Note]  
> El uso de C++ para insertar el control Media Player de Windows es compatible con Windows Media Player 9 series o posterior.

 

Hay varias maneras de usar el control de Media Player de Windows en un programa de C++. Puede crear una instancia del control en una aplicación de consola o puede incrustar el control en una aplicación de Windows. Además, puede implementar interfaces que le permitan ejecutar un control Embedded Player en modo remoto. Puede personalizar la interfaz de usuario de un control incrustado aplicando un archivo de definición de máscara.

Esta información se describe en los temas siguientes.



| Tema                                                                                                                                      | Descripción                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Usar el control de Media Player de Windows en una aplicación de consola](using-the-windows-media-player-control-in-a-console-application.md)     | Describe una sencilla aplicación de consola de C++ que crea instancias del control Media Player de Windows para mostrar la versión.                                                       |
| [Hospedar el control de Media Player de Windows en una aplicación de Windows](hosting-the-windows-media-player-control-in-a-windows-application.md) | Describe cómo utilizar la ventana host ActiveX ATL para incrustar el control Media Player de Windows en un programa de Windows.                                                            |
| [Control remoto del Reproductor de Windows Media](remoting-the-windows-media-player-control.md)                                                 | Describe cómo incrustar el control Media Player de Windows en un programa de C++ en modo remoto, lo que permite a los usuarios desacoplar el control para cambiar al modo completo del reproductor. |
| [Controlar eventos en C++](handling-events-in-c.md)                                                                                         | Describe cómo recibir notificaciones de eventos de Windows Media Player.                                                                                                     |
| [Usar máscaras con el control Media Player de Windows](using-skins-with-the-windows-media-player-control.md)                                 | Describe cómo aplicar un archivo de máscara a un control de Media Player de Windows incrustado en un programa de C++.                                                                             |



 

> [!Note]  
> Puede incrustar el control de Windows Media Player 10 Mobile en una aplicación Windows CE. Las técnicas que se usan para ello son similares a las que se usan con el control de Media Player de escritorio de Windows. Sin embargo, hay diferencias entre ATL para Windows y ATL para Windows CE. En esta documentación se describen las diferencias entre estas implementaciones, si es necesario.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia del modelo de objetos para C++**](object-model-reference-for-c.md)
</dt> <dt>

[**Guía de control del reproductor**](player-control-guide.md)
</dt> </dl>

 

 




