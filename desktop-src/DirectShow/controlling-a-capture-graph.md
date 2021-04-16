---
description: Controlar un gráfico de captura
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controlar un gráfico de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6366645f14822a770b828e59b2201e378a0e1e8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537677"
---
# <a name="controlling-a-capture-graph"></a>Controlar un gráfico de captura

La interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) del administrador de gráficos de filtro tiene métodos para ejecutar, detener y pausar todo el gráfico. Sin embargo, si el gráfico de filtros tiene secuencias de captura y vista previa, es probable que desee controlar los dos flujos de forma independiente. Por ejemplo, puede que desee obtener una vista previa del vídeo sin capturarlo. Puede hacerlo a través del método [**ICaptureGraphBuilder2:: ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) .

> [!Note]  
> Este método no funciona al capturar en un archivo de formato de sistema avanzado (ASF).

 

Controlar el flujo de captura

El código siguiente establece la secuencia de captura de vídeo para que se ejecute durante cuatro segundos, empezando un segundo después de que se ejecute el gráfico:


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



El primer parámetro especifica la secuencia que se va a controlar, como un GUID de categoría de PIN. El segundo parámetro proporciona el tipo de medio. El tercer parámetro es un puntero al filtro de captura. Para controlar todas las secuencias de captura en el gráfico, establezca el segundo y el tercer parámetro en **null**.

Los dos parámetros siguientes definen las horas en que se iniciará y detendrá la secuencia, en relación con la hora a la que se inicia la ejecución del gráfico. Llame a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para ejecutar el gráfico. Hasta que se ejecute el gráfico, el método **ControlStream** no tiene ningún efecto. Si el gráfico ya se está ejecutando, la configuración surte efecto inmediatamente.

Los dos últimos parámetros se usan para obtener notificaciones de eventos cuando el flujo se inicia y se detiene. Para cada secuencia que controla mediante este método, el gráfico de filtros envía un par de eventos: el [**control de secuencia de EC se \_ \_ \_ inicia**](ec-stream-control-started.md) cuando se inicia el flujo y el [**control de secuencia de EC se \_ \_ \_ detiene**](ec-stream-control-stopped.md) cuando se detiene la secuencia. Los valores de **wStartCookie** y **wStopCookie** se usan como el segundo parámetro de evento. Por lo tanto, *lParam2* en el evento Start es igual a **wStartCookie** y *lParam2* en el evento STOP es igual a **wStopCookie**. En el código siguiente se muestra cómo obtener estos eventos:


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



El método **ControlStream** define algunos valores especiales para las horas de inicio y detención.



|             |                                        |                                    |
|-------------|----------------------------------------|------------------------------------|
|             | Start                                  | Stop                               |
| MAXLONGLONG | Nunca inicie esta secuencia.               | No se detenga hasta que el gráfico se detenga. |
| **NULL**    | Iniciar inmediatamente cuando se ejecuta el gráfico. | Detener inmediatamente.                  |



 

Por ejemplo, el código siguiente detiene inmediatamente el flujo de captura:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



Aunque puede detener el flujo de captura y reiniciarlo más adelante, se creará una brecha en las marcas de tiempo. En la reproducción, el vídeo parecerá que se detiene durante el intervalo (en función del formato de archivo).

Controlar la secuencia de vista previa

Para controlar el PIN de vista previa, llame a **ControlStream** , pero establezca el primer parámetro en la \_ versión preliminar de la categoría PIN \_ . Esto funciona igual que en \_ la captura de categoría de PIN \_ , salvo que no se pueden utilizar tiempos de referencia para especificar el inicio y la detención, ya que los marcos de vista previa no tienen marcas de tiempo. Por lo tanto, debe usar **null** o MAXLONGLONG. Use **null** para iniciar la secuencia de vista previa:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



Use MAXLONGLONG para detener la secuencia de vista previa:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



No importa si la secuencia de vista previa proviene de un PIN de vista previa en el filtro de captura o del filtro de forma inteligente. El método **ControlStream** funciona de cualquier manera.

En el caso de los PIN del puerto de vídeo, el método producirá un error. En ese caso, otro enfoque consiste en ocultar la ventana de vídeo. Consulte el gráfico para **IVideoWindow** y use el método [**\_ visible IVideoWindow::p UT**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) para mostrar u ocultar la ventana.


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



Además, si llama a [**IVideoWindow::p UT \_ Autoshow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con el valor OAFALSE antes de ejecutar el gráfico, el filtro de representador de vídeo oculta la ventana hasta que especifique lo contrario. De forma predeterminada, el representador de vídeo muestra la ventana cuando se ejecuta el gráfico.

Comentarios sobre el control de secuencias

El comportamiento predeterminado de un PIN es ofrecer ejemplos cuando se ejecuta el grafo. Por ejemplo, supongamos que llama a **ControlStream** con la captura de categoría de PIN, \_ \_ pero no con la \_ versión preliminar de categoría de PIN \_ . Al ejecutar el gráfico, la secuencia de vista previa se ejecutará inmediatamente, mientras que la secuencia de captura se ejecutará en cualquier momento que se especifique en **ControlStream**.

Si está capturando más de una secuencia y las envía a un filtro MUX (por ejemplo, si va a capturar audio y vídeo en un archivo AVI), debe controlar ambos flujos en tándem. De lo contrario, el filtro MUX podría bloquear la espera de un flujo, ya que intenta intercalar las dos secuencias. Establezca las mismas horas de inicio y detención en todas las secuencias de captura antes de ejecutar el gráfico:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



Internamente, el método **ControlStream** usa la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , que se expone en las clavijas del filtro de captura, el filtro Smart Tee (si existe) y, posiblemente, el filtro Mux. Puede usar esta interfaz directamente, en lugar de llamar a **ControlStream**, aunque no hay ninguna ventaja concreta para hacerlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



