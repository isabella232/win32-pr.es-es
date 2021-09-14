---
description: La interfaz de control de retroiluminación es una interfaz IOCTL estandarizada para controlar el brillo de la retroiluminación DE WIFI.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interfaz de control de retroiluminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069179"
---
# <a name="backlight-control-interface"></a>Interfaz de control de retroiluminación

La interfaz de control de retroiluminación es una interfaz IOCTL estandarizada para controlar el brillo de la retroiluminación DE WIFI.

Las aplicaciones que requieren control mediante programación del brillo de la luz de fondo o proporcionan controles para que el usuario lo haga, deben usar esta interfaz en lugar de una interfaz propietaria. De lo contrario, el sistema no puede consultar el brillo del hardware actual y puede quedar sin sincronizar.

El primer paso consiste en consultar el brillo admitido en el dispositivo mediante el código de control [**\_ DE \_ \_ \_ BRILLO**](ioctl-video-query-supported-brightness.md) COMPATIBLE CON LA CONSULTA DE VÍDEO DE IOCTL. Esta operación devuelve un búfer que especifica los niveles de brillo disponibles. A continuación, puede consultar el brillo de la pantalla actual en el dispositivo mediante el código de control [**DISPLAY \_ BRIGHTNESS \_ \_ \_ DE LA**](ioctl-video-query-display-brightness.md) CONSULTA DE VÍDEO DE IOCTL. Esta operación devuelve la configuración actual para alternar el brillo de la corriente alterna (AC), el brillo de la corriente directa (DC) y el estado de energía.

Para cambiar el brillo de la pantalla, use el código de control [**DISPLAY BRIGHTNESS de IOCTL \_ VIDEO \_ SET. \_ \_**](ioctl-video-set-display-brightness.md) Puede establecer el brillo de la ca, el brillo del controlador de dominio o ambos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>

 

 



