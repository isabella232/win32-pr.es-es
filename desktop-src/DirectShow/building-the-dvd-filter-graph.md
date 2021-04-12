---
description: Creación del gráfico de filtros de DVD
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: Creación del gráfico de filtros de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d15c7d84ec138771e1f5da8be4270faae049cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152600"
---
# <a name="building-the-dvd-filter-graph"></a>Creación del gráfico de filtros de DVD

Al igual que con cualquier aplicación de DirectShow, una aplicación de reproducción de DVD se inicia mediante la creación de un gráfico de filtro. DirectShow proporciona los siguientes componentes para la reproducción de DVD:

-   [Generador de gráficos de DVD](dvd-graph-builder.md). Un objeto auxiliar que crea el gráfico de filtro. Expone la interfaz [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) .
-   Filtro del [navegador de DVD](dvd-navigator-filter.md) . Filtro DirectShow que controla la reproducción de DVD, la navegación y otros comandos.

La reproducción de DVD también requiere un descodificador MPEG-2. Los descodificadores MPEG-2 de hardware y software están disponibles en terceros. En primer lugar, cree una instancia del objeto del generador de gráficos de DVD.


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



En este momento, puede seleccionar y configurar el representador de vídeo antes de compilar el resto del gráfico. Este paso, que es opcional, se describe con más detalle en la sección siguiente. Si omite este paso, el generador de gráficos de DVD selecciona un representador predeterminado. A continuación, compile el gráfico llamando al método [**IDvdGraphBuilder:: RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) .


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



El primer parámetro es el nombre de un directorio que contiene los archivos de DVD. En un disco DVD, estos archivos se encuentran en un directorio llamado VIDEO \_ TS. Si el primer parámetro es **null**, el generador de gráficos de DVD utiliza la primera unidad que contiene un volumen de DVD.

El segundo parámetro contiene varias marcas opcionales para elegir el tipo de descodificador (hardware o software) y otras opciones.

El tercer parámetro es una [**estructura \_ \_ RENDERSTATUS de DVD AM**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) que recibe información de estado. Si el método [**RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) devuelve S \_ false, significa que la llamada se realizó parcialmente correctamente (o que se produjo un error parcial, si es un usuario pesimista). Por ejemplo, podría producirse un error en el método para representar la secuencia de subimagen, aunque el resto de las secuencias se representaran correctamente. Si el método **RenderDvdVideoVolume** devuelve un código de error o el valor S \_ false, puede examinar la estructura **AM \_ \_ RENDERSTATUS de DVD** para obtener más detalles sobre el error.

A continuación, obtenga un puntero al administrador de gráficos de filtro llamando a [**IDvdGraphBuilder:: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph). Este método devuelve un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del administrador de gráficos de filtro.


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



Use el método [**IDvdGraphBuilder:: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) para recuperar interfaces relacionadas con DVD, entre las que se incluyen las siguientes:

-   [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2). Controla los comandos de reproducción y DVD
-   [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2). Devuelve información sobre el estado actual del navegador de DVD.
-   [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder). Controla la presentación de subtítulos. La presentación de subtítulos cerrados está habilitada de forma predeterminada. Para deshabilitarlo, llame a [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) con la \_ marca AM L21 \_ CCSTATE \_ OFF.
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio). Controla el volumen y el equilibrio de audio.

