---
description: Una aplicación rellena el interior de una región llamando a la función FillRgn y suministrando un identificador que identifica un pincel específico.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Rellenar regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d909643155b027f72b4235db366e640d7e53dacd4825b85090f9958aec1c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015405"
---
# <a name="filling-regions"></a>Rellenar regiones

Una aplicación rellena el interior de una región llamando a la [**función FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) y suministrando un identificador que identifica un pincel específico. Cuando una aplicación llama a FillRgn , el sistema rellena la región con el pincel mediante el modo de relleno actual para el contexto de dispositivo especificado. Hay dos modos de relleno: alternativo y sinuoso. La aplicación puede establecer el modo de relleno para un contexto de dispositivo llamando a la [**función SetPolyFillMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) La aplicación puede recuperar el modo de relleno actual para un contexto de dispositivo llamando a [**la función GetPolyFillMode.**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)

En la ilustración siguiente se muestran dos regiones idénticas: una rellena mediante el modo alternativo y la otra rellena mediante el modo de sinuoso.

![ilustración en la que se muestran dos estrellas de cinco puntas: una rellenada solo en los puntos y la otra rellena completamente](images/csrgn-03.png)

## <a name="alternate-mode"></a>Modo alternativo

Para determinar qué píxeles resalta el sistema cuando se especifica el modo alternativo, realice la siguiente prueba:

1.  Seleccione un píxel dentro del interior de la región.
2.  Dibuje un rayo imaginario, en la dirección X positiva, desde ese píxel hacia el infinito.
3.  Cada vez que el rayo forma una intersección con una línea de límite, incremente un valor de recuento.

El sistema resalta el píxel si el valor de recuento es un número impar.

## <a name="winding-mode"></a>Modo de enrollado

Para determinar los píxeles que el sistema resalta cuando se especifica el modo de desa prueba, realice la siguiente prueba:

1.  Determine la dirección en la que se dibuja cada línea de límite.
2.  Seleccione un píxel dentro del interior de la región.
3.  Dibuje un rayo imaginario, en la dirección X positiva, desde el píxel hasta el infinito.
4.  Cada vez que el rayo forma una intersección con una línea de límite con un componente Y positivo, incrementa un valor de recuento. Cada vez que el rayo forma una intersección con una línea de límite con un componente Y negativo, disminuye el valor de recuento.

El sistema resalta el píxel si el valor de recuento es distinto de cero.

 

 



