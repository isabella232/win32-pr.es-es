---
title: Compatibilidad de Unicode con controles comunes
description: En este tema se describe cómo admitir Unicode para notificaciones de control comunes.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01ab987516f1a91b47f8e5fd5f031631956d8c7bf59cd164edd83d414d5e72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668897"
---
# <a name="unicode-support-for-common-controls"></a>Compatibilidad de Unicode con controles comunes

En este tema se describe cómo admitir Unicode para notificaciones de control comunes.


Para las versiones 5.80 y posteriores de comctl32.dll, las notificaciones de controles comunes admiten formatos ANSI y Unicode en Windows sistemas 95 o versiones posteriores. El sistema determina qué formato se va a usar enviando a la ventana un [**mensaje \_ WM NOTIFYFORMAT.**](wm-notifyformat.md) Para especificar un formato, devuelva NFR \_ ANSI para notificaciones ANSI o UNICODE NFR para notificaciones \_ Unicode. Si no controla este mensaje, el sistema llama a [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) para determinar el formato. Puesto Windows 95 y Windows 98 siempre **devuelven FALSE** a esta llamada de función, usan notificaciones ANSI de forma predeterminada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles comunes](common-controls-intro.md)
</dt> </dl>

 

 