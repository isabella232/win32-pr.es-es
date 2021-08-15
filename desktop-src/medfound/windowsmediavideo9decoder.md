---
description: El descodificador Windows Media Video 9 descodifica las secuencias de vídeo codificadas por Windows Media Video Encoder.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Descodificador de Vídeo multimedia 9 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b251b46c94ef88283577dbd8268c3275d8ed6aab9321c98e115a42501e2729ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237267"
---
# <a name="windows-media-video-9-decoder"></a>Windows Descodificador de Vídeo multimedia 9

El descodificador Windows Media Video 9 descodifica las secuencias de vídeo codificadas por [**Windows Media Video Encoder**](windowsmediavideo9encoder.md). El codificador y el descodificador admiten las cuatro categorías siguientes de vídeo codificado.

-   Windows Perfil simple de Media Video 9
-   Windows Perfil principal de Media Video 9
-   Windows Perfil avanzado de Media Video 9
-   Windows Imagen de Vídeo multimedia 9.1

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador Windows Media Video se representa mediante la constante **CLSID \_ CWMVDecMediaObject**. Puede crear una instancia del descodificador de vídeo llamando a **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objeto descodificador de vídeo expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como objeto multimedia DirectX (DMO) y expone la interfaz [**DEFTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un descodificador de vídeo se comporta como un DMO o MFT en función de las interfaces que obtenga y la versión de Windows se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador de vídeo se comporta DMO o MFT.



| Sistema operativo            | Comportamiento del descodificador                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un Windows de vídeo multimedia siempre se comporta como un DMO.                                                                                                                |
| Windows Vista y Windows 7 | De forma predeterminada, un Windows de vídeo multimedia se comporta como un DMO. Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un descodificador de vídeo, se comporta como MFT. |



 

A partir Windows 7, el descodificador Windows Media Video implementa la [**interfaz IDMOQualityControl.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol)

## <a name="input-formats"></a>Formatos de entrada

En la tabla siguiente se muestran los códigos de cuatro caracteres (FOURCC) que corresponden a las categorías de entrada codificada que admite el descodificador Windows Media Video.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Perfil simple de Media Video 9   | "WMV3"                                   |
| Windows Perfil principal de Media Video 9     | "WMV3"                                   |
| Windows Perfil avanzado de Media Video 9 | "WVC1"                                   |
| Windows Imagen de Vídeo multimedia 9.1          | "WMVP" para 9.1, "WVP2" para la versión 9.1 versión 2 |



 

## <a name="output-formats"></a>Formatos de salida

El descodificador Windows Media Video admite los siguientes subtipos de medios de salida cuando actúa como un DMO.

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

El Windows de Media Video admite los siguientes subtipos de medios de salida cuando actúa como MFT.

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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></td>
<td>Especifica si el códec descodifica fotogramas de vídeo entrelazados de la secuencia comprimida como fotogramas progresivas.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></td>
<td>Especifica si el descodificador usará el hardware de aceleración de vídeo de DirectX, si está disponible.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></td>
<td>Especifica el nivel de energía del descodificador.<br/> <dl> Windows 7.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></td>
<td>Especifica si el descodificador debe usar la interpolación de fotogramas.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></td>
<td>Especifica si el descodificador admite la interpolación de fotogramas.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen<br />
Solo lectura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></td>
<td>Especifica el número de subprocesos que usará el descodificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></td>
<td>Especifica el modo de procesamiento posterior para el descodificador.<br/> <dl> Windows Vista y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado, imagen.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>g_wszWMVCNeedsDrain</strong></td>
<td>Especifica si se debe purgar el descodificador.<br/> <dl> Windows 8<br />
Solo lectura.<br />
</dl> Esta propiedad la usa el tiempo de ejecución Windows formato multimedia. El tipo de propiedad <strong>es VARIANT_BOOL</strong>. Si el valor es <strong>VARIANT_TRUE</strong>, el descodificador debe purgarse después de una discontinuidad. Para obtener más información sobre cómo purgar un MFT, vea <a href="basic-mft-processing-model.md">Basic MFT Processing Model</a>.<br/>
<blockquote>
[!Note]<br />
Para consultar esta propiedad, use la <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>interfaz IPropertyBag.</strong></a>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentarios

La resolución máxima permitida por el descodificador Windows Media Video 9 es 4096 x 4096.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Implementación de códec](codecimplementation.md)
</dt> </dl>

 

 
