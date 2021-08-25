---
description: Un contexto de dispositivo de ventana permite que una aplicación dibuje en cualquier parte de una ventana, incluido el área no cliente.
ms.assetid: 7b3c6352-51d5-4fdf-82c2-7a28194f607f
title: Contextos de dispositivo de visualización de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfed34646323114ffcfb7753331b1b5c305a7a0c01a475795a7918f6e5a2dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965095"
---
# <a name="window-display-device-contexts"></a>Contextos de dispositivo de visualización de ventana

Un *contexto de dispositivo de ventana* permite que una aplicación dibuje en cualquier parte de una ventana, incluido el área no cliente. Los contextos de dispositivo de ventana suelen usarse en aplicaciones que procesan los mensajes [**WM \_ NCPAINT**](wm-ncpaint.md) y [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) para ventanas con áreas no cliente personalizadas. No se recomienda usar un contexto de dispositivo de ventana para ningún otro propósito.

Una aplicación puede recuperar un contexto de dispositivo de ventana mediante la [**función GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) con la opción DCX \_ WINDOW especificada. La función recupera un contexto de dispositivo de ventana de la caché de contexto del dispositivo para mostrar. Una ventana que usa un contexto de dispositivo de ventana debe liberarla después de dibujar mediante la [**función ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) lo antes posible. Los contextos de dispositivo de ventana siempre son de la memoria caché; Los estilos de clase \_ CS OWNDC y \_ CS CLASSDC no afectan al contexto del dispositivo.

Cuando una aplicación recupera un contexto de dispositivo de ventana, el sistema establece el origen del dispositivo en la esquina superior izquierda de la ventana en lugar de en la esquina superior izquierda del área de cliente. También establece la región de recorte para incluir toda la ventana, no solo el área de cliente. El sistema establece los valores de atributo actuales de un contexto de dispositivo de ventana en los mismos valores predeterminados que un contexto de dispositivo común. Una aplicación puede cambiar los valores de atributo, pero el sistema no conserva los cambios cuando se libera el contexto del dispositivo.

 

 
