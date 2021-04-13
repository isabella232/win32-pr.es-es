---
title: Usar contextos de dispositivo
description: Usar contextos de dispositivo
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- visualizaciones, contexto de dispositivo
- visualizaciones personalizadas, contexto de dispositivo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función de representación, contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357237"
---
# <a name="using-device-contexts"></a>Usar contextos de dispositivo

El contexto de dispositivo es un identificador estándar de un contexto de dispositivo. Lo necesita para muchas funciones de dibujo para que Microsoft Windows sepa en qué ventana se debe dibujar. Por ejemplo, para dibujar un rectángulo, debe especificar el contexto del dispositivo.


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



Windows Media Player especifica el contexto del dispositivo a través de la función **Render** . Si el complemento se representa mediante una ventana, deberá usar el contexto de dispositivo de esa ventana. Use este contexto de dispositivo para cualquier herramienta de dibujo que requiera un contexto de dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de render**](implementing-render.md)
</dt> </dl>

 

 




