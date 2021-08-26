---
description: Cada monitor puede tener su propia profundidad de color.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Colores en varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd799599f3818ad002ee8a0fa1e9478f383b3052dd3a2cc3b8a40843e431b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115325"
---
# <a name="colors-on-multiple-display-monitors"></a>Colores en varios monitores de pantalla

Cada monitor puede tener su propia profundidad de color. El sistema ajusta automáticamente los colores a medida que las ventanas se mueven entre monitores con diferentes profundidades de color. En general, esto genera buenos resultados. Sin embargo, esto no siempre es óptimo. Para aprovechar las funcionalidades de color de diferentes monitores, consulte la sección Pintar en varios monitores [de](painting-on-multiple-display-monitors.md) pantalla que se muestra a continuación.

Para determinar si todos los monitores tienen el mismo formato de color, llame a [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ SAMEDISPLAYFORMAT.

Si el monitor principal está sobresaltado, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) y [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) funcionan igual que antes, pero en todos los monitores. Además, se sincronizan las paletas de todos los dispositivos de color verde. Si el monitor principal no está sobresaltado, **SelectPalette** y **RealizePalette** seleccionarán la paleta en segundo plano y no se sincronizarán los dispositivos con tantización.

 

 
