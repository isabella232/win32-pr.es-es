---
description: Un contexto de dispositivo de ventana permite a una aplicación dibujar en cualquier parte de una ventana, incluido el área no cliente.
ms.assetid: 7b3c6352-51d5-4fdf-82c2-7a28194f607f
title: Ventana Mostrar contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75abed6177771d9beff56ad5e7dec1f8e0a704c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985343"
---
# <a name="window-display-device-contexts"></a>Ventana Mostrar contextos de dispositivo

Un *contexto de dispositivo de ventana* permite a una aplicación dibujar en cualquier parte de una ventana, incluido el área no cliente. Los contextos de dispositivo de ventana suelen usarse en aplicaciones que procesan los mensajes de [**WM \_ NCPAINT**](wm-ncpaint.md) y [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) para Windows con áreas no cliente personalizadas. No se recomienda usar un contexto de dispositivo de ventana para ningún otro propósito.

Una aplicación puede recuperar un contexto de dispositivo de ventana mediante la función [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) con la \_ opción de ventana DCX especificada. La función recupera un contexto de dispositivo de ventana de la caché de contexto del dispositivo de pantalla. Una ventana que use un contexto de dispositivo de ventana debe liberarla después de dibujar mediante la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) lo antes posible. Los contextos de dispositivo de ventana siempre son de la memoria caché; los \_ estilos de clase CS OWNDC y CS \_ CLASSDC no afectan al contexto del dispositivo.

Cuando una aplicación recupera un contexto de dispositivo de ventana, el sistema establece el origen del dispositivo en la esquina superior izquierda de la ventana en lugar de en la esquina superior izquierda del área de cliente. También establece la región de recorte para incluir toda la ventana, no solo el área cliente. El sistema establece los valores de atributo actuales de un contexto de dispositivo de ventana en los mismos valores predeterminados que un contexto de dispositivo común. Una aplicación puede cambiar los valores de atributo, pero el sistema no conserva los cambios cuando se libera el contexto del dispositivo.

 

 
