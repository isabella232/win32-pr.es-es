---
title: Enumeración WMDM_FORMATCODE
description: El \_ tipo de enumeración FORMATCODE de WMDM define una lista de códigos de formato que describen los tipos de contenido transferidos hacia y desde un dispositivo.
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- Enumeración WMDM_FORMATCODE Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_FORMATCODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04db31578f36455fdf77bb4044ad45e5ca9f9a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698532"
---
# <a name="wmdm_formatcode-enumeration"></a>\_Enumeración FORMATCODE de WMDM

El tipo de enumeración **\_ FORMATCODE de WMDM** define una lista de códigos de formato que describen los tipos de contenido transferidos hacia y desde un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagWMDM_FORMATCODE { 
  WMDM_FORMATCODE_NOTUSED,
  WMDM_FORMATCODE_ALLIMAGES,
  WMDM_FORMATCODE_UNDEFINED,
  WMDM_FORMATCODE_ASSOCIATION,
  WMDM_FORMATCODE_SCRIPT,
  WMDM_FORMATCODE_EXECUTABLE,
  WMDM_FORMATCODE_TEXT,
  WMDM_FORMATCODE_HTML,
  WMDM_FORMATCODE_DPOF,
  WMDM_FORMATCODE_AIFF,
  WMDM_FORMATCODE_WAVE,
  WMDM_FORMATCODE_MP3,
  WMDM_FORMATCODE_AVI,
  WMDM_FORMATCODE_MPEG,
  WMDM_FORMATCODE_ASF,
  WMDM_FORMATCODE_RESERVED_FIRST,
  WMDM_FORMATCODE_RESERVED_LAST,
  WMDM_FORMATCODE_IMAGE_UNDEFINED,
  WMDM_FORMATCODE_IMAGE_EXIF,
  WMDM_FORMATCODE_IMAGE_TIFFEP,
  WMDM_FORMATCODE_IMAGE_FLASHPIX,
  WMDM_FORMATCODE_IMAGE_BMP,
  WMDM_FORMATCODE_IMAGE_CIFF,
  WMDM_FORMATCODE_IMAGE_GIF,
  WMDM_FORMATCODE_IMAGE_JFIF,
  WMDM_FORMATCODE_IMAGE_PCD,
  WMDM_FORMATCODE_IMAGE_PICT,
  WMDM_FORMATCODE_IMAGE_PNG,
  WMDM_FORMATCODE_IMAGE_TIFF,
  WMDM_FORMATCODE_IMAGE_TIFFIT,
  WMDM_FORMATCODE_IMAGE_JP2,
  WMDM_FORMATCODE_IMAGE_JPX,
  WMDM_FORMATCODE_IMAGE_RESERVED_FIRST,
  WMDM_FORMATCODE_IMAGE_RESERVED_LAST,
  WMDM_FORMATCODE_UNDEFINEDFIRMWARE,
          WMDM_FORMATCODE_WBMP
,
                  WMDM_FORMATCODE_JPEGXR
,
  WMDM_FORMATCODE_WINDOWSIMAGEFORMAT,
  WMDM_FORMATCODE_UNDEFINEDAUDIO,
  WMDM_FORMATCODE_WMA,
  WMDM_FORMATCODE_OGG,
  WMDM_FORMATCODE_AAC,
  WMDM_FORMATCODE_AUDIBLE,
  WMDM_FORMATCODE_FLAC,
          WMDM_FORMATCODE_QCELP
,
          WMDM_FORMATCODE_AMR
,
  WMDM_FORMATCODE_UNDEFINEDVIDEO,
  WMDM_FORMATCODE_WMV,
  WMDM_FORMATCODE_MP4,
  WMDM_FORMATCODE_MP2,
          WMDM_FORMATCODE_3G2
,
                  WMDM_FORMATCODE_AVCHD
,
                  WMDM_FORMATCODE_ATSCTS
,
                          WMDM_FORMATCODE_DVBTS
,
  WMDM_FORMATCODE_UNDEFINEDCOLLECTION,
  WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM,
  WMDM_FORMATCODE_ABSTRACTIMAGEALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOALBUM,
  WMDM_FORMATCODE_ABSTRACTVIDEOALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST,
  WMDM_FORMATCODE_ABSTRACTCONTACTGROUP,
  WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER,
  WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION,
  WMDM_FORMATCODE_WPLPLAYLIST,
  WMDM_FORMATCODE_M3UPLAYLIST,
  WMDM_FORMATCODE_MPLPLAYLIST,
  WMDM_FORMATCODE_ASXPLAYLIST,
  WMDM_FORMATCODE_PLSPLAYLIST,
  WMDM_FORMATCODE_UNDEFINEDDOCUMENT,
  WMDM_FORMATCODE_ABSTRACTDOCUMENT,
  WMDM_FORMATCODE_XMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT,
  WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET,
  WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT,
  WMDM_FORMATCODE_UNDEFINEDMESSAGE,
  WMDM_FORMATCODE_ABSTRACTMESSAGE,
  WMDM_FORMATCODE_UNDEFINEDCONTACT,
  WMDM_FORMATCODE_ABSTRACTCONTACT,
  WMDM_FORMATCODE_VCARD2,
  WMDM_FORMATCODE_VCARD3,
  WMDM_FORMATCODE_UNDEFINEDCALENDARITEM,
  WMDM_FORMATCODE_ABSTRACTCALENDARITEM,
  WMDM_FORMATCODE_VCALENDAR1,
  WMDM_FORMATCODE_VCALENDAR2,
  WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE,
  WMDM_FORMATCODE_MEDIA_CAST,
  WMDM_FORMATCODE_SECTION,
                                  WMDM_FORMATCODE_3G2A

} WMDM_FORMATCODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**\_FORMATCODE \_ NOTUSED de WMDM**
</dt> <dd>

