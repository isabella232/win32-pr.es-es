---
description: Además de dibujar líneas o curvas, las aplicaciones pueden dibujar combinaciones de salida de línea y curva llamando a una sola función. Por ejemplo, una aplicación puede dibujar el contorno de un gráfico circular mediante una llamada a la función AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Líneas y curvas combinadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985027"
---
# <a name="combined-lines-and-curves"></a>Líneas y curvas combinadas

Además de dibujar líneas o curvas, las aplicaciones pueden dibujar combinaciones de salida de línea y curva llamando a una sola función. Por ejemplo, una aplicación puede dibujar el contorno de un gráfico circular mediante una llamada a la función [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .

La función [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) dibuja un arco a lo largo del perímetro de un círculo y dibuja una línea que conecta el punto inicial del arco al centro del círculo. Además de usar la función **AngleArc** , una aplicación también puede combinar una salida de curva de línea y irregular mediante la función de [**polidraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .

 

 



