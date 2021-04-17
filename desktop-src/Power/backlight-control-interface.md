---
description: La interfaz de control de retroiluminación es una interfaz IOCTL normalizada para controlar el brillo de la retroiluminación de la LCD.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interfaz de control de retroiluminación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667231"
---
# <a name="backlight-control-interface"></a>Interfaz de control de retroiluminación

La interfaz de control de retroiluminación es una interfaz IOCTL normalizada para controlar el brillo de la retroiluminación de la LCD.

Las aplicaciones que requieren el control mediante programación del brillo de la luz de luz o que proporcionan controles para que el usuario lo hagan deben usar esta interfaz en lugar de una interfaz de propiedad. de lo contrario, el sistema no puede consultar el brillo actual del hardware y puede quedar sin sincronizar.

El primer paso es consultar en el dispositivo el brillo compatible mediante el código de control de [**\_ \_ \_ \_ brillo compatible con la consulta de vídeo ioctl**](ioctl-video-query-supported-brightness.md) . Esta operación devuelve un búfer que especifica los niveles de brillo disponibles. Después, puede consultar el dispositivo para ver el brillo de la pantalla actual mediante la [**consulta de vídeo ioctl mostrar el código de control de \_ \_ \_ \_ brillo**](ioctl-video-query-display-brightness.md) . Esta operación devuelve la configuración actual del brillo (AC) actual alterno, el brillo actual (DC) y el estado de la energía.

Para cambiar el brillo de la pantalla, use el código de control de [**\_ \_ \_ \_ brillo del conjunto de vídeos de ioctl**](ioctl-video-set-display-brightness.md) . Puede establecer el brillo de la AC, el brillo del controlador de dominio o ambos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>

 

 



