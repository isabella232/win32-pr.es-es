---
description: La mayoría de las aplicaciones intentan admitir la salida DE WYSIWYG (lo que ve es lo que obtiene).
ms.assetid: 34a1f37c-0fbf-451b-bb55-80ad85bcd4de
title: Visualización y salida de WYSIWYG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ee426665508bee1299c1fe2c84cbcdcd647fa3989c053744a339ba1f1ad109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947182"
---
# <a name="wysiwyg-display-and-output"></a>Visualización y salida de WYSIWYG

La mayoría de las aplicaciones intentan admitir la salida DE WYSIWYG (lo que ve es lo que obtiene). Esto significa que el texto dibujado con una fuente en negrita Helvetica de 10 puntos en la ventana de la aplicación debe tener una apariencia similar cuando se imprime. La obtención de una salida TRUE DE WYSIWYG es prácticamente imposible e incluso no deseada en la mayoría de los casos. Esto se debe, en parte, a las diferencias en las tecnologías de vídeo e impresora. un píxel en una pantalla suele ser mayor que un punto en una impresora de rayos. Las distancias de visualización también son diferentes; Normalmente, un usuario del equipo se encuentra a unos dos pies de la pantalla, pero los ojos de un lector suelen estar a un pie o menos de la página impresa.

Para compensar las diferencias de legibilidad entre las pantallas y la página impresa, el sistema admite una unidad denominada pulgada lógica que siempre se especifica en píxeles. Para una pantalla de vídeo, la pulgada lógica siempre es mayor que la pulgada física para compensar la distancia de visualización más larga y la resolución (generalmente) más gruesa. En el caso de las impresoras, la pulgada lógica siempre es igual a la pulgada física.

Para obtener un efecto WYSIWYG al dibujar texto, intervienen dos problemas relacionados: hacer que los caracteres individuales parezcan iguales y el diseño de página independiente del dispositivo. Para solucionar el primer problema, una aplicación puede usar la función [**CreateFont**](/windows/desktop/api/wingdi/nf-wingdi-createfonta) para especificar el nombre de fuente y el tamaño de una fuente ideal (o lógica) y, a continuación, llamar a la función [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para identificar el contexto del dispositivo de pantalla o impresora. Cuando la aplicación llama a **SelectObject** , el sistema selecciona una fuente física que es la coincidencia más cercana posible a la fuente lógica especificada. Cuando el sistema selecciona la fuente de presentación, elige una fuente física mayor que el tamaño real. Esto se produce debido a la pulgada lógica más grande en la pantalla. Sin embargo, desde la perspectiva del usuario, parece estar muy cerca del alto correcto. Cuando el sistema selecciona la fuente de la impresora, elige una fuente física que es realmente el tamaño solicitado. Para obtener más información sobre las fuentes y la salida de texto, vea [Fuentes y texto.](/windows/desktop/gdi/fonts-and-text)

El segundo problema, el del diseño de página independiente del dispositivo, se puede solucionar mediante el uso de métricas TrueType. Esto es así incluso cuando se mantiene la compatibilidad con versiones de 16 bits de Windows. Para obtener más información, vea [Using Portable TrueType Metrics](/windows/desktop/gdi/using-portable-truetype-metrics).

Para obtener un efecto WYSIWYG al dibujar gráficos con mapa de bits, una aplicación puede recuperar el ancho y el alto, en pulgadas lógicas, de la pantalla y la página impresa. Con estos valores, la aplicación puede crear factores de escalado horizontal y vertical para mantener la proporción de imágenes con mapa de bits cuando se dibujan en una impresora. Para obtener más información sobre los mapas de bits y la salida del mapa de bits, vea [Mapas de bits.](/windows/desktop/gdi/bitmaps)

 

 
