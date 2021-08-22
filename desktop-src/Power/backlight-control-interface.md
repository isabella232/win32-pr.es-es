---
description: La interfaz de control de retroiluminación es una interfaz IOCTL estandarizada para controlar el brillo de la retroiluminación DE COLOR de fondo.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interfaz de control de retroiluminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a6a82cede03d18f9d237bab09a590f9bcdc0da86651dacd0912357c32d36ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143728"
---
# <a name="backlight-control-interface"></a>Interfaz de control de retroiluminación

La interfaz de control de retroiluminación es una interfaz IOCTL estandarizada para controlar el brillo de la retroiluminación DE COLOR de fondo.

Las aplicaciones que requieren el control mediante programación del brillo de la luz de fondo o proporcionan controles para que el usuario lo haga debe usar esta interfaz en lugar de una interfaz propietaria. De lo contrario, el sistema no puede consultar el brillo del hardware actual y puede quedar sin sincronizar.

El primer paso consiste en consultar el brillo admitido en el dispositivo mediante el código de control [**ICTL \_ VIDEO QUERY \_ SUPPORTED \_ \_ BRIGHTNESS.**](ioctl-video-query-supported-brightness.md) Esta operación devuelve un búfer que especifica los niveles de brillo disponibles. A continuación, puede consultar el brillo de la pantalla actual en el dispositivo mediante el código de control [**DISPLAY BRIGHTNESS de IOCTL \_ VIDEO \_ QUERY. \_ \_**](ioctl-video-query-display-brightness.md) Esta operación devuelve la configuración actual para alternar el brillo actual (AC), el brillo de la corriente directa (DC) y el estado de energía.

Para cambiar el brillo de la pantalla, use el código de control [**DISPLAY BRIGHTNESS de IOCTL \_ VIDEO \_ SET. \_ \_**](ioctl-video-set-display-brightness.md) Puede establecer el brillo de la ca, el brillo del controlador de dominio o ambos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>

 

 



