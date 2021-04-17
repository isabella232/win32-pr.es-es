---
title: Usar estilos de ventana para cambiar la ventana de MCIWnd
description: Usar estilos de ventana para cambiar la ventana de MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- MCIWndCreate función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665791"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a>Usar estilos de ventana para cambiar la ventana de MCIWnd

Como ocurre con cualquier ventana, puede cambiar la apariencia y el comportamiento de una ventana de MCIWnd eligiendo entre los estilos de ventana estándar especificados con la función [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Además, puede elegir entre otros estilos de ventana específicos de MCIWnd Windows. Con estos estilos, la aplicación puede cambiar estas ventanas MCIWnd de las siguientes maneras:

-   Cambiar el tamaño de la ventana.
-   Ocultar o mostrar controles.
-   Emitir mensajes de notificación.
-   Mostrar información en la barra de título.

Puede establecer estilos de ventana mediante su especificación en la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) , o bien puede usar la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) para cambiar el estilo de una ventana MCIWnd existente. También puede consultar una ventana de MCIWnd para obtener sus estilos actuales mediante la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .

Para obtener una lista de los estilos de ventana específicos de MCIWnd, vea [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).

 

 