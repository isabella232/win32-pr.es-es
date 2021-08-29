---
title: Uso de contextos de dispositivo
description: Uso de contextos de dispositivo
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- visualizaciones, contexto de dispositivo
- visualizaciones personalizadas, contexto de dispositivo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función de representación, contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e07247de9496cd0221b6031e65c0f68def0bade8ce1c814c5096daff486098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507155"
---
# <a name="using-device-contexts"></a>Uso de contextos de dispositivo

El contexto del dispositivo es un identificador estándar para un contexto de dispositivo. Necesita esto para muchas funciones de dibujo para que Microsoft Windows la ventana en la que dibujar. Por ejemplo, para dibujar un rectángulo, debe especificar el contexto del dispositivo.


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



El contexto del dispositivo se especifica mediante Reproductor de Windows Media a través de la **función Render.** Si el complemento se representa mediante una ventana, deberá usar el contexto de dispositivo de esa ventana. Use este contexto de dispositivo para cualquier herramienta de dibujo que requiera un contexto de dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de Render**](implementing-render.md)
</dt> </dl>

 

 




