---
title: Escribir flujos con píxeles no cuadrados
description: Escribir flujos con píxeles no cuadrados
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- SDK de Windows Media Format, escribir secuencias de vídeo
- SDK de Windows Media Format, secuencias de vídeo
- SDK de Windows Media Format, píxeles no cuadrados
- Windows Media Format SDK, píxeles (no cuadrado)
- Advanced Systems Format (ASF), escribir secuencias de vídeo
- ASF (formato de sistemas avanzados), escribir secuencias de vídeo
- Advanced Systems Format (ASF), secuencias de vídeo
- ASF (formato de sistemas avanzados), secuencias de vídeo
- Advanced Systems Format (ASF), píxeles no cuadrados
- ASF (formato de sistemas avanzados), píxeles no cuadrados
- Advanced Systems Format (ASF), píxeles (no cuadrados)
- ASF (formato de sistemas avanzados), píxeles (no cuadrados)
- escribir secuencias de vídeo
- secuencias de vídeo, escritura
- secuencias de vídeo, píxeles no cuadrados
- píxeles no cuadrados
- píxeles (no cuadrados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077309"
---
# <a name="writing-streams-with-non-square-pixels"></a>Escribir flujos con píxeles no cuadrados

Hay dos formas de crear secuencias de vídeo con píxeles no cuadrados que se mostrarán correctamente en Windows Media Player. La primera técnica implica establecer los atributos de nivel de flujo en el encabezado del archivo. La segunda técnica implica agregar una extensión de unidad de datos a una secuencia en el perfil y, a continuación, establecer un valor para ella en cada ejemplo que se escribe.

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a>Para usar los atributos de encabezado de nivel de secuencia para establecer la relación de aspecto de píxeles

1.  Configure el objeto de escritor. Para obtener más información, consulte [Writing ASF files](writing-asf-files.md).
2.  Cree o cargue un perfil con una o varias secuencias de vídeo. Para obtener más información, vea [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md).
3.  Llame a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). (Llame siempre a este método antes de establecer los atributos de encabezado).
4.  Llame a **QueryInterface** para obtener la interfaz [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) y llame al método [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) dos veces para agregar [**AspectRatioX**](aspectratiox.md) y [**AspectRatioY**](aspectratioy.md) como atributos de nivel de secuencia de la secuencia de vídeo. Estos atributos son valores **DWORD** .
5.  Escriba el archivo.

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a>Para usar las extensiones de unidad de datos para establecer la relación de aspecto de píxeles

**Antes de escribir:**

1.  Configure el objeto de escritor. Para obtener más información, consulte [Writing ASF files](writing-asf-files.md).
2.  Cree o cargue un perfil con una o varias secuencias de vídeo. Para obtener más información, vea [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md).
3.  Para cada secuencia (de cualquier tipo de medio) del perfil, llame a [**IWMStreamConfig:: SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) para especificar un nombre único de su elección. No asigne a dos secuencias el mismo nombre.
4.  Use [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) en el flujo de vídeo para agregar una extensión de unidad de datos para la relación de aspecto de píxeles.
5.  Llame a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).
6.  Escriba el archivo.

**Al escribir:**

-   Para cada ejemplo, llame a [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) y especifique la \_ propiedad WM SampleExtensionGUID \_ PixelAspectRatio junto con el valor correcto. Los valores de relación de aspecto se escriben como dos valores concatenados de dos dígitos. Por ejemplo, 16:9 se escribe como 1609 o 0x0649. Siempre es un valor de 2 bytes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Para leer y escribir secuencias de vídeo con píxeles no cuadrados**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




