---
title: Opciones de salida
description: Opciones de salida
ms.assetid: effe6c07-e6df-45b0-b865-2a025c466d6f
keywords:
- SDK de Windows Media Format, constantes globales
- Advanced Systems Format (ASF), constantes globales
- ASF (formato de sistemas avanzados), constantes globales
- constantes globales, lista de
- SDK de Windows Media Format, constantes
- Advanced Systems Format (ASF), constantes
- ASF (formato de sistemas avanzados), constantes
- constantes, lista de
- SDK de Windows Media Format, configuración de salida
- Advanced Systems Format (ASF), configuración de salida
- ASF (formato de sistemas avanzados), configuración de salida
- configuración de salida
- lectores sincrónicos, configuración de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5a02d508f76057dd72e34558a7ca8d29de4847
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149070"
---
# <a name="output-settings"></a>Opciones de salida

Las constantes globales siguientes se usan para identificar la configuración de salida del lector y el objeto de lector sincrónico.



| Constante global                | tipo de DataType del \_ atributo WMT \_  | Descripción de *pValue*                                                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszAllowInterlacedOutput    | **tipo de WMT \_ \_ bool**  | Si es true, el lector proporcionará fotogramas entrelazados, si lo admite la salida.                                                                                                                                                                                                                                            |
| g \_ wszDedicatedDeliveryThread  | **tipo de WMT \_ \_ bool**  | Si es true, esta salida tendrá un subproceso dedicado creado para la entrega de sus ejemplos. No se admite en el lector sincrónico.                                                                                                                                                                                            |
| g \_ wszDeliverOnReceive         | **tipo de WMT \_ \_ bool**  | Si es true, los ejemplos de esta salida se entregarán en cuanto estén disponibles desde el lector. Esto puede dar lugar a que los ejemplos de este resultado se entreguen de forma desordenada y antes de las muestras correspondientes de otras salidas.                                                                                            |
| g \_ wszDynamicRangeControl      | **tipo de WMT \_ \_ DWORD** | Especifica el nivel de control de intervalo dinámico que se va a utilizar para la salida. Se establece en un valor comprendido entre 0 y 2, donde 0 indica que no hay ningún control de intervalo dinámico (el valor predeterminado) y 2 es el nivel máximo de control de intervalo dinámico (el menor intervalo dinámico).                                                                                |
| g \_ wszEarlyDataDelivery        | **tipo de WMT \_ \_ DWORD** | Tiempo, en milisegundos, que especifica la cantidad anterior de entrega de los ejemplos. Si es mayor que cero, los ejemplos de esta salida se recuperarán y descodificarán para que los ejemplos se entreguen antes que los ejemplos de otras salidas. Normalmente, el lector entrega muestras en el orden del tiempo de presentación.         |
| g \_ wszEnableDiscreteOutput     | **tipo de WMT \_ \_ bool**  | Si es true, el lector habilitará la salida de audio multicanal de alta definición. Esta configuración solo es válida para las secuencias de audio codificadas con el códec Windows Media Audio 9 Professional. Si esta opción se establece en true, también debe especificar la configuración de los altavoces del equipo cliente estableciendo g \_ wszSpeakerConfig. |
| g \_ wszEnableFrameInterpolation | **tipo de WMT \_ \_ bool**  | Si es true, el códec entregará el flujo de vídeo a una [*velocidad de fotogramas*](wmformat-glossary.md)más alta, interpolando los fotogramas de forma algorítmica.                                                                                                                                                          |
| g \_ wszJustInTimeDecode         | **tipo de WMT \_ \_ bool**  | Si es true, los datos se deben descodificar lo más tarde posible. No se admite en el lector sincrónico.                                                                                                                                                                                                                            |
| g \_ wszNeedsPreviousSample      | **tipo de WMT \_ \_ bool**  | Si es true, el ejemplo requiere que se descomprime el ejemplo anterior. Esta configuración solo se aplica a los fotogramas Delta en vídeo comprimido y es de solo lectura.                                                                                                                                                                       |
| g \_ wszScrambledAudio           | **tipo de WMT \_ \_ bool**  | Si es true, esta salida usará el esquema de ocultación de errores de audio codificado. Esta es una configuración válida solo para salidas de audio.                                                                                                                                                                                                |
| g \_ wszSingleOutputBuffer       | **tipo de WMT \_ \_ bool**  | Si es true, se debe usar un único búfer de salida (por ejemplo, un búfer de vídeo® de DirectDraw). No se admite en el lector sincrónico.                                                                                                                                                                                           |
| g \_ wszSoftwareScaling          | **tipo de WMT \_ \_ bool**  | Si es false, el vídeo no se escala. (No debe haber ningún cambio en la resolución).                                                                                                                                                                                                                                                |
| g \_ wszSpeakerConfig            | **tipo de WMT \_ \_ DWORD** | Si la descodificación de audio multicanal está habilitada al establecer g \_ wszEnableDiscreteOutput, esta configuración especifica la configuración de los altavoces del equipo cliente. Establezca en una de las constantes de configuración de altavoces de DirectSound.                                                                                                   |
| g \_ wszStreamLanguage           | **tipo de la \_ \_ palabra WMT**  | Índice de la lista de idiomas del idioma que se va a entregar para esta salida. Se usa para las salidas que representan las secuencias mutuamente excluyentes por el lenguaje.                                                                                                                                                                      |
| g \_ wszVideoSampleDurations     | **tipo de WMT \_ \_ bool**  | Si es true, el lector proporcionará duraciones de ejemplo precisas.                                                                                                                                                                                                                                                                |
| g \_ wszEnableWMAProSPDIFOutput  | **tipo de WMT \_ \_ bool**  | Si es true, el lector incluirá el formato de interfaz digital de Sony/Phillips (S/PDIF) en los tipos de salida enumerados.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReaderAdvanced2::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getoutputsetting)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**IWMSyncReader::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputsetting)
</dt> <dt>

[**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting)
</dt> </dl>

 

 




