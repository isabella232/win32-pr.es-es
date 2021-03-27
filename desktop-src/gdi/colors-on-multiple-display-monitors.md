---
description: Cada monitor puede tener su propia profundidad de color.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Colores en varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001526"
---
# <a name="colors-on-multiple-display-monitors"></a>Colores en varios monitores de pantalla

Cada monitor puede tener su propia profundidad de color. El sistema ajusta automáticamente los colores a medida que las ventanas se mueven por los monitores con diferentes profundidades de color. En general, esto produce buenos resultados. Sin embargo, esto no es siempre óptimo. Para aprovechar las capacidades de color de los distintos monitores, consulte la sección [pintar en varios monitores de pantalla](painting-on-multiple-display-monitors.md) siguiente.

Para determinar si todos los monitores tienen el mismo formato de color, llame a [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ SAMEDISPLAYFORMAT.

Si el monitor principal está en la paleta, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) y [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) funcionan igual que antes, pero en todos los monitores. Además, las paletas de todos los dispositivos de paleta están sincronizadas. Si el monitor principal no es de paleta, **SelectPalette** y **RealizePalette** seleccionarán la paleta en segundo plano y los dispositivos de paleta no se sincronizarán.

 

 
