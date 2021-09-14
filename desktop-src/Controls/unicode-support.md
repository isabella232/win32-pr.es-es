---
title: Compatibilidad de Unicode con controles comunes
description: En este tema se describe cómo admitir Unicode para notificaciones de control comunes.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165454"
---
# <a name="unicode-support-for-common-controls"></a>Compatibilidad de Unicode con controles comunes

En este tema se describe cómo admitir Unicode para notificaciones de control comunes.


Para las versiones 5.80 y posteriores de comctl32.dll, las notificaciones de controles comunes admiten formatos ANSI y Unicode en Windows sistemas 95 o versiones posteriores. El sistema determina el formato que se va a usar mediante el envío de un mensaje [**\_ DE WM NOTIFYFORMAT**](wm-notifyformat.md) a la ventana. Para especificar un formato, devuelva NFR \_ ANSI para notificaciones ANSI o \_ NFR UNICODE para notificaciones Unicode. Si no controla este mensaje, el sistema llama a [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) para determinar el formato. Dado Windows 95 y Windows 98 siempre **devuelven FALSE** a esta llamada de función, usan notificaciones ANSI de forma predeterminada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles comunes](common-controls-intro.md)
</dt> </dl>

 

 