---
description: El descodificador de Windows Media Video 9 descodifica las secuencias de vídeo codificadas por el codificador Windows Media Video.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Descodificador de Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718873"
---
# <a name="windows-media-video-9-decoder"></a>Descodificador de Windows Media Video 9

El descodificador de Windows Media Video 9 descodifica las secuencias de vídeo codificadas por el [**codificador Windows Media Video**](windowsmediavideo9encoder.md). El codificador y el descodificador admiten las cuatro categorías siguientes de vídeo codificado.

-   Perfil sencillo de Windows Media Video 9
-   Perfil principal de Windows Media Video 9
-   Perfil avanzado de Windows Media Video 9
-   Windows Media Video imagen 9,1

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador de Windows Media Video se representa mediante la constante **\_ CWMVDecMediaObject de CLSID**. Puede crear una instancia del descodificador de vídeo llamando a **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objeto de descodificador de vídeo expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto pueda usarse como una transformación de Media Foundation (MFT).

Un descodificador de vídeo se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador de vídeo se comporta como DMO o MFT.



| Sistema operativo            | Comportamiento del descodificador                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un descodificador de vídeo de Windows Media siempre se comporta como DMO.                                                                                                                |
| Windows Vista y Windows 7 | De forma predeterminada, un descodificador de vídeo de Windows Media se comporta como un DMO. Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un descodificador de vídeo, se comporta como una MFT. |



 

A partir de Windows 7, el descodificador de Windows Media Video implementa la interfaz [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .

## <a name="input-formats"></a>Formatos de entrada

En la tabla siguiente se muestran los códigos de cuatro caracteres (FOURCCs) que corresponden a las categorías de entrada codificada admitidas por el descodificador de Windows Media Video.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Perfil sencillo de Windows Media Video 9   | "WMV3"                                   |
| Perfil principal de Windows Media Video 9     | "WMV3"                                   |
| Perfil avanzado de Windows Media Video 9 | "WVC1"                                   |
| Windows Media Video imagen 9,1          | "WMVP" para 9,1, "WVP2" para la versión 2 de 9,1 |



 

## <a name="output-formats"></a>Formatos de salida

El descodificador de Windows Media Video admite los siguientes subtipos de medios de salida cuando actúa como DMO.

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

El descodificador de Windows Media Video admite los siguientes subtipos de medios de salida cuando actúa como MFT.

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

El descodificador de Windows Media Video admite las siguientes propiedades.



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
<td>Especifica si el códec descodifica fotogramas de vídeo entrelazados del flujo comprimido como tramas progresivas.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></td>
<td>Especifica si el descodificador usará hardware de aceleración de vídeo de DirectX, si está disponible.<br/> <dl> Windows XP y versiones posteriores.<br />
Perfil simple, perfil principal, perfil avanzado.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></td>
<td>Especifica el nivel de energía para el descodificador.<br/> <dl> Windows 7.<br />
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
</dl> El tiempo de ejecución de Windows Media Format usa esta propiedad. El tipo de propiedad es <strong>VARIANT_BOOL</strong>. Si el valor es <strong>VARIANT_TRUE</strong>, el descodificador se debe purgar después de una discontinuidad. Para obtener más información acerca de cómo purgar una MFT, vea <a href="basic-mft-processing-model.md">modelo de procesamiento de MFT básico</a>.<br/>
<blockquote>
[!Note]<br />
Para consultar esta propiedad, use la interfaz <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

La resolución máxima permitida por el descodificador de Windows Media Video 9 es 4096x4096.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Implementación de códecs](codecimplementation.md)
</dt> </dl>

 

 
