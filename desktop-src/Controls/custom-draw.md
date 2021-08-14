---
title: Dibujo personalizado
description: El dibujo personalizado no es un control común; es un servicio que proporcionan muchos controles comunes.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16271e915a942e21f3f3763237a25c37a8b934fc1a44a016bb7e3938491a3c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413183"
---
# <a name="custom-draw"></a>Dibujo personalizado

El dibujo personalizado no es un control común; es un servicio que proporcionan muchos controles comunes. El servicio de dibujo personalizado permite a una aplicación mayor flexibilidad a la hora de personalizar la apariencia de un control. La aplicación puede aprovechar las notificaciones de dibujo personalizadas para cambiar fácilmente la fuente que se usa para mostrar elementos o dibujar manualmente un elemento sin tener que realizar un dibujo de propietario completo.

Esta sección contiene información sobre los elementos de programación utilizados con el dibujo personalizado.

## <a name="overviews"></a>Temas de introducción



| Tema                                      | Contenido                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca del dibujo personalizado](about-custom-draw.md) | Esta sección contiene información general sobre la funcionalidad de dibujo personalizado y proporciona información general conceptual sobre cómo una aplicación puede admitir el dibujo personalizado.<br/> |
| [Usar dibujo personalizado](using-custom-draw.md) | Esta sección contiene ejemplos que muestran cómo implementar el dibujo personalizado. <br/>                                                                              |



 

## <a name="notifications"></a>Notificaciones



| Tema                               | Contenido                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW](nm-customdraw.md) | Notifica a la ventana primaria de un control las operaciones de dibujo personalizadas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/> |



 

## <a name="structures"></a>Estructuras



| Tema                                | Contenido                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | Contiene información específica de un código [de notificación DE NM \_ CUSTOMDRAW.](nm-customdraw.md)<br/> |



 

 

 





