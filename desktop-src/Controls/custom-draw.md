---
title: Dibujo personalizado
description: El dibujo personalizado no es un control común; es un servicio que proporcionan muchos controles comunes.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994029"
---
# <a name="custom-draw"></a>Dibujo personalizado

El dibujo personalizado no es un control común; es un servicio que proporcionan muchos controles comunes. El servicio de dibujo personalizado permite que una aplicación tenga mayor flexibilidad en la personalización de la apariencia de un control. La aplicación puede aprovechar las notificaciones de dibujo personalizadas para cambiar fácilmente la fuente usada para mostrar elementos o dibujar manualmente un elemento sin tener que realizar un dibujo de propietario completo.

Esta sección contiene información sobre los elementos de programación utilizados con Draw personalizado.

## <a name="overviews"></a>Temas de introducción



| Tema                                      | Contenido                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de Draw personalizado](about-custom-draw.md) | Esta sección contiene información general sobre la funcionalidad de dibujo personalizado y proporciona información conceptual sobre cómo una aplicación puede admitir el dibujo personalizado.<br/> |
| [Usar Draw personalizado](using-custom-draw.md) | Esta sección contiene ejemplos que muestran cómo implementar Draw personalizado. <br/>                                                                              |



 

## <a name="notifications"></a>Notificaciones



| Tema                               | Contenido                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW](nm-customdraw.md) | Notifica a la ventana primaria de un control sobre las operaciones de dibujo personalizadas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/> |



 

## <a name="structures"></a>Estructuras



| Tema                                | Contenido                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | Contiene información específica de un código de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) .<br/> |



 

 

 





