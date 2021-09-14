---
description: Ejemplo EVRPresenter
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Ejemplo EVRPresenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359741"
---
# <a name="evrpresenter-sample"></a>Ejemplo EVRPresenter

Muestra cómo implementar un presentador personalizado para [el representador de](enhanced-video-renderer.md) vídeo mejorado (EVR). El presentador personalizado se puede usar con el filtro DirectShow EVR o el Microsoft Media Foundation EVR.

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las Media Foundation siguientes:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a>Uso

El ejemplo EVRPresenter compila un archivo DLL que es un servidor COM para el presentador. Antes de usar el presentador personalizado, debe registrar el archivo DLL.

Para usar este ejemplo en Media Foundation:

1.  Compile el ejemplo.
2.  Regsvr32 EvrPresenter.dll.
3.  Compile y ejecute [el ejemplo MFPlayer](/previous-versions//bb970516(v=vs.85)).
4.  En el **menú** Archivo, seleccione **Abrir** archivo.
5.  En el **cuadro de diálogo** Abrir archivo, seleccione Custom **EVR Presenter (Presentador de EVR personalizado).**
6.  Seleccione un archivo para la reproducción.

Para usar este ejemplo en DirectShow:

1.  Compile el ejemplo.
2.  Registrar EvrPresenter.dll.
3.  Compile y ejecute el ejemplo EVRPlayer. Este ejemplo se incluye con los ejemplos DirectShow en el SDK de Windows.
4.  En el **menú** Archivo, seleccione **EvR Presenter**.
5.  Seleccione un archivo para la reproducción.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de github Windows ejemplos clásicos](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> <dt>

[Cómo escribir un presentador de EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