No se usa ningún código de formato.

</dd> <dt>

<span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**\_FORMATCODE \_ ALLIMAGES de WMDM**
</dt> <dd>

Código de formato que se puede usar para consultar todas las imágenes.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**FORMATCODE de WMDM \_ \_ sin definir**
</dt> <dd>

Código de formato usado para consultar todos los objetos no definidos.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**\_Asociación de FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato usado para definir un vínculo entre dos objetos.

</dd> <dt>

<span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**\_script FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para un archivo de script.

</dd> <dt>

<span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**\_archivo ejecutable FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para un archivo ejecutable.

</dd> <dt>

<span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**\_texto FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para un archivo de texto.

</dd> <dt>

<span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**\_HTML FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para un archivo HTML.

</dd> <dt>

<span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**\_FORMATCODE \_ DPOF de WMDM**
</dt> <dd>

Código de formato usado para representar el formato de orden de impresión digital.

</dd> <dt>

<span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**\_FORMATCODE \_ AIFF de WMDM**
</dt> <dd>

Código de formato usado para representar el formato de archivo de intercambio de audio.

</dd> <dt>

<span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**\_Wave FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato usado para un archivo WAV.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**\_Mp3 FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato usado para un archivo MP3.

</dd> <dt>

<span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**\_AVI FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato usado para un archivo AVI.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**\_FORMATCODE \_ MPEG de WMDM**
</dt> <dd>

Código de formato usado para un archivo MPEG.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**\_FORMATCODE \_ ASF de WMDM**
</dt> <dd>

Código de formato usado para representar un archivo de formato de sistema avanzado (ASF).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**FORMATCODE de WMDM \_ \_ reservado \_ primero**
</dt> <dd>

Código de formato que es el primero de un intervalo reservado para el protocolo de transferencia de imágenes (PTP).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**\_último FORMATCODE de WMDM \_ reservado \_**
</dt> <dd>

Código de formato que está en último lugar en un intervalo reservado para PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_imagen FORMATCODE de WMDM \_ \_ sin definir**
</dt> <dd>

Código de formato usado para representar e imagen de un tipo no definido.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**\_ \_ imagen Exif FORMATCODE \_ de WMDM**
</dt> <dd>

Código de formato para un archivo EXIF. También se usa para imágenes JPEG no incluidas en la imagen de WMDM \_ FORMATCODE \_ \_ JP2 o WMDM \_ FORMATCODE \_ Image \_ jpx.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**\_TIFFEP de \_ imagen \_ FORMATCODE de WMDM**
</dt> <dd>

Código de formato usado para las imágenes que son del tipo Tagged Image File Format para la fotografía electrónica (TIFF/EP)

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**\_imagen de FORMATCODE para WMDM \_ \_**
</dt> <dd>

