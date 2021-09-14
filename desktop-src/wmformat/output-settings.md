---
title: Opciones de salida
description: Opciones de salida
ms.assetid: effe6c07-e6df-45b0-b865-2a025c466d6f
keywords:
- Windows SDK de formato multimedia, constantes globales
- Formato de sistemas avanzados (ASF), constantes globales
- ASF (formato de sistemas avanzados), constantes globales
- constantes globales, lista de
- Windows SDK de formato multimedia, constantes
- Formato de sistemas avanzados (ASF),constantes
- ASF (formato de sistemas avanzados),constantes
- constants,list of
- Windows SDK de formato multimedia, configuración de salida
- Formato de sistemas avanzados (ASF), configuración de salida
- ASF (formato de sistemas avanzados), configuración de salida
- configuración de salida
- lectores sincrónicos, configuración de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5a02d508f76057dd72e34558a7ca8d29de4847
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266956"
---
# <a name="output-settings"></a>Opciones de salida

Las siguientes constantes globales se usan para identificar la configuración de salida para el lector y el objeto de lector sincrónico.



| Constante global                | TIPO DE \_ DATOS ATTR DE WMT \_  | Descripción de *pValue*                                                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszAllowInterlacedOutput    | **TIPO WMT \_ \_ BOOL**  | Si es True, el lector entregará fotogramas entrelazados, si es compatible con la salida.                                                                                                                                                                                                                                            |
| g \_ wszDedicatedDeliveryThread  | **TIPO WMT \_ \_ BOOL**  | Si es True, esta salida tendrá un subproceso dedicado creado para la entrega de sus ejemplos. No se admite en el lector sincrónico.                                                                                                                                                                                            |
| g \_ wszDeliverOnReceive         | **TIPO WMT \_ \_ BOOL**  | Si es True, los ejemplos de esta salida se entregarán en cuanto estén disponibles en el lector. Esto puede dar lugar a que las muestras de esta salida se entreguen fuera de orden y antes de las muestras correspondientes de otras salidas.                                                                                            |
| g \_ wszDynamicRangeControl      | **DWORD \_ DE TIPO \_ WMT** | Especifica el nivel de control de intervalo dinámico que se va a usar para la salida. Establezca en un valor de 0 a 2, donde 0 indica que no hay control de intervalo dinámico (valor predeterminado) y 2 es el nivel máximo del control de intervalo dinámico (el intervalo dinámico más pequeño).                                                                                |
| g \_ wszEarlyDataDelivery        | **DWORD \_ DE TIPO \_ WMT** | Tiempo, en milisegundos, que especifica cuánto antes se deben entregar las muestras. Si es mayor que cero, las muestras de esta salida se recuperarán y descodificarán para que las muestras se entreguen antes que las muestras para otras salidas. Normalmente, el lector entrega muestras en orden de tiempo de presentación.         |
| g \_ wszEnableDiscreteOutput     | **TIPO WMT \_ \_ BOOL**  | Si es True, el lector habilitará la salida de audio multicanal de alta definición. Esta configuración solo es válida para las secuencias de audio codificadas con el códec Windows Media Audio 9 Professional formato. Si esta opción se establece en true, también debe especificar la configuración del hablante del equipo cliente estableciendo g \_ wszSpeakerConfig. |
| g \_ wszEnableFrameInterpolation | **TIPO WMT \_ \_ BOOL**  | Si es True, el códec entregará la secuencia de vídeo a una velocidad de fotogramas [*mayor,*](wmformat-glossary.md)interpolando los fotogramas de forma algorítmica.                                                                                                                                                          |
| g \_ wszJustInTimeDecode         | **TIPO WMT \_ \_ BOOL**  | Si es True, los datos se deben descodificar lo más tarde posible. No se admite en el lector sincrónico.                                                                                                                                                                                                                            |
| g \_ wszNeedsPreviousSample      | **TIPO WMT \_ \_ BOOL**  | Si es true, el ejemplo requiere que se descomprima el ejemplo anterior. Esta configuración solo se aplica a los fotogramas delta en vídeo comprimido y es de solo lectura.                                                                                                                                                                       |
| g \_ wszScrambledAudio           | **TIPO WMT \_ \_ BOOL**  | Si es True, esta salida usará el esquema de ocultación de errores de audio codificado. Se trata de una configuración válida solo para las salidas de audio.                                                                                                                                                                                                |
| g \_ wszSingleOutputBuffer       | **TIPO WMT \_ \_ BOOL**  | Si es True, se debe usar un búfer de salida único (por ejemplo, un búfer de vídeo ® DirectDraw). No se admite en el lector sincrónico.                                                                                                                                                                                           |
| g \_ wszSoftwareScaling          | **TIPO WMT \_ \_ BOOL**  | Si es False, el vídeo no se escala. (No debe haber ningún cambio en la resolución).                                                                                                                                                                                                                                                |
| g \_ wszSpeakerConfig            | **DWORD \_ DE TIPO \_ WMT** | Si la descodación de audio multicanal está habilitada estableciendo g wszEnableDiscreteOutput, esta configuración especifica la configuración del hablante \_ del equipo cliente. Establezca en una de las constantes de configuración del altavoz DirectSound.                                                                                                   |
| g \_ wszStreamLanguage           | **PALABRA DE \_ TIPO \_ WMT**  | Índice de la lista de idioma del idioma que se va a entregar para esta salida. Se usa para las salidas que representan secuencias mutuamente excluyentes por idioma.                                                                                                                                                                      |
| g \_ wszVideoSampleDurations     | **TIPO WMT \_ \_ BOOL**  | Si es True, el lector entregará duraciones de muestra precisas.                                                                                                                                                                                                                                                                |
| g \_ wszEnableWMAProSPDIFOutput  | **TIPO WMT \_ \_ BOOL**  | Si es True, el lector incluirá el formato de interfaz digital (S/PDIF) de Sony/Phillips en los tipos de salida enumerados.                                                                                                                                                                                                       |



 

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

 

 