Por ejemplo, el código siguiente devuelve la interfaz [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



La manera recomendada para generar el gráfico de filtro de reproducción de DVD es que un objeto de [generador de gráficos de DVD](dvd-graph-builder.md) lo haga automáticamente. Este enfoque se muestra a continuación y en la aplicación de ejemplo de DVD. Si necesita compilar el gráfico de filtros de DVD manualmente, puede hacerlo siguiendo las reglas básicas de creación de gráficos que se describen en otro lugar de la documentación de DirectShow. Por lo general, no debe agregar, quitar, conectar o desconectar de forma manual filtros individuales en el gráfico creado por el generador de gráficos de DVD, ya que esto puede confundir el código de limpieza.

Configuración del representador de vídeo

DirectShow proporciona varios filtros de representador de vídeo. Antes de compilar el gráfico, puede elegir el representador de vídeo que prefiera. Seleccione el representador mediante una llamada a [**IDvdGraphBuilder:: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) y solicite una interfaz específica para ese representador:

-   Filtro de mezclador de superposición: [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo).
-   Representador de mezcla de vídeo 7 (VMR-7): [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig).
-   Procesador de mezcla de vídeo 9 (VMR-9): [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9).
-   Representador de vídeo mejorado (EVR): [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig).

Si solicita cualquiera de estas interfaces antes de compilar el gráfico de filtros, el generador de gráficos de DVD crea el representador de vídeo correspondiente. Más adelante, al compilar el gráfico, el generador de gráficos de DVD intentará usar ese representador. Pero si no puede compilar el gráfico con el representador que ha seleccionado, puede cambiar a otro representador. Por ejemplo, es posible que el descodificador de MPEG-2 no sea compatible con el filtro VMR, en cuyo caso el generador de gráficos de DVD tendría como valor predeterminado el mezclador de superposición.

Estas interfaces también le ofrecen la oportunidad de configurar el representador antes de conectarse al descodificador. Por ejemplo, puede establecer la opción VMR para usar el modo sin ventanas en lugar del modo de ventana predeterminado. Para obtener más información acerca de los representadores de vídeo, consulte el tema [sobre la representación de vídeo en DirectShow](about-video-rendering-in-directshow.md).

En Windows XP y versiones posteriores, el generador de gráficos de DVD siempre usa el [representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7), a menos que:

-   El autor de la llamada consulta las interfaces que solo encontraron el [mezclador de superposición](overlay-mixer-filter.md), como [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). Esto envía una sugerencia al generador de gráficos de DVD que quiere que la aplicación use el mezclador de superposición y no la VMR. Windows Media Player también tiene una opción de cuadro de diálogo para forzar el uso del mezclador de superposición.
-   El descodificador instalado no es compatible con VMR. Durante la creación de gráficos, se usa la nueva interfaz [**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) para comprobar la compatibilidad de VMR del descodificador. Si no está presente, el generador de gráficos de DVD usará el mezclador de superposición.
-   Al utilizar un descodificador de hardware, el descodificador no puede conectarse al [Administrador de puertos de vídeo](video-port-manager.md) (VPM). Si un descodificador de hardware no puede usar VPM, no puede usar la VMR y, por tanto, el generador de gráficos de DVD intenta crear un gráfico con el mezclador de superposición.
-   Se sabe que la tarjeta de presentación tiene recursos o capacidades insuficientes para admitir la VMR, pero no informa correctamente de esto en el controlador. (Algunos casos conocidos están excluidos específicamente por el generador de gráficos de DVD).
-   La conexión entre el descodificador y el VMR produce un error por cualquier motivo, normalmente debido a una falta de VRAM para crear las superficies necesarias. En estos casos, el generador de gráficos de DVD desactiva el uso de VMR e intenta usar el mezclador de superposición para crear un gráfico.

Modo de ventana

En el modo de ventana (mezclador de superposición o VMR), el representador crea su propia ventana de vídeo. Para convertir esta ventana en un elemento secundario de la ventana de la aplicación, llame a [**IVideoWindow::p \_ propietario UT**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un identificador a la aplicación. Llame también a [**IVideoWindow::p UT \_ estiloVentana**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) para establecer los \_ estilos WS Child y WS \_ CLIPSIBLINGS en la ventana de vídeo del representador. Para obtener los mensajes del mouse desde la ventana de vídeo del representador, llame a [**IVideoWindow::p UT \_ MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) con un identificador a la ventana de la aplicación. Este método configura un "purga de mensajes": la ventana de vídeo reenvía los mensajes de mouse que recibe a la ventana de purga de mensajes.


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



La purga de mensajes hace que la selección de botones de menú de DVD sea algo complicada. Suponiendo que la ventana de vídeo no rellena el área de cliente completa de la aplicación, algunos eventos del mouse estarán fuera de la ventana de vídeo. Al obtener un evento del mouse desde la ventana de vídeo, debe procesarlo para la *navegación del menú* de DVD. No se deben procesar los eventos del mouse desde *fuera* de la ventana de vídeo. Con el consumo de mensajes, no hay forma de distinguir entre ambos. Además, las coordenadas de los eventos del mouse desde la ventana de vídeo son relativas al área cliente de la ventana de vídeo. pero los eventos del mouse desde fuera de la ventana de vídeo son relativos al área cliente de la aplicación.

Modo sin ventanas

El modo sin ventanas evita los problemas con los mensajes del mouse por completo. No necesita una purga de mensajes, porque VMR (o EVR) no crea su propia ventana en modo sin ventanas. En su lugar, dibuja directamente en la ventana de la aplicación. Si el rectángulo de destino es menor que el área de cliente de la aplicación, el navegador de DVD tiene esto en cuenta al calcular las posiciones de los botones de DVD. Por lo tanto, cuando reciba un mensaje del mouse, puede pasar las coordenadas directamente al navegador de DVD, tal como se describe en la sección navegación por el menú.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 