Código de formato para un archivo de tipo FPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**\_BMP de \_ imagen \_ FORMATCODE de WMDM**
</dt> <dd>

Código de formato para un archivo de tipo BMP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**\_CIFF de \_ imagen \_ FORMATCODE de WMDM**
</dt> <dd>

Dar formato al código de una imagen en el formato de archivo de imagen de cámara.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**\_ \_ imagen GIF de FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para un archivo GIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**imagen de WMDM \_ FORMATCODE \_ \_ JFIF**
</dt> <dd>

Código de formato para un archivo de tipo JFIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**\_ \_ imagen PCD FORMATCODE \_ de WMDM**
</dt> <dd>

Código de formato para una imagen de tipo Photo CD.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**\_ \_ imagen PICT FORMATCODE \_ de WMDM**
</dt> <dd>

Código de formato para una imagen de tipo PICT.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**\_ \_ imagen PNG de FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para una imagen de tipo PNG.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**\_ \_ imagen TIFF de FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para un archivo de tipo TIFF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**\_TIFFIT de \_ imagen \_ FORMATCODE de WMDM**
</dt> <dd>

Código de formato para una imagen de tipo Tagged Image File Format con tecnología de imagen.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**\_JP2 de \_ imagen \_ FORMATCODE de WMDM**
</dt> <dd>

Código de formato para una imagen de JPEG200.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**\_jpx de \_ imagen \_ FORMATCODE de WMDM**
</dt> <dd>

Código de formato para una imagen creada en JPEG200, mediante el registro de imagen extendida. La extensión de nombre de archivo suele ser. JPF o. jpx.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**\_imagen FORMATCODE de WMDM \_ \_ reservada en \_ primer lugar**
</dt> <dd>

Código de formato que es el primero de un intervalo reservado para una referencia de imagen en PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**\_última imagen de FORMATCODE de WMDM \_ \_ reservada \_**
</dt> <dd>

Código de formato que es el último de un intervalo reservado para una referencia de imagen en PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**\_FORMATCODE \_ UNDEFINEDFIRMWARE de WMDM**
</dt> <dd>

Dar formato al código cuando el firmware no está definido.

</dd> <dt>

<span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ FORMATCODE \_ WBMP** 
</dt> <dd>

Código de formato para una imagen de mapa de bits del Protocolo de aplicación inalámbrica (. WBMP).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ FORMATCODE \_ JPEGXR** 
</dt> <dd>

Dar formato al código para una imagen fotográfica HD

</dd> <dt>

<span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**\_FORMATCODE \_ WINDOWSIMAGEFORMAT de WMDM**
</dt> <dd>

Código de formato para el formato de imagen de Windows.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**\_FORMATCODE \_ UNDEFINEDAUDIO de WMDM**
</dt> <dd>

Código de formato para un archivo de audio de tipo no definido.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**FORMATCODE de WMDM \_ \_**
</dt> <dd>

Código de formato para un archivo Windows Media Audio (WMA).

</dd> <dt>

<span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**\_FORMATCODE \_ OGG de WMDM**
</dt> <dd>

Código de formato para un archivo de audio codificado en Vorbis en un contenedor OGG.

</dd> <dt>

<span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**\_AAC FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para un archivo AAC (codificación de audio avanzado).

</dd> <dt>

<span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**FORMATCODE de WMDM \_ \_**
</dt> <dd>

Código de formato para un archivo audible.

</dd> <dt>

<span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**\_FORMATCODE \_ FLAC de WMDM**
</dt> <dd>

Código de formato para un archivo de códec de audio sin pérdida (FLAC).

</dd> <dt>

<span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ FORMATCODE \_ QCELP** 
</dt> <dd>

Código de formato para un archivo de códec de predicción lineal (QCELP) de Qualcomm Code entusiasmado.

</dd> <dt>

<span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ \_AMR FORMATCODE** 
</dt> <dd>

Código de formato para un archivo de códec de audio de varias velocidades adaptable (AMR).

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**\_FORMATCODE \_ UNDEFINEDVIDEO de WMDM**
</dt> <dd>

Dar formato al código para un archivo de vídeo con un tipo no definido.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**FORMATCODE de WMDM \_ \_**
</dt> <dd>

Código de formato para un archivo Windows Media Video (WMV).

</dd> <dt>

<span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**\_FORMATCODE \_ MP4 de WMDM**
</dt> <dd>

