---
title: Compatibilidad con Unicode para controles comunes
description: En este tema se describe cómo admitir Unicode para las notificaciones de control comunes.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995752"
---
# <a name="unicode-support-for-common-controls"></a>Compatibilidad con Unicode para controles comunes

En este tema se describe cómo admitir Unicode para las notificaciones de control comunes.


En las versiones 5,80 y posteriores de comctl32.dll, las notificaciones de controles comunes admiten los formatos ANSI y Unicode en sistemas Windows 95 o posterior. El sistema determina el formato que se va a usar mediante el envío de la ventana a un mensaje de [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) . Para especificar un formato, devuelve \_ ANSI de NFR para las notificaciones ANSI o \_ Unicode NFR para las notificaciones Unicode. Si no controla este mensaje, el sistema llama a [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) para determinar el formato. Dado que Windows 95 y Windows 98 siempre devuelven **false** a esta llamada de función, usan notificaciones ANSI de forma predeterminada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles comunes](common-controls-intro.md)
</dt> </dl>

 

 