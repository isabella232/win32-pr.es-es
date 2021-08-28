---
title: Tipos de extensión de ejemplo
description: Tipos de extensión de ejemplo
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows SDK de formato multimedia, extensiones de ejemplo
- Formato de sistemas avanzados (ASF), extensiones de ejemplo
- ASF (formato de sistemas avanzados), extensiones de ejemplo
- Windows SDK de formato multimedia, extensiones de unidad de datos
- Formato de sistemas avanzados (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- Windows SDK de formato multimedia, propiedades de búfer
- Formato de sistemas avanzados (ASF), propiedades de búfer
- ASF (formato de sistemas avanzados), propiedades de búfer
- extensiones de ejemplo, tipos
- extensiones de unidad de datos, tipos
- propiedades de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1404dfee60c3de179df2bee0f7f123112002108
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479781"
---
# <a name="sample-extension-types"></a>Tipos de extensión de ejemplo

Las extensiones de ejemplo, también denominadas extensiones de unidad de datos (DUE) o propiedades de búfer, son elementos de datos que se adjuntan a los ejemplos multimedia en la sección de datos del archivo ASF. Se definen varios tipos de extensiones de ejemplo en Windows SDK de formato multimedia. También puede crear sus propios tipos de extensión.

Para usar extensiones de ejemplo, debe identificar el tipo de extensión en los datos de configuración de flujo del perfil. Llame al [**método IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para configurar una secuencia para aceptar ejemplos con datos extendidos.

Las extensiones de ejemplo individuales se deben agregar a los ejemplos de entrada llamando al [**método INSSBuffer3::SetProperty.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) Al leer ejemplos, puede llamar al método [**INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) para recuperar los datos de extensión. También puede usar los métodos de la [**interfaz INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) para enumerar las extensiones de unidad de datos asociadas a un ejemplo.

En la tabla siguiente se enumeran los identificadores predefinidos de extensión de unidad de datos y se describen los datos que se adjuntan a los ejemplos de cada uno.




| GUID de extensión de ejemplo | Descripción | 
|-----------------------|-------------|
| WM_SampleExtensionGUID_OutputCleanPoint | Los datos indican si el ejemplo es un <a href="wmformat-glossary.md"><em>punto limpio.</em></a> Un valor de cero indica que el ejemplo no es un punto limpio. Un valor distinto de cero indica que es un punto limpio. Este tipo de extensión de unidad de datos (DUE) de ejemplo se usa para realizar un seguimiento de los puntos limpios al escribir secuencias multimedia precomprimidas que se codificaron con códecs de terceros. | 
| WM_SampleExtensionGUID_Timecode | Los datos son una <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> estructura que contiene datos de código de tiempo SMPTE asociados al ejemplo. El tamaño de este DUE siempre es WM_SampleExtension_Timecode_Size, que es de 14 bytes.<br /> | 
| WM_SampleExtensionGUID_FileName | Este tipo de extensión de ejemplo se usa para secuencias de archivos. Los datos de un ejemplo de flujo de archivo son un fragmento de un archivo de datos. Los datos de la extensión de ejemplo especifican el nombre del archivo del que se tomó el contenido del ejemplo. El nombre de archivo es una cadena de caracteres anchos que contiene el nombre de archivo en formato name.extension sin ninguna información de ruta de acceso.<br /> | 
| WM_SampleExtensionGUID_ContentType | Los datos identifican el tipo de contenido que contiene el ejemplo. Este tipo de extensión de ejemplo se usa con secuencias de vídeo entrelazadas. Todo el contenido entrelazado usa la marca WM_CT_INTERLACED combinada por un <strong>OR</strong> bit a bit con WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST o WM_CT_REPEAT_FIRST_FIELD.<br /> El orden de campo no se usa en el proceso de codificación, pero se mantiene con los ejemplos comprimidos para que se pueda pasar al hardware de representación. La reproducción de contenido entrelazado con el orden de campo incorrecto introduce artefactos como la vibración del movimiento en el vídeo.<br /> El tamaño de este DUE siempre es WM_SampleExtension_ContentType_Size.<br /> | 
| WM_SampleExtensionGUID_PixelAspectRatio | Los datos indican la relación de aspecto de píxeles del contenido del ejemplo. Esto solo se aplica al vídeo. Este tipo de extensión se usa para identificar la relación de aspecto de píxeles no cuadrados. Para obtener más información, <a href="to-read-and-write-video-streams-with-non-square-pixels.md">vea To Read and Write Video Secuencias with Non-Square Pixels</a>.<br /> Los valores de relación de aspecto se almacenan como una palabra cuyo byte bajo es el aspecto X y cuyo byte alto es el aspecto Y. Por ejemplo, 16:9 se almacena como 0x0910.<br /> El tamaño de este DUE siempre es WM_SampleExtension_PixelAspectRatio_Size, que es de 2 bytes.<br /> | 
| WM_SampleExtensionGUID_SampleDuration | Los datos indican la duración, en milisegundos, de la muestra contenida en el objeto de búfer. En la reproducción, si se establece due, el objeto lector lo usará para sobrescribir el valor de duración de la muestra existente. Este DUE lo establecen automáticamente los componentes en tiempo de ejecución del SDK en secuencias de vídeo con velocidades de bits de 100 kbps o superiores, donde la sobrecarga de la información de DUE no es significativa. No se establece para secuencias con velocidades de bits inferiores a 100 kbps. Las aplicaciones no deben establecer este DUE manualmente porque el escritor (en secuencias de velocidad de bits alta) sobrescribirá el valor con sus propios datos.<br /> El tamaño de este DUE siempre es WM_SampleExtension_SampleDuration_Size, que es de 2 bytes.<br /> | 
| WM_SampleExtensionGUID_ChromaLocation | Los datos indican el tipo de submuestreo de croma usado en el formato de vídeo I420. El valor de esta extensión se establece en uno de los valores siguientes:<br /><ul><li>WM_CL_INTERLACED420</li><li>WM_CL_PROGRESSIVE420</li></ul>Esta extensión de unidad de datos no está configurada en el perfil. Se incluye en la salida de ejemplos del descodificador.<br /> El tamaño de este DUE siempre es WM_SampleExtension_ChromaLocation_Size, que es de 1 byte.<br /> | 
| WM_SampleExtensionGUID_ColorSpaceInfo | Los datos proporcionan información sobre el espacio de color utilizado para el fotograma de vídeo actual. El valor de esta extensión es una <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> estructura.<br /> Esta extensión de unidad de datos no está configurada en el perfil. Se incluye en la salida de ejemplos del descodificador.<br /> El tamaño de este DUE siempre es WM_SampleExtension_ColorSpaceInfo_Size, que es de 3 bytes.<br /> | 
| WM_SampleExtensionGUID_UserDataInfo | Los datos son datos de usuario personalizados. Los cuatro primeros bytes de los datos contienen el tamaño de los datos personalizados.<br /> El byte siguiente contiene el tipo de datos de usuario proporcionado en la extensión de ejemplo. Se admiten los siguientes tipos:<br /><ul><li>0x1F: datos de usuario de nivel de secuencia</li><li>0x1E: datos de usuario de nivel de punto de entrada</li><li>0x1D: datos de usuario de nivel de marco</li><li>0x1C: datos de usuario de nivel de campo</li><li>0x1B: datos de usuario de nivel de segmento</li></ul>El sexto y los bytes subsiguientes contienen los datos del usuario. Hay tantos bytes de datos de usuario como se especifica en el número de los cuatro primeros bytes.<br /> Esta extensión de unidad de datos no está configurada en el perfil. Se incluye en ejemplos que son la salida del descodificador.<br /> | 
| WM_SampleExtensionGUID_SampleProtectionSalt | Los datos se cifran por ejemplo. Este tipo de extensión de ejemplo se usa para el contenido que se importa desde un formato de archivo que no es ASF y un esquema de protección de derechos distinto de Windows DRM multimedia. Al importar contenido protegido, cada ejemplo debe incluir una sal única. Normalmente, este valor es un contador que aumenta de forma monónica.<br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 





