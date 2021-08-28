---
description: El descodificador Windows Media Video 9 descodifica secuencias de vídeo codificadas por Windows Media Video Encoder.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Descodificador de Vídeo multimedia 9 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df973e78f69e1f1ff0e649b2c4f5637380be9f27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474311"
---
# <a name="windows-media-video-9-decoder"></a>Windows Descodificador de Vídeo multimedia 9

El descodificador Windows Media Video 9 descodifica las secuencias de vídeo codificadas por Windows [**Media Video Encoder**](windowsmediavideo9encoder.md). El codificador y el descodificador admiten las cuatro categorías siguientes de vídeo codificado.

-   Windows Perfil simple de Media Video 9
-   Windows Perfil principal de Vídeo multimedia 9
-   Windows Perfil avanzado de Media Video 9
-   Windows Imagen de Vídeo multimedia 9.1

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador Windows Media Video se representa mediante la constante **CLSID \_ CWMVDecMediaObject**. Puede crear una instancia del descodificador de vídeo llamando a **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objeto descodificador de vídeo expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como objeto multimedia directX (DMO) y expone la interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un descodificador de vídeo se comporta como un DMO o un MFT en función de las interfaces que obtenga y la versión de Windows se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador de vídeo se comporta DMO o MFT.



| Sistema operativo            | Comportamiento del descodificador                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un Windows de vídeo multimedia siempre se comporta como un DMO.                                                                                                                |
| Windows Vista y Windows 7 | De forma predeterminada, un descodificador Windows vídeo multimedia se comporta como un DMO. Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un descodificador de vídeo, se comporta como un MFT. |



 

A partir Windows 7, el descodificador Windows Media Video implementa la [**interfaz IDMOQualityControl.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol)

## <a name="input-formats"></a>Formatos de entrada

En la tabla siguiente se muestran los códigos de cuatro caracteres (FOURCC) que corresponden a las categorías de entrada codificada que son compatibles con el descodificador Windows Media Video.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Perfil simple de Media Video 9   | "WMV3"                                   |
| Windows Perfil principal de Vídeo multimedia 9     | "WMV3"                                   |
| Windows Perfil avanzado de Media Video 9 | "WVC1"                                   |
| Windows Imagen de Vídeo multimedia 9.1          | "WMVP" para 9.1, "WVP2" para la versión 9.1 2 |



 

## <a name="output-formats"></a>Formatos de salida

El Windows de Vídeo multimedia admite los siguientes subtipos de medios de salida cuando actúa como DMO.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

El Windows media video admite los siguientes subtipos de medios de salida cuando actúa como MFT.

-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="properties"></a>Propiedades

El descodificador Windows Media Video admite las siguientes propiedades.




| Propiedad | Descripción | 
|----------|-------------|
| <a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a> | Especifica si el códec descodifica fotogramas de vídeo entrelazados de la secuencia comprimida como fotogramas progresivas.<br /><dl> Windows XP y versiones posteriores.<br />Perfil simple, perfil principal, perfil avanzado.<br />Lectura/escritura<br /></dl> | 
| <a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a> | Especifica si el descodificador usará hardware de aceleración de vídeo directX, si está disponible.<br /><dl> Windows XP y versiones posteriores.<br />Perfil simple, perfil principal, perfil avanzado.<br />De solo escritura.<br /></dl> | 
| <a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a> | Especifica el nivel de energía del descodificador.<br /><dl> Windows 7.<br />Perfil simple, perfil principal, perfil avanzado, imagen.<br />Lectura/escritura<br /></dl> | 
| <a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a> | Especifica si el descodificador debe usar la interpolación de fotogramas.<br /><dl> Windows XP y versiones posteriores.<br />Perfil simple, perfil principal, perfil avanzado, imagen.<br />De solo escritura.<br /></dl> | 
| <a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a> | Especifica si el descodificador admite la interpolación de fotogramas.<br /><dl> Windows XP y versiones posteriores.<br />Perfil simple, perfil principal, perfil avanzado, imagen<br />Solo lectura.<br /></dl> | 
| <a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a> | Especifica el número de subprocesos que usará el descodificador.<br /><dl> Windows Vista y versiones posteriores.<br />Perfil simple, perfil principal, perfil avanzado, imagen.<br />Lectura/escritura<br /></dl> | 
| <a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a> | Especifica el modo de procesamiento posterior para el descodificador.<br /><dl> Windows Vista y versiones posteriores.<br />Perfil simple, perfil principal, perfil avanzado, imagen.<br />De solo escritura.<br /></dl> | 
| <strong>g_wszWMVCNeedsDrain</strong> | Especifica si se debe purgar el descodificador.<br /><dl> Windows 8<br />Solo lectura.<br /></dl> Esta propiedad la usa el tiempo de ejecución Windows formato multimedia. El tipo de propiedad <strong>es VARIANT_BOOL</strong>. Si el valor es <strong>VARIANT_TRUE</strong>, el descodificador se debe purgar después de una discontinuidad. Para obtener más información sobre cómo purgar un MFT, vea <a href="basic-mft-processing-model.md">Basic MFT Processing Model</a>.<br /><blockquote>[!Note]<br />Para consultar esta propiedad, use la <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>interfaz IPropertyBag.</strong></a></blockquote><br /> | 




 

## <a name="remarks"></a>Comentarios

La resolución máxima permitida por el descodificador Windows Media Video 9 es 4096 x 4096.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Implementación de códec](codecimplementation.md)
</dt> </dl>

 

 
