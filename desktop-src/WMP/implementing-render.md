---
title: Implementación de render
description: Implementación de render
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- visualizaciones, eventos con tiempo
- visualizaciones personalizadas, eventos con tiempo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- visualizaciones, función RenderWindow
- visualizaciones personalizadas, función RenderWindow
- Función render, parámetros
- RenderWindow función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077321"
---
# <a name="implementing-render"></a>Implementación de render

La forma más sencilla de pensar en la programación de la visualización es que está creando un controlador para un evento con hora. A intervalos específicos, Windows Media Player toma una instantánea de los datos de audio que se reproducen y proporciona los datos de la instantánea a la visualización cargada actualmente. Esto es similar a la programación controlada por eventos y forma parte del modelo de programación de Microsoft Windows. Escribirá código y esperará a que lo llame un evento determinado.

Si el código es una implementación de la función [IWMPEffects:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) para la representación en modo sin ventanas, recibe los parámetros siguientes:

*TimedLevel*

Se trata de una estructura que define los datos de audio que el código va a analizar. La estructura se compone de dos matrices. La primera matriz se basa en la información de frecuencia y contiene una instantánea del espectro de audio dividida en porciones de 1024. Cada celda de la matriz contiene un valor comprendido entre 0 y 255. La primera celda comienza en 20 Hz y en el último 22050 Hz. La matriz es bidimensional para representar audio estéreo. La segunda matriz se basa en la información de la forma de onda y se corresponde con la potencia de audio, donde la onda más fuerte es, cuanto mayor sea el valor. La matriz de la forma de onda es una instantánea granular de los últimos 1024 segmentos de energía de audio tomados en intervalos de tiempo muy pequeños. Esta matriz también es bidimensional para representar audio estéreo.

*CÁMARAS*

Se trata de un identificador de Microsoft Windows para un contexto de dispositivo. Esto proporciona una manera de identificar la superficie de dibujo en Windows. No es necesario crearlo, solo tiene que usarlo para llamadas específicas de funciones de dibujo.

*RECT*

Se trata de un rectángulo de Microsoft Windows que define el tamaño de una superficie de dibujo. Se trata de un rectángulo sencillo con cuatro propiedades: **izquierda**, **derecha**, **superior** e **inferior**. Los valores reales son proporcionados por Windows Media Player para que pueda determinar cómo el usuario o el desarrollador de máscaras ha ajustado el tamaño de la ventana en la que se va a dibujar. También determina la posición en la HDC en la que se supone que se debe representar el efecto.

Si el código es una implementación de la función **IWMPEffects2:: RenderWindowed** para la representación en una ventana, recibe los parámetros siguientes:

*TimedLevel*

Esta es la misma información que recibe la función de **representación** .

*fRequiredRender*

El parámetro *fRequiredRender* le informa de que la visualización debe volver a dibujarse, por ejemplo, cuando se arrastra otra ventana sobre ella. Cuando este valor es false, puede omitir el código de representación de forma segura si el elemento multimedia actual está detenido o en pausa. Esto le permite evitar consumir ciclos de CPU innecesariamente.

El complemento de ejemplo generado por el Asistente para complementos no proporciona una implementación personalizada para **RenderWindowed**. En su lugar, el código de complemento de ejemplo recupera el contexto de dispositivo de la ventana primaria proporcionada por Windows Media Player en [IWMPEffects2:: Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), recupera las dimensiones de la ventana primaria como una estructura Rect y, a continuación, llama a a través de para **representar** mediante el contexto de dispositivo, el Rect y el puntero de nivel de tiempo de **RenderWindowed**.

En las secciones siguientes se proporciona más información acerca de la implementación de **Render**:

-   [Usar niveles de tiempo](using-timed-levels.md)
-   [Usar contextos de dispositivo](using-device-contexts.md)
-   [Usar rectángulos](using-rectangles.md)
-   [Código de representación de ejemplo](sample-render-code.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar el código**](implementing-your-code.md)
</dt> </dl>

 

 