Código de formato para un archivo MP4.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**FORMATCODE de WMDM y \_ \_ MP2**
</dt> <dd>

Código de formato para un archivo MP2.

</dd> <dt>

<span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ FORMATCODE \_ 3g2** 
</dt> <dd>

Código de formato para un formato de contenedor multimedia 3G2 (3GPP2). Un archivo de este tipo puede contener audio, vídeo o texto.

</dd> <dt>

<span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ FORMATCODE \_ AVCHD** 
</dt> <dd>

Código de formato para un archivo de vídeo AVCHD (codificación avanzada de vídeo de alta definición).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ FORMATCODE \_ ATSC** 
</dt> <dd>

Código de formato para el formato estándar del Comité de sistemas de televisión avanzado (ATSC).

</dd> <dt>

<span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ FORMATCODE \_ DVBTS** 
</dt> <dd>

Código de formato para un vídeo MPEG-2 y MPEG-1 capa II, o audio AC-3, dentro de una secuencia de transporte MPEG-2 compatible con DVB.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**\_FORMATCODE \_ UNDEFINEDCOLLECTION de WMDM**
</dt> <dd>

Código de formato para una colección de un tipo no definido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**\_FORMATCODE \_ ABSTRACTMULTIMEDIAALBUM de WMDM**
</dt> <dd>

Código de formato para un álbum multimedia en el que el objeto contiene las propiedades de un álbum multimedia y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**\_FORMATCODE \_ ABSTRACTIMAGEALBUM de WMDM**
</dt> <dd>

Código de formato para un álbum de imagen donde el objeto contiene las propiedades de un álbum de imagen y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**\_FORMATCODE \_ ABSTRACTAUDIOALBUM de WMDM**
</dt> <dd>

Código de formato para un álbum de audio donde el objeto contiene las propiedades de un álbum de audio y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**\_FORMATCODE \_ ABSTRACTVIDEOALBUM de WMDM**
</dt> <dd>

Código de formato para un álbum de vídeo en el que el objeto contiene las propiedades de un álbum de vídeo y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**\_FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST de WMDM**
</dt> <dd>

Código de formato para una lista de reproducción de audio o vídeo donde el objeto contiene las propiedades de una lista de reproducción de audio/vídeo y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**\_FORMATCODE \_ ABSTRACTCONTACTGROUP de WMDM**
</dt> <dd>

Dar formato al código para un grupo de contactos donde el objeto contiene las propiedades de un grupo de contactos y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**\_FORMATCODE \_ ABSTRACTMESSAGEFOLDER de WMDM**
</dt> <dd>

Código de formato para una carpeta de mensajes donde el objeto contiene las propiedades de una carpeta de mensajes y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**\_FORMATCODE \_ ABSTRACTCHAPTEREDPRODUCTION de WMDM**
</dt> <dd>

Código de formato para una producción en capítulo en la que el objeto contiene las propiedades de una producción de capítulo y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**\_FORMATCODE \_ WPLPLAYLIST de WMDM**
</dt> <dd>

Código de formato para una lista de reproducción formateada con formato de lista de reproducción de Windows Media.

</dd> <dt>

<span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**\_FORMATCODE \_ M3UPLAYLIST de WMDM**
</dt> <dd>

Dar formato al código de una lista de reproducción con formato M3U.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**\_FORMATCODE \_ MPLPLAYLIST de WMDM**
</dt> <dd>

Dar formato al código para una lista de reproducción con formato MPL.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**\_FORMATCODE \_ ASXPLAYLIST de WMDM**
</dt> <dd>

Dar formato al código para una lista de reproducción con formato ASX.

</dd> <dt>

<span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**\_FORMATCODE \_ PLSPLAYLIST de WMDM**
</dt> <dd>

Dar formato al código para una lista de reproducción con formato esperen.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**\_FORMATCODE \_ UNDEFINEDDOCUMENT de WMDM**
</dt> <dd>

Código de formato para un documento de tipo no definido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**\_FORMATCODE \_ ABSTRACTDOCUMENT de WMDM**
</dt> <dd>

Código de formato para un documento en el que el objeto contiene las propiedades de un documento y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**\_XMLDOCUMENT FORMATCODE de WMDM \_**
</dt> <dd>

