---
description: Además de dibujar líneas o curvas, las aplicaciones pueden dibujar combinaciones de salida de línea y curva llamando a una sola función. Por ejemplo, una aplicación puede dibujar el contorno de un gráfico circular mediante una llamada a la función AngleMonte.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Líneas y curvas combinadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1939b863bfacf2176f15c950b48c8b7c91cc43e7b6b4d4c58ac08e1760c4cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105724"
---
# <a name="combined-lines-and-curves"></a>Líneas y curvas combinadas

Además de dibujar líneas o curvas, las aplicaciones pueden dibujar combinaciones de salida de línea y curva llamando a una sola función. Por ejemplo, una aplicación puede dibujar el contorno de un gráfico circular mediante una llamada a [**la función AngleMonte.**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)

La [**función AngleOr**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) dibuja un arco a lo largo del perímetro de un círculo y dibuja una línea que conecta el punto inicial del arco con el centro del círculo. Además de usar la función **AngleGraf,** una aplicación también puede combinar la salida de curva irregular y de línea mediante [**la función PolyDraw.**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)

 

 



