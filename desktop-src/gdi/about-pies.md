---
description: Un gráfico circular es una región enlazada por la intersección de una curva de elipse y dos radiales. En la ilustración siguiente se muestra un gráfico circular dibujada con la función de gráfico circular.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Acerca de los gráficos circulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082372"
---
# <a name="about-pies"></a>Acerca de los gráficos circulares

Un *gráfico circular* es una región enlazada por la intersección de una curva de elipse y dos radiales. En la ilustración siguiente se muestra un gráfico circular dibujada con la función de [**gráfico circular**](/windows/desktop/api/Wingdi/nf-wingdi-pie) .

![Ilustración en la que se muestra una elipse con un círculo sombreado](images/csfsh-03.png)

Al llamar a un [**gráfico circular**](/windows/win32/api/wingdi/nf-wingdi-pie), una aplicación proporciona las coordenadas de las esquinas superior izquierda e inferior derecha del rectángulo delimitador de la elipse, así como las coordenadas de dos puntos que definen dos radiales.

Cuando el sistema dibuja la parte curva del gráfico circular, usa la dirección de arco actual para el contexto de dispositivo determinado. La dirección de arco predeterminada es en sentido contrario a las agujas del reloj. Una aplicación puede restablecer la dirección del arco llamando a la función [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .

 

 
