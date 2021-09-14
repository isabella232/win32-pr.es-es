---
description: Controlar una captura Graph
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controlar una captura Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00573256c1c010e23dfc598ceca5ac62d772711
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161575"
---
# <a name="controlling-a-capture-graph"></a>Controlar una captura Graph

La interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) de Filter Graph Manager tiene métodos para ejecutar, detener y pausar todo el gráfico. Sin embargo, si el gráfico de filtros tiene secuencias de captura y vista previa, es probable que quiera controlar las dos secuencias de forma independiente. Por ejemplo, es posible que quiera obtener una vista previa del vídeo sin capturarlo. Puede hacerlo mediante el método [**ICaptureGraphBuilder2::ControlStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream)

> [!Note]  
> Este método no funciona al capturar en un archivo de formato de sistemas avanzados (ASF).

 

Control del flujo de captura

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



El primer parámetro especifica qué flujo se va a controlar, como UN GUID de categoría de pin. El segundo parámetro proporciona el tipo de medio. El tercer parámetro es un puntero al filtro de captura. Para controlar todas las secuencias de captura del gráfico, establezca el segundo y tercer parámetro en **NULL.**

Los dos parámetros siguientes definen las horas a las que se iniciará y detendrá la secuencia, en relación con la hora en que el gráfico comienza a ejecutarse. Llame [**a IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para ejecutar el gráfico. Hasta que ejecute el gráfico, el **método ControlStream** no tiene ningún efecto. Si el gráfico ya se está ejecutando, la configuración se hace efectiva inmediatamente.

Los dos últimos parámetros se usan para obtener notificaciones de eventos cuando la secuencia se inicia y se detiene. Para cada secuencia que se controla mediante este método, el gráfico de filtros envía un par de eventos: [**EC \_ STREAM CONTROL \_ \_ STARTED**](ec-stream-control-started.md) cuando se inicia la secuencia y [**EC STREAM CONTROL \_ \_ \_ STOPPED**](ec-stream-control-stopped.md) cuando se detiene la secuencia. Los valores de **wStartCookie** y **wStopCookie** se usan como segundo parámetro de evento. Por lo tanto, *lParam2* en el evento de inicio es igual a **wStartCookie** y *lParam2* en el evento stop es igual a **wStopCookie**. El código siguiente muestra cómo obtener estos eventos:


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



El **método ControlStream** define algunos valores especiales para las horas de inicio y de detenerse.



| Value | Start                                  | Stop                               |
|-------------|----------------------------------------|---------|
| MAXLONGLONG | No inicie nunca esta secuencia.               | No se detenga hasta que se detenga el gráfico. |
| **NULL**    | Comience inmediatamente cuando se ejecute el gráfico. | Detenga inmediatamente.                  |



 

Por ejemplo, el código siguiente detiene la secuencia de captura inmediatamente:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



Aunque puede detener la secuencia de captura y reiniciarla más adelante, esto creará un intervalo en las marcas de tiempo. Durante la reproducción, el vídeo parecerá detendse durante la separación (en función del formato de archivo).

Controlar la secuencia de vista previa

Para controlar la marca de vista previa, llame **a ControlStream,** pero establezca el primer parámetro en PIN \_ CATEGORY \_ PREVIEW. Esto funciona igual que para PIN CATEGORY CAPTURE, salvo que no se pueden usar horas de referencia para especificar el inicio y la detenerse, porque los fotogramas de vista previa no tienen marcas \_ \_ de tiempo. Por lo tanto, debe **usar NULL** o MAXLONGLONG. Use **NULL para** iniciar la secuencia de vista previa:


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



No importa si la secuencia de vista previa procede de un pin de vista previa en el filtro de captura o del filtro Smart Tee. El **método ControlStream** funciona de cualquier manera.

Sin embargo, en el caso de los pins de puerto de vídeo, se producirá un error en el método. En ese caso, otro enfoque es ocultar la ventana de vídeo. Consulte el gráfico **para IVideoWindow** y use el método [**IVideoWindow::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) para mostrar u ocultar la ventana.


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



Además, si llama [**a IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con el valor OAFALSE antes de ejecutar el gráfico, el filtro Representador de vídeo oculta la ventana hasta que especifique lo contrario. De forma predeterminada, el representador de vídeo muestra la ventana al ejecutar el gráfico.

Comentarios sobre el control de flujo

El comportamiento predeterminado de un pin es entregar ejemplos cuando se ejecuta el gráfico. Por ejemplo, suponga que llama a **ControlStream** con PIN \_ CATEGORY CAPTURE pero no con PIN CATEGORY \_ \_ \_ PREVIEW. Al ejecutar el gráfico, la secuencia de vista previa se ejecutará inmediatamente, mientras que la secuencia de captura se ejecutará en el momento especificado en **ControlStream**.

Si va a capturar más de una secuencia y enviarla a un filtro mux (por ejemplo, si va a capturar audio y vídeo en un archivo AVI), debe controlar ambas secuencias conjuntamente. De lo contrario, el filtro mux podría bloquear la espera de una secuencia, ya que intenta intercalar las dos secuencias. Establezca las mismas horas de inicio y de detenerse en todas las secuencias de captura antes de ejecutar el gráfico:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



Internamente, el método **ControlStream** usa la interfaz [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) que se expone en los pines del filtro de captura, el filtro Smart Tee (si está presente) y, posiblemente, el filtro mux. Puede usar esta interfaz directamente, en lugar de llamar a **ControlStream**, aunque no hay ninguna ventaja concreta de hacerlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



