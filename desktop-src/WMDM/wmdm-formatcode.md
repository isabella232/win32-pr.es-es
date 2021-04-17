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
# <a name="wmdm_formatcode-enumeration"></a><span data-ttu-id="58ecc-104">\_Enumeración FORMATCODE de WMDM</span><span class="sxs-lookup"><span data-stu-id="58ecc-104">WMDM\_FORMATCODE enumeration</span></span>

<span data-ttu-id="58ecc-105">El tipo de enumeración **\_ FORMATCODE de WMDM** define una lista de códigos de formato que describen los tipos de contenido transferidos hacia y desde un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58ecc-105">The **WMDM\_FORMATCODE** enumeration type defines a list of format codes that describe types of content transferred to and from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ecc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58ecc-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="58ecc-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="58ecc-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="58ecc-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**\_FORMATCODE \_ NOTUSED de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM\_FORMATCODE\_NOTUSED**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-109">No se usa ningún código de formato.</span><span class="sxs-lookup"><span data-stu-id="58ecc-109">No format code is used.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**\_FORMATCODE \_ ALLIMAGES de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM\_FORMATCODE\_ALLIMAGES**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-111">Código de formato que se puede usar para consultar todas las imágenes.</span><span class="sxs-lookup"><span data-stu-id="58ecc-111">Format code that can be used to query for all images.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**FORMATCODE de WMDM \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="58ecc-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM\_FORMATCODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-113">Código de formato usado para consultar todos los objetos no definidos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-113">Format code used to query for all undefined objects.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**\_Asociación de FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM\_FORMATCODE\_ASSOCIATION**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-115">Código de formato usado para definir un vínculo entre dos objetos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-115">Format code used to define a link between two objects.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**\_script FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM\_FORMATCODE\_SCRIPT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-117">Código de formato para un archivo de script.</span><span class="sxs-lookup"><span data-stu-id="58ecc-117">Format code for a script file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**\_archivo ejecutable FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM\_FORMATCODE\_EXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-119">Código de formato para un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="58ecc-119">Format code for an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**\_texto FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM\_FORMATCODE\_TEXT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-121">Código de formato para un archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="58ecc-121">Format code for a text file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**\_HTML FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM\_FORMATCODE\_HTML**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-123">Código de formato para un archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="58ecc-123">Format code for an HTML file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**\_FORMATCODE \_ DPOF de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM\_FORMATCODE\_DPOF**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-125">Código de formato usado para representar el formato de orden de impresión digital.</span><span class="sxs-lookup"><span data-stu-id="58ecc-125">Format code used to represent the digital print order format.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**\_FORMATCODE \_ AIFF de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM\_FORMATCODE\_AIFF**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-127">Código de formato usado para representar el formato de archivo de intercambio de audio.</span><span class="sxs-lookup"><span data-stu-id="58ecc-127">Format code used to represent the audio interchange file format.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**\_Wave FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM\_FORMATCODE\_WAVE**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-129">Código de formato usado para un archivo WAV.</span><span class="sxs-lookup"><span data-stu-id="58ecc-129">Format code used for a WAV file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**\_Mp3 FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM\_FORMATCODE\_MP3**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-131">Código de formato usado para un archivo MP3.</span><span class="sxs-lookup"><span data-stu-id="58ecc-131">Format code used for an MP3 file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**\_AVI FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM\_FORMATCODE\_AVI**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-133">Código de formato usado para un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="58ecc-133">Format code used for an AVI file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**\_FORMATCODE \_ MPEG de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM\_FORMATCODE\_MPEG**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-135">Código de formato usado para un archivo MPEG.</span><span class="sxs-lookup"><span data-stu-id="58ecc-135">Format code used for an MPEG file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**\_FORMATCODE \_ ASF de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM\_FORMATCODE\_ASF**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-137">Código de formato usado para representar un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="58ecc-137">Format code used to represent an Advanced Systems Format (ASF) file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**FORMATCODE de WMDM \_ \_ reservado \_ primero**</span><span class="sxs-lookup"><span data-stu-id="58ecc-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM\_FORMATCODE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-139">Código de formato que es el primero de un intervalo reservado para el protocolo de transferencia de imágenes (PTP).</span><span class="sxs-lookup"><span data-stu-id="58ecc-139">Format code that is the first in a range reserved for Picture Transfer Protocol (PTP).</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**\_último FORMATCODE de WMDM \_ reservado \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM\_FORMATCODE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-141">Código de formato que está en último lugar en un intervalo reservado para PTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-141">Format code that is last in a range reserved for PTP.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_imagen FORMATCODE de WMDM \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="58ecc-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM\_FORMATCODE\_IMAGE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-143">Código de formato usado para representar e imagen de un tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-143">Format code used to represent and image of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**\_ \_ imagen Exif FORMATCODE \_ de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM\_FORMATCODE\_IMAGE\_EXIF**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-145">Código de formato para un archivo EXIF.</span><span class="sxs-lookup"><span data-stu-id="58ecc-145">Format code for an EXIF file.</span></span> <span data-ttu-id="58ecc-146">También se usa para imágenes JPEG no incluidas en la imagen de WMDM \_ FORMATCODE \_ \_ JP2 o WMDM \_ FORMATCODE \_ Image \_ jpx.</span><span class="sxs-lookup"><span data-stu-id="58ecc-146">Also used for JPEG images not covered by WMDM\_FORMATCODE\_IMAGE\_JP2 or WMDM\_FORMATCODE\_IMAGE\_JPX.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**\_TIFFEP de \_ imagen \_ FORMATCODE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFEP**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-148">Código de formato usado para las imágenes que son del tipo Tagged Image File Format para la fotografía electrónica (TIFF/EP)</span><span class="sxs-lookup"><span data-stu-id="58ecc-148">Format code used for images that are of type Tagged Image File Format for Electronic Photography (TIFF/EP)</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**\_imagen de FORMATCODE para WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM\_FORMATCODE\_IMAGE\_FLASHPIX**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-150">Código de formato para un archivo de tipo FPX.</span><span class="sxs-lookup"><span data-stu-id="58ecc-150">Format code for a file of type FPX.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**\_BMP de \_ imagen \_ FORMATCODE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM\_FORMATCODE\_IMAGE\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-152">Código de formato para un archivo de tipo BMP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-152">Format code for a file of type BMP.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**\_CIFF de \_ imagen \_ FORMATCODE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM\_FORMATCODE\_IMAGE\_CIFF**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-154">Dar formato al código de una imagen en el formato de archivo de imagen de cámara.</span><span class="sxs-lookup"><span data-stu-id="58ecc-154">Format code for an image in the camera image file format.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**\_ \_ imagen GIF de FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM\_FORMATCODE\_IMAGE\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-156">Código de formato para un archivo GIF.</span><span class="sxs-lookup"><span data-stu-id="58ecc-156">Format code for a GIF file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**imagen de WMDM \_ FORMATCODE \_ \_ JFIF**</span><span class="sxs-lookup"><span data-stu-id="58ecc-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM\_FORMATCODE\_IMAGE\_JFIF**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-158">Código de formato para un archivo de tipo JFIF.</span><span class="sxs-lookup"><span data-stu-id="58ecc-158">Format code for a file of type JFIF.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**\_ \_ imagen PCD FORMATCODE \_ de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM\_FORMATCODE\_IMAGE\_PCD**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-160">Código de formato para una imagen de tipo Photo CD.</span><span class="sxs-lookup"><span data-stu-id="58ecc-160">Format code for an image of type photo cd.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**\_ \_ imagen PICT FORMATCODE \_ de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM\_FORMATCODE\_IMAGE\_PICT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-162">Código de formato para una imagen de tipo PICT.</span><span class="sxs-lookup"><span data-stu-id="58ecc-162">Format code for an image of type PICT.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**\_ \_ imagen PNG de FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM\_FORMATCODE\_IMAGE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-164">Código de formato para una imagen de tipo PNG.</span><span class="sxs-lookup"><span data-stu-id="58ecc-164">Format code for an image of type PNG.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**\_ \_ imagen TIFF de FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-166">Código de formato para un archivo de tipo TIFF.</span><span class="sxs-lookup"><span data-stu-id="58ecc-166">Format code for a file of type TIFF.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**\_TIFFIT de \_ imagen \_ FORMATCODE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFIT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-168">Código de formato para una imagen de tipo Tagged Image File Format con tecnología de imagen.</span><span class="sxs-lookup"><span data-stu-id="58ecc-168">Format code for an image of type Tagged Image File Format with image technology.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**\_JP2 de \_ imagen \_ FORMATCODE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM\_FORMATCODE\_IMAGE\_JP2**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-170">Código de formato para una imagen de JPEG200.</span><span class="sxs-lookup"><span data-stu-id="58ecc-170">Format code for a jpeg200 image.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**\_jpx de \_ imagen \_ FORMATCODE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM\_FORMATCODE\_IMAGE\_JPX**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-172">Código de formato para una imagen creada en JPEG200, mediante el registro de imagen extendida.</span><span class="sxs-lookup"><span data-stu-id="58ecc-172">Format code for an image built on JPEG200, using extended still image registration.</span></span> <span data-ttu-id="58ecc-173">La extensión de nombre de archivo suele ser. JPF o. jpx.</span><span class="sxs-lookup"><span data-stu-id="58ecc-173">The file name extension is usually .jpf or .jpx.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**\_imagen FORMATCODE de WMDM \_ \_ reservada en \_ primer lugar**</span><span class="sxs-lookup"><span data-stu-id="58ecc-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-175">Código de formato que es el primero de un intervalo reservado para una referencia de imagen en PTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-175">Format code that is the first in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**\_última imagen de FORMATCODE de WMDM \_ \_ reservada \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-177">Código de formato que es el último de un intervalo reservado para una referencia de imagen en PTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-177">Format code that is the last in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**\_FORMATCODE \_ UNDEFINEDFIRMWARE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM\_FORMATCODE\_UNDEFINEDFIRMWARE**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-179">Dar formato al código cuando el firmware no está definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-179">Format code when firmware is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ FORMATCODE \_ WBMP**</span><span class="sxs-lookup"><span data-stu-id="58ecc-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span> **WMDM\_FORMATCODE\_WBMP**</span></span> 
</dt> <dd>

