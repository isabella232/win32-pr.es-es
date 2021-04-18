---
description: La mayoría de las aplicaciones intentan admitir el resultado WYSIWYG (lo que se ve es lo que se obtiene).
ms.assetid: 34a1f37c-0fbf-451b-bb55-80ad85bcd4de
title: Presentación y salida de WYSIWYG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c03e4fa653c0d8e891cb079a7a7e7a003f9ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716794"
---
# <a name="wysiwyg-display-and-output"></a>Presentación y salida de WYSIWYG

La mayoría de las aplicaciones intentan admitir el resultado WYSIWYG (lo que se ve es lo que se obtiene). Esto significa que el texto dibujado con una fuente Helvetica Bold de 10 puntos en la ventana de la aplicación debe tener una apariencia similar cuando se imprime. Obtener una salida WYSIWYG verdadera es prácticamente imposible e incluso no deseable en la mayoría de los casos. Esto se debe, en parte, a las diferencias en las tecnologías de vídeo y de impresora. un píxel en una pantalla suele ser mayor que un punto en una impresora láser común. Las distancias de visualización también son diferentes; Normalmente, un usuario de un equipo se encuentra cerca de dos metros de la pantalla, pero los ojos de un lector suelen ser un pie o menos de la página impresa.

Para compensar las diferencias de legibilidad entre las pantallas y la página impresa, el sistema admite una unidad denominada pulgada lógica que siempre se especifica en píxeles. En el caso de una pantalla de vídeo, la pulgada lógica siempre es mayor que la pulgada física para compensar la distancia de visualización más larga y la resolución más gruesa (generalmente). En el caso de las impresoras, la pulgada lógica siempre es igual a la pulgada física.

Para obtener un efecto WYSIWYG al dibujar texto, se implican dos problemas relacionados: hacer que los caracteres individuales tengan el mismo aspecto y el diseño de página independiente del dispositivo. Para solucionar el primer problema, una aplicación puede usar la función [**CreateFont**](/windows/desktop/api/wingdi/nf-wingdi-createfonta) para especificar el nombre y el tamaño de la fuente de una fuente ideal (o lógica) y, a continuación, llamar a la función [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para identificar el contexto de dispositivo de impresora o pantalla. Cuando la aplicación llama a **SelectObject** , el sistema selecciona una fuente física que sea la coincidencia más cercana a la fuente lógica especificada. Cuando el sistema selecciona la fuente de visualización, elige una fuente física que es mayor que el tamaño real. Esto se debe a la pulgada lógica más grande de la pantalla. Sin embargo, desde el punto de vista del usuario, parece estar muy cerca del alto correcto. Cuando el sistema selecciona la fuente de la impresora, elige una fuente física que es realmente el tamaño solicitado. Para obtener más información sobre las fuentes y la salida de texto, vea [fuentes y texto](/windows/desktop/gdi/fonts-and-text).

El segundo problema, que es el diseño de página independiente del dispositivo, se puede resolver mediante el uso de métricas TrueType. Esto es así incluso cuando se mantiene la compatibilidad con las versiones de 16 bits de Windows. Para obtener más información, consulte [uso de métricas TrueType portátiles](/windows/desktop/gdi/using-portable-truetype-metrics).

Para obtener un efecto WYSIWYG al dibujar gráficos de mapa de imágenes, una aplicación puede recuperar el ancho y el alto, en pulgadas lógicas, de la pantalla y la página impresa. Con estos valores, la aplicación puede crear factores de escalado horizontal y vertical para mantener la proporción de imágenes de mapa de imagen cuando se dibujan en una impresora. Para obtener más información sobre los mapas de bits y la salida de mapas de bits, vea [mapas de bits](/windows/desktop/gdi/bitmaps).

 

 
