---
description: El descodificador de vídeo MPEG-2 es una Media Foundation que descodifica vídeo MPEG-1 y MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Descodificador de vídeo MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e2b270cadb114875fb63bc6c57ce2ddd63eecb2815b8fe3bcee175710d1771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012595"
---
# <a name="mpeg-2-video-decoder"></a>Descodificador de vídeo MPEG-2

El descodificador de vídeo MPEG-2 [es una transformación Media Foundation que](media-foundation-transforms.md) descodifica vídeo MPEG-1 y MPEG-2. El descodificador admite vídeo mpeg-2 de perfil simple y principal (H.262, ISO/IEC 13818-2) y vídeo MPEG-1 (ISO/IEC 11172-2).

## <a name="input-types"></a>Tipos de entrada

El descodificador admite los siguientes tipos de medios de entrada.

| Atributo                                                 | Descripción                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md) | **VÍDEO \_ MFMediaType**                                                  |
| [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ MPEG1**<br/> **MFVideoFormat \_ MPEG2**<br/> |



 

## <a name="output-types"></a>Tipos de salida

El descodificador admite los siguientes tipos de salida.

| Atributo                                                 | Descripción                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md) | **VÍDEO \_ MFMediaType**                                                                                                                                                         |
| [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ I420**<br/> **MFVideoFormat \_ IYUV**<br/> **MFVideoFormat \_ NV12**<br/> **MFVideoFormat \_ YUY2**<br/> **MFVideoFormat \_ YV12**<br/> |



 

## <a name="remarks"></a>Comentarios

El descodificador de vídeo MPEG-2 expone las interfaces siguientes:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

La entrada al descodificador debe ser una secuencia elemental. La resolución máxima admitida es de 1920 × 1088 píxeles.

El descodificador admite la aceleración de vídeo de DirectX (DXVA) mediante Microsoft Direct3D 9 o Microsoft Direct3D 11.

### <a name="special-decoding-modes"></a>Modos de decodificación especiales

-   **Modo de baja latencia.** Este modo es adecuado para escenarios como las comunicaciones en tiempo real. Reduce la latencia de inicio, por lo que el descodificador genera la primera muestra de salida antes. Sin embargo, el descodificador almacena en búfer menos muestras en este modo, lo que puede provocar problemas, ya que el descodificador no descodifica tantos fotogramas de antemano. Para habilitar el modo de baja latencia, establezca el [atributo CODECAPI \_ AVLowLatencyMode.](codecapi-avlowlatencymode.md)
-   **Buscando.** Para una búsqueda precisa, llame [**al método IMFTransform::SetOutputBounds.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) Cuando se llama a este método, el descodificador solo genera fotogramas que se encuentran dentro del intervalo de marcas de tiempo especificado por el autor de la llamada.
-   **Modo de generación de miniaturas**. Este modo está pensado para la generación rápida de imágenes en miniatura. En este modo, el descodificador descodifica inicialmente solo fotogramas I. Si no se encuentra ningún fotograma I dentro de un número determinado de fotogramas, el descodificador inicia la descodificación de fotogramas P y genera fotogramas distintos de I en un intervalo fijo (uno por *N* imágenes) hasta que se alcanza un fotograma I. Para habilitar el modo de generación de miniaturas, establezca la propiedad [CODECAPI \_ AVDecVideoThumbnailGenerationMode.](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   **Juego de trucos.** El descodificador puede descodificar a velocidades más rápidas que en tiempo real. Con velocidades de reproducción más altas, el descodificador pasará a descodificar solo fotogramas I. Para la reproducción inversa, solo se descodifican los fotogramas I.

### <a name="codec-properties"></a>Propiedades del códec

El descodificador admite las siguientes propiedades a través [**del método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)



| Propiedad                                                                                                      | Descripción                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | Habilita o deshabilita el modo de generación de miniaturas.                                                             |
| [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | Habilita o deshabilita lacodización acelerada de hardware.                                                         |
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Habilita o deshabilita el modo de baja latencia.                                                                      |
| [EL DESCODIFICADOR DE MFT \_ EXPONE LOS TIPOS DE SALIDA EN ORDEN \_ \_ \_ \_ \_ \_ NATIVO](mft-decoder-expose-output-types-in-native-order.md) | Especifica si el descodificador expone tipos de salida que son adecuados para la transcodificación antes que otros formatos. |



 

De estas propiedades, también se puede establecer lo siguiente a través de la [**interfaz ICodecAPI:**](/windows/win32/api/strmif/nn-strmif-icodecapi)

-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>Limitaciones

-   El descodificador no se admite en plataformas basadas en IA-64.
-   El descodificador no admite el descifrado css ni la reproducción de DVD cifrados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                       |
| Archivo DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
