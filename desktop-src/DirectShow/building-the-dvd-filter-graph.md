---
description: Creación del filtro de DVD Graph
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: Creación del filtro de DVD Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049c8bc52fd382be863cdf5a0e6b124534e0b9280d28536abc58a6f4e64e81e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662658"
---
# <a name="building-the-dvd-filter-graph"></a>Creación del filtro de DVD Graph

Al igual que con cualquier DirectShow, una aplicación de reproducción de DVD comienza mediante la creación de un gráfico de filtro. DirectShow proporciona los siguientes componentes para la reproducción de DVD:

-   [DVD Graph Builder](dvd-graph-builder.md). Objeto auxiliar que construye el gráfico de filtro. Expone la interfaz [**IDvdGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)
-   [Filtro DVD Navigator.](dvd-navigator-filter.md) Filtro DirectShow que controla la reproducción de DVD, la navegación y otros comandos.

La reproducción de DVD también requiere un descodificador MPEG-2. Los descodificadores MPEG-2 de hardware y software están disponibles de terceros. En primer lugar, cree una instancia del objeto DVD Graph Builder.


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



En este momento, puede seleccionar y configurar el representador de vídeo antes de compilar el resto del gráfico. Este paso, que es opcional, se describe con más detalle en la sección siguiente. Si omite este paso, el generador Graph DVD selecciona un representador predeterminado. A continuación, compile el gráfico mediante una llamada [**al método IDvdGraphBuilder::RenderDvdVideoVolume.**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume)


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



El primer parámetro es el nombre de un directorio que contiene los archivos DVD. En un disco de DVD, estos archivos residen en un directorio denominado VIDEO \_ TS. Si el primer parámetro es **NULL,** el dvd Graph Builder usa la primera unidad que contiene un volumen de DVD.

El segundo parámetro contiene varias marcas opcionales para elegir el tipo de descodificador (hardware o software) y otras opciones.

El tercer parámetro es una estructura [**\_ \_ RENDERSTATUS de DVD de AM**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) que recibe información de estado. Si el [**método RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) devuelve S FALSE, significa que la llamada se ha producido parcialmente correctamente (o se ha producido un error parcial, si es \_ pesimista). Por ejemplo, es posible que el método no represente la secuencia de subaspección, aunque las demás secuencias se representen correctamente. Si el **método RenderDvdVideoVolume** devuelve un código de error o el valor S FALSE, puede examinar la estructura \_ **\_ \_ RENDERSTATUS** del DVD de AM para obtener detalles sobre el error.

A continuación, obtenga un puntero al Administrador de Graph mediante una llamada [**a IDvdGraphBuilder::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph). Este método devuelve un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) Graph Filter manager.


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



Use el [**método IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) para recuperar interfaces relacionadas con DVD, incluidas las siguientes:

-   [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2). Controles de reproducción y comandos de DVD
-   [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2). Devuelve información sobre el estado actual del navegador de DVD.
-   [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder). Controla la presentación de subtítulos. La presentación de subtítulos está habilitada de forma predeterminada. Para deshabilitarlo, llame a [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) con la marca \_ AM L21 \_ CCSTATE \_ Off.
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio). Controla el volumen y el equilibrio de audio.

