---
title: Administrador de ventanas de escritorio
description: La característica de composición de escritorio, introducida en Windows Vista, cambió fundamentalmente la forma en que las aplicaciones muestran píxeles en la pantalla.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Administrador de ventanas de escritorio (DWM),about
- DWM (Administrador de ventanas de escritorio),about
- Administrador de ventanas de escritorio (DWM),composition
- DWM (Administrador de ventanas de escritorio),composition
- composición de escritorio
- composición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8259be171f225cc955546314febdff5395a47318499b830ee855bc8b985b025
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456045"
---
# <a name="desktop-window-manager"></a>Administrador de ventanas de escritorio

La característica de composición de escritorio, introducida en Windows Vista, cambió fundamentalmente la forma en que las aplicaciones muestran píxeles en la pantalla. Cuando la composición de escritorio está habilitada, las ventanas individuales ya no se dibujan directamente en la pantalla o en el dispositivo de pantalla principal como lo hacían en versiones anteriores de Windows. En su lugar, su dibujo se redirige a superficies fuera de la pantalla en la memoria de vídeo, que luego se representan en una imagen de escritorio y se presentan en la pantalla.

La composición de escritorio la realiza Administrador de ventanas de escritorio (DWM). A través de la composición de escritorio, DWM permite efectos visuales en el escritorio, así como varias características, como marcos de ventanas de cristal, animaciones de transición de ventanas 3D, Windows Flip y Windows Flip3D y compatibilidad con alta resolución.

El Administrador de ventanas de escritorio se ejecuta como un Windows servicio. Se puede habilitar y deshabilitar mediante el elemento Herramientas administrativas Panel de control, en Servicios, como administrador de Administrador de ventanas de escritorio sesión.

Muchas de las características de DWM se pueden controlar o acceder mediante una aplicación a través de las API de DWM. En la siguiente documentación se describen las características y los requisitos de las API de DWM.

-   [Información general de DWM](desktop-window-manager-overviews.md)
-   [Código de ejemplo de DWM](dwm-samples.md)
-   [Referencia de DWM](reference.md)

 

 