<span data-ttu-id="58ecc-181">Código de formato para una imagen de mapa de bits del Protocolo de aplicación inalámbrica (. WBMP).</span><span class="sxs-lookup"><span data-stu-id="58ecc-181">Format code for a Wireless Application Protocol Bitmap (.wbmp) image.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ FORMATCODE \_ JPEGXR**</span><span class="sxs-lookup"><span data-stu-id="58ecc-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span> **WMDM\_FORMATCODE\_JPEGXR**</span></span> 
</dt> <dd>

<span data-ttu-id="58ecc-183">Dar formato al código para una imagen fotográfica HD</span><span class="sxs-lookup"><span data-stu-id="58ecc-183">Format code for an HD Photo image</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**\_FORMATCODE \_ WINDOWSIMAGEFORMAT de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-185">Código de formato para el formato de imagen de Windows.</span><span class="sxs-lookup"><span data-stu-id="58ecc-185">Format code for Windows image format.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**\_FORMATCODE \_ UNDEFINEDAUDIO de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM\_FORMATCODE\_UNDEFINEDAUDIO**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-187">Código de formato para un archivo de audio de tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-187">Format code for an audio file of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**FORMATCODE de WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM\_FORMATCODE\_WMA**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-189">Código de formato para un archivo Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="58ecc-189">Format code for a Windows Media Audio (WMA) file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**\_FORMATCODE \_ OGG de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM\_FORMATCODE\_OGG**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-191">Código de formato para un archivo de audio codificado en Vorbis en un contenedor OGG.</span><span class="sxs-lookup"><span data-stu-id="58ecc-191">Format code for a Vorbis-encoded audio file in an Ogg container.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**\_AAC FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM\_FORMATCODE\_AAC**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-193">Código de formato para un archivo AAC (codificación de audio avanzado).</span><span class="sxs-lookup"><span data-stu-id="58ecc-193">Format code for an Advanced Audio Coding (AAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**FORMATCODE de WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM\_FORMATCODE\_AUDIBLE**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-195">Código de formato para un archivo audible.</span><span class="sxs-lookup"><span data-stu-id="58ecc-195">Format code for an Audible file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**\_FORMATCODE \_ FLAC de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM\_FORMATCODE\_FLAC**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-197">Código de formato para un archivo de códec de audio sin pérdida (FLAC).</span><span class="sxs-lookup"><span data-stu-id="58ecc-197">Format code for a Free Lossless Audio Codec (FLAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ FORMATCODE \_ QCELP**</span><span class="sxs-lookup"><span data-stu-id="58ecc-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span> **WMDM\_FORMATCODE\_QCELP**</span></span> 
</dt> <dd>

<span data-ttu-id="58ecc-199">Código de formato para un archivo de códec de predicción lineal (QCELP) de Qualcomm Code entusiasmado.</span><span class="sxs-lookup"><span data-stu-id="58ecc-199">Format code for a Qualcomm Code Excited Linear Prediction (QCELP) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ \_AMR FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="58ecc-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span> **WMDM\_FORMATCODE\_AMR**</span></span> 
</dt> <dd>

<span data-ttu-id="58ecc-201">Código de formato para un archivo de códec de audio de varias velocidades adaptable (AMR).</span><span class="sxs-lookup"><span data-stu-id="58ecc-201">Format code for an Adaptive Multi-Rate audio (AMR) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**\_FORMATCODE \_ UNDEFINEDVIDEO de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM\_FORMATCODE\_UNDEFINEDVIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-203">Dar formato al código para un archivo de vídeo con un tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-203">Format code for a video file with an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**FORMATCODE de WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM\_FORMATCODE\_WMV**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-205">Código de formato para un archivo Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="58ecc-205">Format code for a Windows Media Video (WMV) file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**\_FORMATCODE \_ MP4 de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM\_FORMATCODE\_MP4**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-207">Código de formato para un archivo MP4.</span><span class="sxs-lookup"><span data-stu-id="58ecc-207">Format code for an MP4 file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**FORMATCODE de WMDM y \_ \_ MP2**</span><span class="sxs-lookup"><span data-stu-id="58ecc-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM\_FORMATCODE\_MP2**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-209">Código de formato para un archivo MP2.</span><span class="sxs-lookup"><span data-stu-id="58ecc-209">Format code for an MP2 file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ FORMATCODE \_ 3g2**</span><span class="sxs-lookup"><span data-stu-id="58ecc-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span> **WMDM\_FORMATCODE\_3G2**</span></span> 
</dt> <dd>

<span data-ttu-id="58ecc-211">Código de formato para un formato de contenedor multimedia 3G2 (3GPP2).</span><span class="sxs-lookup"><span data-stu-id="58ecc-211">Format code for a 3G2 (3GPP2) multimedia container format.</span></span> <span data-ttu-id="58ecc-212">Un archivo de este tipo puede contener audio, vídeo o texto.</span><span class="sxs-lookup"><span data-stu-id="58ecc-212">A file of this type may contain audio, video, or text.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ FORMATCODE \_ AVCHD**</span><span class="sxs-lookup"><span data-stu-id="58ecc-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span> **WMDM\_FORMATCODE\_AVCHD**</span></span> 
</dt> <dd>

<span data-ttu-id="58ecc-214">Código de formato para un archivo de vídeo AVCHD (codificación avanzada de vídeo de alta definición).</span><span class="sxs-lookup"><span data-stu-id="58ecc-214">Format code for an AVCHD (Advanced Video Coding High Definition) video file.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ FORMATCODE \_ ATSC**</span><span class="sxs-lookup"><span data-stu-id="58ecc-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span> **WMDM\_FORMATCODE\_ATSCTS**</span></span> 
</dt> <dd>

<span data-ttu-id="58ecc-216">Código de formato para el formato estándar del Comité de sistemas de televisión avanzado (ATSC).</span><span class="sxs-lookup"><span data-stu-id="58ecc-216">Format code for the Advanced Television Systems Committee (ATSCTS) format standard.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ FORMATCODE \_ DVBTS**</span><span class="sxs-lookup"><span data-stu-id="58ecc-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span> **WMDM\_FORMATCODE\_DVBTS**</span></span> 
</dt> <dd>

<span data-ttu-id="58ecc-218">Código de formato para un vídeo MPEG-2 y MPEG-1 capa II, o audio AC-3, dentro de una secuencia de transporte MPEG-2 compatible con DVB.</span><span class="sxs-lookup"><span data-stu-id="58ecc-218">Format code for an MPEG-2 video and MPEG-1 Layer II, or AC-3, audio within a DVB-compliant MPEG-2 Transport Stream.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**\_FORMATCODE \_ UNDEFINEDCOLLECTION de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM\_FORMATCODE\_UNDEFINEDCOLLECTION**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-220">Código de formato para una colección de un tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-220">Format code for a collection of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**\_FORMATCODE \_ ABSTRACTMULTIMEDIAALBUM de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTMULTIMEDIAALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-222">Código de formato para un álbum multimedia en el que el objeto contiene las propiedades de un álbum multimedia y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-222">Format code for a multimedia album where the object contains the properties of a multimedia album and, optionally, data.</span></span> <span data-ttu-id="58ecc-223">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-223">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**\_FORMATCODE \_ ABSTRACTIMAGEALBUM de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM\_FORMATCODE\_ABSTRACTIMAGEALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-225">Código de formato para un álbum de imagen donde el objeto contiene las propiedades de un álbum de imagen y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-225">Format code for an image album where the object contains the properties of an image album and, optionally, data.</span></span> <span data-ttu-id="58ecc-226">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-226">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**\_FORMATCODE \_ ABSTRACTAUDIOALBUM de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-228">Código de formato para un álbum de audio donde el objeto contiene las propiedades de un álbum de audio y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-228">Format code for an audio album where the object contains the properties of an audio album and, optionally, data.</span></span> <span data-ttu-id="58ecc-229">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-229">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**\_FORMATCODE \_ ABSTRACTVIDEOALBUM de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTVIDEOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-231">Código de formato para un álbum de vídeo en el que el objeto contiene las propiedades de un álbum de vídeo y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-231">Format code for a video album where the object contains the properties of a video album and, optionally, data.</span></span> <span data-ttu-id="58ecc-232">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-232">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**\_FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-234">Código de formato para una lista de reproducción de audio o vídeo donde el objeto contiene las propiedades de una lista de reproducción de audio/vídeo y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-234">Format code for an audio/video playlist where the object contains the properties of an audio/video playlist and, optionally, data.</span></span> <span data-ttu-id="58ecc-235">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-235">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**\_FORMATCODE \_ ABSTRACTCONTACTGROUP de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACTGROUP**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-237">Dar formato al código para un grupo de contactos donde el objeto contiene las propiedades de un grupo de contactos y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-237">Format code for a contact group where the object contains the properties of a contact group and, optionally, data.</span></span> <span data-ttu-id="58ecc-238">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-238">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**\_FORMATCODE \_ ABSTRACTMESSAGEFOLDER de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGEFOLDER**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-240">Código de formato para una carpeta de mensajes donde el objeto contiene las propiedades de una carpeta de mensajes y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-240">Format code for a message folder where the object contains the properties of a message folder and, optionally, data.</span></span> <span data-ttu-id="58ecc-241">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-241">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**\_FORMATCODE \_ ABSTRACTCHAPTEREDPRODUCTION de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM\_FORMATCODE\_ABSTRACTCHAPTEREDPRODUCTION**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-243">Código de formato para una producción en capítulo en la que el objeto contiene las propiedades de una producción de capítulo y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-243">Format code for a chaptered production where the object contains the properties of a chaptered production and, optionally, data.</span></span> <span data-ttu-id="58ecc-244">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-244">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**\_FORMATCODE \_ WPLPLAYLIST de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM\_FORMATCODE\_WPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-246">Código de formato para una lista de reproducción formateada con formato de lista de reproducción de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="58ecc-246">Format code for a playlist formatted with Windows Media playlist formatting.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**\_FORMATCODE \_ M3UPLAYLIST de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM\_FORMATCODE\_M3UPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-248">Dar formato al código de una lista de reproducción con formato M3U.</span><span class="sxs-lookup"><span data-stu-id="58ecc-248">Format code for a playlist with M3U formatting.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**\_FORMATCODE \_ MPLPLAYLIST de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM\_FORMATCODE\_MPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-250">Dar formato al código para una lista de reproducción con formato MPL.</span><span class="sxs-lookup"><span data-stu-id="58ecc-250">Format code for a playlist with MPL formatting.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**\_FORMATCODE \_ ASXPLAYLIST de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM\_FORMATCODE\_ASXPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-252">Dar formato al código para una lista de reproducción con formato ASX.</span><span class="sxs-lookup"><span data-stu-id="58ecc-252">Format code for a playlist with ASX formatting.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**\_FORMATCODE \_ PLSPLAYLIST de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM\_FORMATCODE\_PLSPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-254">Dar formato al código para una lista de reproducción con formato esperen.</span><span class="sxs-lookup"><span data-stu-id="58ecc-254">Format code for a playlist with PLS formatting.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**\_FORMATCODE \_ UNDEFINEDDOCUMENT de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM\_FORMATCODE\_UNDEFINEDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-256">Código de formato para un documento de tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-256">Format code for a document of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**\_FORMATCODE \_ ABSTRACTDOCUMENT de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM\_FORMATCODE\_ABSTRACTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-258">Código de formato para un documento en el que el objeto contiene las propiedades de un documento y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-258">Format code for a document where the object contains the properties of a document and, optionally, data.</span></span> <span data-ttu-id="58ecc-259">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-259">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**\_XMLDOCUMENT FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM\_FORMATCODE\_XMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-261">Dar formato al código para un documento XML.</span><span class="sxs-lookup"><span data-stu-id="58ecc-261">Format code for an XML document.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**\_FORMATCODE \_ MICROSOFTWORDDOCUMENT de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM\_FORMATCODE\_MICROSOFTWORDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-263">Dar formato al código para un documento de Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="58ecc-263">Format code for a Microsoft Word document.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**\_FORMATCODE \_ MHTCOMPILEDHTMLDOCUMENT de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM\_FORMATCODE\_MHTCOMPILEDHTMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-265">Código de formato para un documento HTML compilado.</span><span class="sxs-lookup"><span data-stu-id="58ecc-265">Format code for a compiled HTML document.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**\_FORMATCODE \_ MICROSOFTEXCELSPREADSHEET de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM\_FORMATCODE\_MICROSOFTEXCELSPREADSHEET**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-267">Dar formato al código para una hoja de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="58ecc-267">Format code for a Microsoft Excel spreadsheet.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**\_FORMATCODE \_ MICROSOFTPOWERPOINTDOCUMENT de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM\_FORMATCODE\_MICROSOFTPOWERPOINTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-269">Dar formato al código para un documento de Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="58ecc-269">Format code for a Microsoft PowerPoint document.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**\_FORMATCODE \_ UNDEFINEDMESSAGE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM\_FORMATCODE\_UNDEFINEDMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-271">Código de formato para un mensaje de tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-271">Format code for a message of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**\_FORMATCODE \_ ABSTRACTMESSAGE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-273">Código de formato para un mensaje en el que el objeto contiene las propiedades de un mensaje y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-273">Format code for a message where the object contains the properties of a message and, optionally, data.</span></span> <span data-ttu-id="58ecc-274">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-274">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**\_FORMATCODE \_ UNDEFINEDCONTACT de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM\_FORMATCODE\_UNDEFINEDCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-276">Código de formato para un contacto de tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-276">Format code for a contact of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**\_FORMATCODE \_ ABSTRACTCONTACT de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-278">Código de formato para un contacto en el que el objeto contiene las propiedades de un contacto y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-278">Format code for a contact where the object contains the properties of a contact and, optionally, data.</span></span> <span data-ttu-id="58ecc-279">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-279">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**\_FORMATCODE \_ VCARD2 de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM\_FORMATCODE\_VCARD2**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-281">Dar formato al código para una tarjeta electrónica con formato vCard versión 2.</span><span class="sxs-lookup"><span data-stu-id="58ecc-281">Format code for an electronic card with vcard version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**\_FORMATCODE \_ VCARD3 de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM\_FORMATCODE\_VCARD3**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-283">Dar formato al código para una tarjeta electrónica con formato vCard versión 3.</span><span class="sxs-lookup"><span data-stu-id="58ecc-283">Format code for an electronic card with vcard version 3 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**\_FORMATCODE \_ UNDEFINEDCALENDARITEM de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM\_FORMATCODE\_UNDEFINEDCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-285">Código de formato para un elemento de calendario electrónico de tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-285">Format code for an electronic calendar item of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**\_FORMATCODE \_ ABSTRACTCALENDARITEM de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM\_FORMATCODE\_ABSTRACTCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-287">Código de formato para un elemento de calendario en el que el objeto contiene las propiedades de un elemento de calendario y, opcionalmente, los datos.</span><span class="sxs-lookup"><span data-stu-id="58ecc-287">Format code for a calendar item where the object contains the properties of a calendar item and, optionally, data.</span></span> <span data-ttu-id="58ecc-288">Los datos contenidos tienen un formato no definido con respecto a la especificación MTP.</span><span class="sxs-lookup"><span data-stu-id="58ecc-288">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**\_FORMATCODE \_ VCALENDAR1 de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM\_FORMATCODE\_VCALENDAR1**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-290">Código de formato para un elemento de calendario electrónico con formato vCalendar versión 1.</span><span class="sxs-lookup"><span data-stu-id="58ecc-290">Format code for an electronic calendar item with vcalendar version 1 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**\_FORMATCODE \_ VCALENDAR2 de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM\_FORMATCODE\_VCALENDAR2**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-292">Código de formato para un elemento de calendario electrónico con formato vCalendar versión 2.</span><span class="sxs-lookup"><span data-stu-id="58ecc-292">Format code for an electronic calendar item with vcalendar version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**\_FORMATCODE \_ UNDEFINEDWINDOWSEXECUTABLE de WMDM**</span><span class="sxs-lookup"><span data-stu-id="58ecc-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM\_FORMATCODE\_UNDEFINEDWINDOWSEXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-294">Código de formato para un ejecutable basado en Windows de tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="58ecc-294">Format code for a Windows-based executable of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**\_ \_ conversión multimedia FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM\_FORMATCODE\_MEDIA\_CAST**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-296">Código de formato para un objeto de conversión de multimedia.</span><span class="sxs-lookup"><span data-stu-id="58ecc-296">Format code for a media cast object.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_sección FORMATCODE de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="58ecc-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**WMDM\_FORMATCODE\_SECTION**</span></span>
</dt> <dd>

<span data-ttu-id="58ecc-298">Código de formato para una sección de datos que se encuentra en otro objeto.</span><span class="sxs-lookup"><span data-stu-id="58ecc-298">Format code for a section of data that is contained in another object.</span></span>

</dd> <dt>

<span data-ttu-id="58ecc-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ FORMATCODE \_ 3G2A**</span><span class="sxs-lookup"><span data-stu-id="58ecc-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span> **WMDM\_FORMATCODE\_3G2A**</span></span> 
</dt> <dd>

<span data-ttu-id="58ecc-300">Código de formato para un formato de contenedor multimedia 3G2A (3GPP2A).</span><span class="sxs-lookup"><span data-stu-id="58ecc-300">Format code for a 3G2A (3GPP2A) multimedia container format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58ecc-301">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58ecc-301">Remarks</span></span>

<span data-ttu-id="58ecc-302">Para detectar los formatos admitidos por un dispositivo, una aplicación puede usar [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para consultar la propiedad del dispositivo **g \_ wszWMDMFormatsSupported** .</span><span class="sxs-lookup"><span data-stu-id="58ecc-302">To discover the formats supported by a device, an application can use [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to query the **g\_wszWMDMFormatsSupported** device property.</span></span>

<span data-ttu-id="58ecc-303">Para detectar las capacidades del dispositivo para un formato determinado, una aplicación puede llamar a [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="58ecc-303">To discover device capabilities for a particular format, an application can call [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span>

<span data-ttu-id="58ecc-304">Una aplicación puede establecer el código de formato al crear un almacenamiento en el dispositivo incluyendo la propiedad **g \_ wszWMDMFormatCode** en los metadatos pasados en el parámetro *pMetaData* de una llamada a [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span><span class="sxs-lookup"><span data-stu-id="58ecc-304">An application can set the format code while creating a storage on device by including the **g\_wszWMDMFormatCode** property in metadata passed in the *pMetaData* parameter of a call to [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span>

<span data-ttu-id="58ecc-305">Una aplicación puede consultar el código de formato de un almacenamiento llamando a [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) y recuperando la propiedad **g \_ wszWMDMFormatCode** .</span><span class="sxs-lookup"><span data-stu-id="58ecc-305">An application can query the format code of a storage by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) and retrieving the **g\_wszWMDMFormatCode** property.</span></span>

<span data-ttu-id="58ecc-306">Si el dispositivo admite el establecimiento del código de formato después de la creación de almacenamiento, una aplicación puede usar [**IWMDMStorage3:: setMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) para establecer la propiedad **g \_ wszWMDMFormatCode** .</span><span class="sxs-lookup"><span data-stu-id="58ecc-306">If the device supports setting the format code after the creation of storage, an application can use [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) to set the **g\_wszWMDMFormatCode** property.</span></span> <span data-ttu-id="58ecc-307">Es posible que algunos dispositivos no permitan cambiar el código de formato una vez creado el almacenamiento en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58ecc-307">Some devices may not allow changing the format code after the storage is created on the device.</span></span> <span data-ttu-id="58ecc-308">Por lo tanto, se recomienda encarecidamente establecer esta propiedad junto con los metadatos pasados en [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) .</span><span class="sxs-lookup"><span data-stu-id="58ecc-308">Therefore, setting this property along with the metadata passed in [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) is strongly recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ecc-309">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58ecc-309">Requirements</span></span>



| <span data-ttu-id="58ecc-310">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ecc-310">Requirement</span></span> | <span data-ttu-id="58ecc-311">Value</span><span class="sxs-lookup"><span data-stu-id="58ecc-311">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="58ecc-312">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58ecc-312">Header</span></span><br/> | <dl> <span data-ttu-id="58ecc-313"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="58ecc-313"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ecc-314">Vea también</span><span class="sxs-lookup"><span data-stu-id="58ecc-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ecc-315">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="58ecc-315">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="58ecc-316">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="58ecc-316">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="58ecc-317">**IWMDMDevice3:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="58ecc-317">**IWMDMDevice3::GetProperty**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[<span data-ttu-id="58ecc-318">**IWMDMStorage3:: GetMetadata**</span><span class="sxs-lookup"><span data-stu-id="58ecc-318">**IWMDMStorage3::GetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[<span data-ttu-id="58ecc-319">**IWMDMStorage3::SetMetadata**</span><span class="sxs-lookup"><span data-stu-id="58ecc-319">**IWMDMStorage3::SetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[<span data-ttu-id="58ecc-320">**IWMDMStorage4::GetSpecifiedMetadata**</span><span class="sxs-lookup"><span data-stu-id="58ecc-320">**IWMDMStorage4::GetSpecifiedMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[<span data-ttu-id="58ecc-321">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="58ecc-321">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[<span data-ttu-id="58ecc-322">**Constantes de metadatos**</span><span class="sxs-lookup"><span data-stu-id="58ecc-322">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 