Por ejemplo, el código siguiente devuelve la [**interfaz IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



La manera recomendada de crear el gráfico de filtros de reproducción de DVD es hacer que un objeto [DVD Graph Builder](dvd-graph-builder.md) lo haga automáticamente. Este enfoque se muestra a continuación y en la aplicación de ejemplo de DVD. Si necesita compilar manualmente el gráfico de filtros de DVD, puede hacerlo siguiendo las reglas básicas de compilación de grafos que se deba a otra parte en la documentación DirectShow datos. Por lo general, no debe agregar, quitar, conectar ni desconectar manualmente filtros individuales en el gráfico creado por DVD Graph Builder, ya que si lo hace, podría confundir el código de limpieza.

Configuración del representador de vídeo

DirectShow proporciona varios filtros de representador de vídeo. Antes de compilar el gráfico, puede elegir el representador de vídeo que prefiera. Seleccione el representador llamando a [**IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) y solicitando una interfaz específica para ese representador:

-   Overlay Mixer Filter: [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo).
-   Representador de mezcla de vídeo 7 (VMR-7): [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig).
-   Representador de mezcla de vídeo 9 (VMR-9): [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9).
-   Representador de vídeo mejorado (EVR): [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig).

Si solicita cualquiera de estas interfaces antes de compilar el gráfico de filtros, el generador de DVD Graph Builder crea el representador de vídeo correspondiente. Más adelante, al compilar el gráfico, el generador Graph DVD intentará usar ese representador. Pero si no puede compilar el gráfico con el representador seleccionado, puede cambiar a otro representador. Por ejemplo, es posible que el descodificador MPEG-2 no sea compatible con el filtro VMR, en cuyo caso dvd Graph Builder tendría como valor predeterminado el valor predeterminado de Overlay Mixer.

Estas interfaces también le dan la oportunidad de configurar el representador antes de conectarse al descodificador. Por ejemplo, puede establecer el VMR para que use el modo sin ventanas en lugar del modo de ventana predeterminado. Para obtener más información sobre los representadores de vídeo, vea el tema Acerca de [la representación de vídeo en DirectShow](about-video-rendering-in-directshow.md).

En Windows XP y versiones posteriores, DVD Graph Builder siempre usa el representador de mezcla de vídeo [7](video-mixing-renderer-filter-7.md) (VMR-7), a menos que:

-   El autor de la llamada consulta las interfaces que solo encontraron el Mixer [,](overlay-mixer-filter.md)como [**IMixerPinConfig2.**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) Esto envía una sugerencia a DVD Graph Builder de que la aplicación quiere usar el archivo Overlay Mixer y no vmr. Reproductor de Windows Media tiene también una opción de cuadro de diálogo para forzar el uso de La superposición Mixer.
-   El descodificador instalado no es compatible con VMR. Durante la creación del grafo, se usa la nueva interfaz [**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) para comprobar la compatibilidad con VMR del descodificador. Si no está presente, el generador de Graph DVD usará el cuadro de diálogo Superposición Mixer.
-   Mientras se usa un descodificador de hardware, el descodificador no se puede conectar al [Administrador de puertos de](video-port-manager.md) vídeo (VPM). Si un descodificador de hardware no puede usar el VPM, no puede usar el VMR y, por tanto, el generador de DVD Graph intenta crear un gráfico mediante el comando Overlay Mixer.
-   Se sabe que la tarjeta de presentación no tiene recursos o capacidades suficientes para admitir vmr, pero no lo informa correctamente en el controlador. (Algunos casos conocidos se excluyen específicamente mediante DVD Graph Builder).
-   La conexión entre el descodificador y el VMR produce un error por cualquier motivo, normalmente debido a la falta de VRAM para crear las superficies necesarias. En estos casos, dvd Graph Builder desactiva el uso de VMR e intenta usar el Mixer superposición para crear un gráfico.

Modo de ventana

En el modo de ventana (Mixer o VMR), el representador crea su propia ventana de vídeo. Para convertir esta ventana en un elemento secundario de la ventana de la aplicación, llame a [**IVideoWindow::p ut \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un identificador para la aplicación. Llame también [**a IVideoWindow::p ut \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) para establecer los estilos WS CHILD y \_ WS CLIPSIBLINGS en la ventana de \_ vídeo del representador. Para obtener mensajes del mouse desde la ventana de vídeo del representador, llame a [**IVideoWindow::p ut \_ MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) con un identificador para la ventana de la aplicación. Este método configura una "purga de mensajes": la ventana de vídeo reenvía los mensajes del mouse que recibe a la ventana de purga de mensajes.


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



La purga de mensajes hace que la selección de botones de menú de DVD sea algo complicada. Suponiendo que la ventana de vídeo no llena todo el área de cliente de la aplicación, algunos eventos del mouse estarán fuera de la ventana de vídeo. Al obtener un evento del mouse desde dentro *de la* ventana de vídeo, debe procesarlo para la navegación del menú DVD. No se deben *procesar los eventos* del mouse desde fuera de la ventana de vídeo. Con la purga del mensaje, no hay ninguna manera de distinguir entre los dos. Además, las coordenadas de los eventos del mouse de la ventana de vídeo son relativas al área cliente de la ventana de vídeo. pero los eventos del mouse desde fuera de la ventana de vídeo son relativos al área de cliente de la aplicación.

Modo sin ventanas

El modo sin ventana evita por completo los problemas con los mensajes del mouse. No necesita una purga de mensajes, ya que el VMR (o EVR) no crea su propia ventana en modo sin ventanas. En su lugar, se dibuja directamente en la ventana de la aplicación. Si el rectángulo de destino es menor que el área de cliente de la aplicación, el navegador de DVD lo tiene en cuenta al calcular las posiciones del botón de DVD. Por lo tanto, cuando recibe un mensaje del mouse, puede pasar las coordenadas directamente al navegador de DVD, como se describe en la sección Navegación por menús.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 
