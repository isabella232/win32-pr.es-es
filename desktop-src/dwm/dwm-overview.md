---
title: Administrador de ventanas de escritorio
description: La característica de composición de escritorio, introducida en Windows Vista, ha cambiado fundamentalmente el modo en que las aplicaciones muestran píxeles en la pantalla.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Administrador de ventanas de escritorio (DWM), acerca de
- DWM (Administrador de ventanas de escritorio), acerca de
- Administrador de ventanas de escritorio (DWM), composición
- DWM (Administrador de ventanas de escritorio), composición
- composición de escritorio
- composición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776728"
---
# <a name="desktop-window-manager"></a>Administrador de ventanas de escritorio

La característica de composición de escritorio, introducida en Windows Vista, ha cambiado fundamentalmente el modo en que las aplicaciones muestran píxeles en la pantalla. Cuando la composición del escritorio está habilitada, las ventanas individuales ya no se dibujan directamente en la pantalla o en el dispositivo de pantalla principal como ocurría en versiones anteriores de Windows. En su lugar, su dibujo se redirige a superficies fuera de la pantalla en la memoria de vídeo, que luego se representan en una imagen de escritorio y se muestran en la pantalla.

La composición del escritorio se realiza mediante el Administrador de ventanas de escritorio (DWM). A través de la composición del escritorio, DWM permite efectos visuales en el escritorio, así como diversas características, como marcos de ventanas de cristal, animaciones de transición de ventanas 3D, Windows Flip y Windows Flip3D y compatibilidad con alta resolución.

La Administrador de ventanas de escritorio se ejecuta como un servicio de Windows. Se puede habilitar y deshabilitar mediante el elemento del panel de control herramientas administrativas, en servicios, como Administrador de ventanas de escritorio administrador de sesión.

Una aplicación puede controlar muchas de las características de DWM o tener acceso a ellas a través de las API de DWM. En la documentación siguiente se describen las características y los requisitos de las API de DWM.

-   [Información general de DWM](desktop-window-manager-overviews.md)
-   [Código de ejemplo de DWM](dwm-samples.md)
-   [Referencia de DWM](reference.md)

 

 




