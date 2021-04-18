---
title: Tipos de extensión de ejemplo
description: Tipos de extensión de ejemplo
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- SDK de Windows Media Format, extensiones de ejemplo
- Advanced Systems Format (ASF), extensiones de ejemplo
- ASF (formato de sistemas avanzados), extensiones de ejemplo
- Windows Media Format SDK, extensiones de unidad de datos
- Advanced Systems Format (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- SDK de Windows Media Format, propiedades de búfer
- Advanced Systems Format (ASF), propiedades de búfer
- ASF (formato de sistemas avanzados), propiedades de búfer
- extensiones de ejemplo, tipos
- extensiones de unidad de datos, tipos
- propiedades de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "105714349"
---
# <a name="sample-extension-types"></a>Tipos de extensión de ejemplo

Las extensiones de ejemplo, también denominadas extensiones de unidad de datos (cuotas) o propiedades de búfer, son elementos de datos que se adjuntan a los ejemplos de medios en la sección de datos del archivo ASF. En el SDK de Windows Media Format se definen varios tipos de extensiones de ejemplo. También puede crear sus propios tipos de extensión.

Para usar las extensiones de ejemplo, debe identificar el tipo de extensión en los datos de configuración de la secuencia del perfil. Llame al método [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para configurar una secuencia que acepte ejemplos con datos extendidos.

Las extensiones de ejemplo individuales se deben agregar a los ejemplos de entrada mediante una llamada al método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Al leer ejemplos, puede llamar al método [**INSSBuffer3:: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) para recuperar los datos de la extensión. También puede utilizar los métodos de la interfaz [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) para enumerar las extensiones de unidad de datos adjuntas a un ejemplo.

En la tabla siguiente se enumeran los identificadores de extensión de unidad de datos predefinidos y se describen los datos que se adjuntan a los ejemplos de cada uno.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID de extensión de ejemplo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_SampleExtensionGUID_OutputCleanPoint</td>
<td>Los datos indican si el ejemplo es un <a href="wmformat-glossary.md"><em>cleanpoint</em></a>. Un valor de cero indica que el ejemplo no es un cleanpoint. Un valor distinto de cero indica que se trata de un cleanpoint. Este tipo de extensión de unidad de datos (vencimiento) de ejemplo se usa para realizar un seguimiento de cleanpoints al escribir secuencias de medios precomprimidos codificados con códecs de terceros.</td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_Timecode</td>
<td>Los datos son una estructura <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> que contiene datos de código de tiempo SMPTE asociados al ejemplo. El tamaño de este debido siempre es WM_SampleExtension_Timecode_Size, que es 14 bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_FileName</td>
<td>Este tipo de extensión de ejemplo se usa para las secuencias de archivo. Los datos de un ejemplo de secuencia de archivos son una parte de un archivo de datos. Los datos de la extensión de ejemplo especifican el nombre del archivo del que se tomó el contenido de la muestra. El nombre de archivo es una cadena de caracteres anchos que contiene el nombre de archivo en el formato Name. Extension sin información de ruta de acceso.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ContentType</td>
<td>Los datos identifican el tipo de contenido que contiene el ejemplo. Este tipo de extensión de ejemplo se usa con secuencias de vídeo entrelazadas. Todo el contenido entrelazado utiliza la marca WM_CT_INTERLACED combinada por <strong>una operación OR bit a bit</strong> con WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST o WM_CT_REPEAT_FIRST_FIELD.<br/> El orden de los campos no se utiliza en el proceso de codificación, pero se mantiene con los ejemplos comprimidos para que se pueda pasar al hardware de representación. La reproducción de contenido entrelazado con el orden de campo incorrecto presenta artefactos como la vibración de movimiento en el vídeo.<br/> El tamaño de este debido siempre es WM_SampleExtension_ContentType_Size.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_PixelAspectRatio</td>
<td>Los datos indican la relación de aspecto de píxeles del contenido en el ejemplo. Esto solo se aplica al vídeo. Este tipo de extensión se usa para identificar la relación de aspecto de los píxeles no cuadrados. Para obtener más información, vea <a href="to-read-and-write-video-streams-with-non-square-pixels.md">para leer y escribir secuencias de vídeo con píxeles no cuadrados</a>.<br/> Los valores de relación de aspecto se almacenan como una palabra cuyo byte bajo es el aspecto X y cuyo byte alto es el aspecto Y. Por ejemplo, 16:9 se almacena como 0x0910.<br/> El tamaño de este debido siempre es WM_SampleExtension_PixelAspectRatio_Size, que es 2 bytes.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleDuration</td>
<td>Los datos indican la duración, en milisegundos, del ejemplo contenido en el objeto de búfer. En la reproducción, si esta causa se establece, el objeto de lector la usará para sobrescribir el valor de duración de ejemplo existente. Esto se debe a que los componentes en tiempo de ejecución de SDK establecen automáticamente en secuencias de vídeo con velocidades de bits de 100 kbps o superiores, donde la sobrecarga de la información debida no es significativa. No se establece para las secuencias con velocidades de bits en 100 kbps. Las aplicaciones no deben establecer esto debido a que el escritor (en flujos de velocidad de bits alto) sobrescribirá el valor con sus propios datos.<br/> El tamaño de este debido siempre es WM_SampleExtension_SampleDuration_Size, que es 2 bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_ChromaLocation</td>
<td>Los datos indican el tipo de submuestreo de croma usado en el formato de vídeo i420. El valor de esta extensión se establece en uno de los valores siguientes:<br/>
<ul>
<li>WM_CL_INTERLACED420</li>
<li>WM_CL_PROGRESSIVE420</li>
</ul>
Esta extensión de unidad de datos no está configurada en el perfil. Se incluye en los resultados de los ejemplos del descodificador.<br/> El tamaño de este debido siempre es WM_SampleExtension_ChromaLocation_Size, que es 1 byte.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ColorSpaceInfo</td>
<td>Los datos proporcionan información sobre el espacio de colores usado para el fotograma de vídeo actual. El valor de esta extensión es una estructura de <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> .<br/> Esta extensión de unidad de datos no está configurada en el perfil. Se incluye en los resultados de los ejemplos del descodificador.<br/> El tamaño de este debido siempre es WM_SampleExtension_ColorSpaceInfo_Size, que es 3 bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_UserDataInfo</td>
<td>Los datos son datos de usuario personalizados. Los primeros cuatro bytes de los datos contienen el tamaño de los datos personalizados.<br/> El siguiente byte contiene el tipo de datos de usuario proporcionados en la extensión de ejemplo. Se admiten los siguientes tipos:<br/>
<ul>
<li>0x1F: datos de usuario de nivel de secuencia</li>
<li>0x1E: datos de usuario de nivel de punto de entrada</li>
<li>0x1D: datos de usuario de nivel de marco</li>
<li>0x1C-datos de usuario de nivel de campo</li>
<li>0x1B: datos de usuario de nivel de segmento</li>
</ul>
Los bytes sexto y siguiente contienen los datos del usuario. Hay tantos bytes de datos de usuario como especifica el número en los primeros cuatro bytes.<br/> Esta extensión de unidad de datos no está configurada en el perfil. Se incluye en los ejemplos que se generan desde el descodificador.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleProtectionSalt</td>
<td>Los datos se cifran mediante un ejemplo. Este tipo de extensión de ejemplo se usa para el contenido que se importa desde un formato de archivo no ASF y un esquema de protección de derechos distinto de DRM de Windows Media. Al importar contenido protegido, cada ejemplo debe incluir un valor Salt único. Normalmente, este valor es un contador que aumenta de forma continuada.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 





