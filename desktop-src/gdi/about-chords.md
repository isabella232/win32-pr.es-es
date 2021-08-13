---
description: Una curva es una región delimitada por la intersección de una elipse y un segmento de línea denominado secant. En la ilustración siguiente se muestra un gráfico dibujado mediante la función Desenlazado.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Acerca de los contrabandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3bad0d17d34386ada7c7c3b46bb1bcc4db5f9a2ce572ce78c33f8f4b6af909
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400535"
---
# <a name="about-chords"></a>Acerca de los contrabandos

Una *curva* es una región delimitada por la intersección de una elipse y un segmento de línea denominado *secant*. En la ilustración siguiente se muestra un gráfico dibujado mediante la [**función Desenlazado.**](/windows/desktop/api/Wingdi/nf-wingdi-chord)

![ilustración de una elipse, en la que se muestran dos radiales, un secant y un desenlazador](images/csfsh-02.png)

Al llamar [**a Desenlace**](/windows/win32/api/wingdi/nf-wingdi-chord), una aplicación proporciona las coordenadas de las esquinas superior izquierda e inferior derecha del rectángulo delimitador de la elipse, así como las coordenadas de dos puntos que definen dos radiales. Un radial es una línea dibujada desde el centro del rectángulo delimitador de una elipse hasta un punto de la elipse.

Cuando el sistema dibuja la parte curva del desenlazado, lo hace usando la dirección del arco actual para el contexto de dispositivo especificado. La dirección del arco predeterminada es en sentido contrario a las agujas del reloj. Puede hacer que la aplicación restablezca la dirección del arco mediante una llamada a la [**función SetDirection.**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection)

 

 