Dar formato al código para un documento XML.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**\_FORMATCODE \_ MICROSOFTWORDDOCUMENT de WMDM**
</dt> <dd>

Dar formato al código para un documento de Microsoft Word.

</dd> <dt>

<span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**\_FORMATCODE \_ MHTCOMPILEDHTMLDOCUMENT de WMDM**
</dt> <dd>

Código de formato para un documento HTML compilado.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**\_FORMATCODE \_ MICROSOFTEXCELSPREADSHEET de WMDM**
</dt> <dd>

Dar formato al código para una hoja de cálculo de Microsoft Excel.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**\_FORMATCODE \_ MICROSOFTPOWERPOINTDOCUMENT de WMDM**
</dt> <dd>

Dar formato al código para un documento de Microsoft PowerPoint.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**\_FORMATCODE \_ UNDEFINEDMESSAGE de WMDM**
</dt> <dd>

Código de formato para un mensaje de tipo no definido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**\_FORMATCODE \_ ABSTRACTMESSAGE de WMDM**
</dt> <dd>

Código de formato para un mensaje en el que el objeto contiene las propiedades de un mensaje y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**\_FORMATCODE \_ UNDEFINEDCONTACT de WMDM**
</dt> <dd>

Código de formato para un contacto de tipo no definido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**\_FORMATCODE \_ ABSTRACTCONTACT de WMDM**
</dt> <dd>

Código de formato para un contacto en el que el objeto contiene las propiedades de un contacto y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**\_FORMATCODE \_ VCARD2 de WMDM**
</dt> <dd>

Dar formato al código para una tarjeta electrónica con formato vCard versión 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**\_FORMATCODE \_ VCARD3 de WMDM**
</dt> <dd>

Dar formato al código para una tarjeta electrónica con formato vCard versión 3.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**\_FORMATCODE \_ UNDEFINEDCALENDARITEM de WMDM**
</dt> <dd>

Código de formato para un elemento de calendario electrónico de tipo no definido.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**\_FORMATCODE \_ ABSTRACTCALENDARITEM de WMDM**
</dt> <dd>

Código de formato para un elemento de calendario en el que el objeto contiene las propiedades de un elemento de calendario y, opcionalmente, los datos. Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**\_FORMATCODE \_ VCALENDAR1 de WMDM**
</dt> <dd>

Código de formato para un elemento de calendario electrónico con formato vCalendar versión 1.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**\_FORMATCODE \_ VCALENDAR2 de WMDM**
</dt> <dd>

Código de formato para un elemento de calendario electrónico con formato vCalendar versión 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**\_FORMATCODE \_ UNDEFINEDWINDOWSEXECUTABLE de WMDM**
</dt> <dd>

Código de formato para un ejecutable basado en Windows de tipo no definido.

</dd> <dt>

<span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**\_ \_ conversión multimedia FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para un objeto de conversión de multimedia.

</dd> <dt>

<span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_sección FORMATCODE de WMDM \_**
</dt> <dd>

Código de formato para una sección de datos que se encuentra en otro objeto.

</dd> <dt>

<span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ FORMATCODE \_ 3G2A** 
</dt> <dd>

Código de formato para un formato de contenedor multimedia 3G2A (3GPP2A).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para detectar los formatos admitidos por un dispositivo, una aplicación puede usar [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para consultar la propiedad del dispositivo **g \_ wszWMDMFormatsSupported** .

Para detectar las capacidades del dispositivo para un formato determinado, una aplicación puede llamar a [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).

Una aplicación puede establecer el código de formato al crear un almacenamiento en el dispositivo incluyendo la propiedad **g \_ wszWMDMFormatCode** en los metadatos pasados en el parámetro *pMetaData* de una llamada a [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).

Una aplicación puede consultar el código de formato de un almacenamiento llamando a [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) y recuperando la propiedad **g \_ wszWMDMFormatCode** .

Si el dispositivo admite el establecimiento del código de formato después de la creación de almacenamiento, una aplicación puede usar [**IWMDMStorage3:: setMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) para establecer la propiedad **g \_ wszWMDMFormatCode** . Es posible que algunos dispositivos no permitan cambiar el código de formato una vez creado el almacenamiento en el dispositivo. Por lo tanto, se recomienda encarecidamente establecer esta propiedad junto con los metadatos pasados en [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[**Constantes de metadatos**](metadata-constants.md)
</dt> </dl>

 

 





