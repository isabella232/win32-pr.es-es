---
title: Implementación de Render
description: Implementación de Render
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- visualizaciones, eventos con tiempo
- visualizaciones personalizadas, eventos con tiempo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- visualizaciones, función RenderWindow
- visualizaciones personalizadas, función RenderWindow
- Render function,parameters
- Función RenderWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249632"
---
# <a name="implementing-render"></a>Implementación de Render

La manera más fácil de pensar en la programación de visualizaciones es crear un controlador para un evento con tiempo. A intervalos específicos, Reproductor de Windows Media toma una instantánea de los datos de audio que está reproduciendo y proporciona los datos de la instantánea a la visualización cargada actualmente. Esto es similar a la programación basada en eventos y forma parte del modelo de programación de Microsoft Windows. Escriba código y espere a que lo llame un evento determinado.

Si el código es una implementación de la función [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) para la representación en modo sin ventanas, recibe los parámetros siguientes:

*TimedLevel*

Se trata de una estructura que define los datos de audio que analizará el código. La estructura se compone de dos matrices. La primera matriz se basa en la información de frecuencia y contiene una instantánea del espectro de audio dividido en 1024 partes. Cada celda de la matriz contiene un valor de 0 a 255. La primera celda comienza a 20 Hz y la última a 22050 Hz. La matriz es bidimensional para representar audio estéreo. La segunda matriz se basa en la información de forma de onda y corresponde a la potencia de audio, donde cuanto más fuerte sea la onda, mayor será el valor. La matriz de formas de onda es una instantánea granular de los últimos 1024 segmentos de potencia de audio tomados a intervalos de tiempo muy pequeños. Esta matriz también es bidimensional para representar audio estéreo.

*HDC*

Se trata de un identificador Windows Microsoft para un contexto de dispositivo. Esto proporciona una manera de identificar la superficie de dibujo que se va a Windows. No es necesario crearlo, solo tiene que usarlo para llamadas de función de dibujo específicas.

*RECT*

Se trata de un rectángulo Windows microsoft que define el tamaño de una superficie de dibujo. Se trata de un rectángulo simple con cuatro propiedades: **izquierda,** **derecha,** **superior** e **inferior.** Los valores reales se proporcionan mediante Reproductor de Windows Media para que pueda determinar cómo el usuario o el desarrollador de máscaras ha dimensionado la ventana en la que va a dibujar. También determina la posición en el HDC en la que se supone que se representará el efecto.

Si el código es una implementación de la función **IWMPEffects2::RenderWindowed** para la representación en una ventana, recibe los parámetros siguientes:

*TimedLevel*

Se trata de la misma información que recibe **la función Render.**

*fRequiredRender*

El *parámetro fRequiredRender* le informa de que la visualización debe volver a dibujarse, por ejemplo, cuando se arrastra otra ventana sobre ella. Cuando este valor es false, puede omitir de forma segura el código de representación si el elemento multimedia actual está detenido o en pausa. Esto le permite evitar consumir ciclos de CPU innecesariamente.

El complemento de ejemplo generado por el Asistente para complementos no proporciona una implementación personalizada para **RenderWindowed.** En su lugar, el código de complemento de ejemplo recupera el contexto de dispositivo de la ventana primaria proporcionada por Reproductor de Windows Media en [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), recupera las dimensiones de la ventana primaria como una estructura RECT y, a continuación, llama a a **Render** mediante el contexto del dispositivo, el RECT y el puntero de nivel con tiempo de **RenderWindowed**.

En las secciones siguientes se proporciona más información sobre cómo implementar **Render**:

-   [Uso de niveles con tiempo](using-timed-levels.md)
-   [Uso de contextos de dispositivo](using-device-contexts.md)
-   [Usar rectángulos](using-rectangles.md)
-   [Ejemplo de código de representación](sample-render-code.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación del código**](implementing-your-code.md)
</dt> </dl>

 

 




