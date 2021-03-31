---
description: Transformaciones de preprocesamiento del descodificador de MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Transformaciones de preprocesamiento del descodificador de MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70df51b26ec3fa25d67a03a4e494869a2f25760
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806440"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a>Transformaciones de preprocesamiento del descodificador de MPEG

**Panorámica y PanScan**

Para formar la imagen 4x3, puede rellenar la parte superior e inferior de la imagen (denominada imagen de pantalla ancha) o bien extraer una parte 4x3 de la imagen (denominada imagen de PanScan). Los menús y los flujos de subimagens se superpondrán encima de la imagen de vídeo final. Las imágenes de proporción de 16x9 se almacenan en un formato de 4x3 anamorphic. La expansión del vídeo de origen de la relación de aspecto de anamorphic 4x3 720 x 480 a una relación de aspecto 16x9 forma la imagen de aspecto 16x9 original.

A continuación se muestra una descripción de cómo mostrar correctamente cada uno de los modos y sus aspectos destacados:

-   **Pantalla panorámica:** El vídeo de origen se expande en el área 16x9 más grande de la ventana de salida. Los resaltados son relativos al interior del área 16x9. Las barras negras deben agregarse a la parte superior e inferior, o a los lados, para mantener un área 16x9.
-   **Examen panorámico:** En el vídeo 16x9, use el desplazamiento horizontal proporcionado en el flujo de MPEG2 para extraer una subventana de 4x3. Coloque la subventana 4x3 en el área 4x3 mayor de la ventana del cliente de salida. Las coordenadas del resaltado son relativas a la ventana de salida de 4x3 y no tienen ninguna relación con el vídeo de 16x9 de origen. Las barras negras deben agregarse a la parte superior e inferior, o a los lados, para mantener un área 4x3.
-   **Panorámica:** Calcule el área 4x3 más grande de la ventana de salida. Las barras negras deben agregarse a la parte superior e inferior, o a los lados, para mantener un área 4x3. El vídeo de 4x3 de anamorphic de origen (que representa una imagen 16x9) se coloca en la subventana 16x9 más grande dentro del área 4x3. Las barras negras se deben agregar a la parte superior e inferior de la subventana para mantener un área 16x9. Las coordenadas del resaltado son relativas al área 4x3 y no tienen ninguna relación con el vídeo de 16x9 de origen. Es posible que un disco especifique un resaltado que se encuentra fuera del área 16x9 (pero aún en la ventana 4x3). En el caso de 4x3 video, el vídeo se coloca en el área de salida 4x3 más grande de la ventana del cliente de salida. Las barras negras deben agregarse a la parte superior e inferior, o a los lados, para mantener un área 4x3.

**Preprocesamiento de MPEG con DVD Navigator y VMR**

Actualmente, se pasa al descodificador un \_ tipo de medio de vídeo MPEG2 de formato \_ (cuyo bloque de formato apunta a una estructura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ). En los clavijas de salida, el descodificador genera un formato \_ VideoInfo2 tipo de medio, cuyo bloque Format apunta a una estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Se ha cambiado el nombre del campo **dwReserved** de la estructura a marcas **dwControls** .

El miembro **dwControlFlags** contendrá ahora los nuevos bits.



|                          |            |
|--------------------------|------------|
| AMCONTROL \_ usado          | 0x00000001 |
| AMCONTROL \_ Pad \_ a \_ 4x3  | 0x00000002 |
| AMCONTROL \_ Pad \_ a \_ 16x9 | 0x00000004 |



 

AMCONTROL \_ Used se usa para comprobar si se admiten estas nuevas marcas. Un filtro de origen debe establecer la \_ marca AMCONTROL Used y ver si QueryAccept (mediatype) se realiza correctamente en el PIN de nivel inferior. Si se rechaza, no se pueden usar las marcas AMCONTROL y dwReserved1 debe establecerse en 0.

AMCONTROL \_ Pad \_ to \_ 4x3 indica que la imagen se debe rellenar y mostrar en un área de 4x3.

AMCONTROL \_ Pad \_ to \_ 16x9 indica que la imagen se debe rellenar y mostrar en un área de 16x9.

El descodificador debe copiar o procesar ciegamente los bits. Si el descodificador realiza la panorámica, debe modificar la relación de aspecto de los píxeles, rellenar la imagen y quitar los bits AMCONTROL correspondientes \_ \* .

MPEG2VIDEOINFO. dwFlags contiene ahora tres marcas para controlar el modo en que se debe mostrar el contenido:

-   `AMMPEG2_DoPanScan (0x00000001)`: Si se establece esta marca, el descodificador de vídeo MPEG-2 debe recortar la imagen de salida basada en vectores de recorrido panorámico en la extensión de presentación de imágenes \_ \_ y cambiar la relación de aspecto de la imagen a 4x3. VMR no debe recibir un ejemplo 16x9 con esta marca. Una implementación sencilla podría modificar el rectángulo de origen para indicar una región de origen de 540 de ancho con un borde izquierdo igual al desplazamiento de visualización de la extensión de presentación de imágenes \_ \_ .
-   `AMMPEG2_LetterboxAnalogOut (0x00000020)`: Cuando un descodificador de hardware muestra este flujo en una salida de vídeo (normalmente un conector de SVIDEO en la tarjeta), debe aplicar las reglas para mostrar un ejemplo de 16x9 en una pantalla de 4x3.

    Un descodificador de software (o un descodificador de hardware que genera una salida enviada a la VMR) tiene dos opciones al procesar imágenes:

    1.  Omitir esta marca y pasar el contenido de VideoInfoHeader2 a VMR (la \_ marca de AMCONTROL \_ a \_ 4x3 ya se establecerá mediante el [navegador de DVD](dvd-navigator-filter.md) en el ejemplo). El VMR encontrará un ejemplo de vídeo 16x9 con el panel de AMCONTROL \_ \_ en el \_ marcador de 4x3 establecido y una secuencia de subimagen de 4x3. La aplicación debe establecer los rectángulos de destino normalizados de salida de los dos flujos para que tengan el mismo ancho.
    2.  Convierta el flujo anamorphic en una imagen de 4x3. para ello, rellene la parte superior e inferior de la imagen y establezca la relación de aspecto de la imagen en 4x3 (vea la panorámica anterior) y quite el \_ panel \_ de AMCONTROL \_ de 4X3 bit del VIDEOINFOHEADER2.

    Los descodificadores de DirectXVA que combinan el vídeo y las secuencias de subimagen tendrán que procesar esta marca. Si el hardware no puede escalar la subimagen combinada, el descodificador debe generar una secuencia de subimagen independiente para que la VMR se fusione con el vídeo.

-   `AMMPEG2_WidescreenAnalogOut (0x00000200)`: Cuando un descodificador de hardware muestra esta secuencia en una salida de vídeo (normalmente un conector de SVIDEO en la tarjeta), debe suponer una presentación de 16x9 (anamorphic).

    Un descodificador de software (o un descodificador de hardware que genera una salida enviada a la VMR) tiene dos opciones al procesar una imagen de anamorphic:

    1.  Omita esta marca y copie el contenido de VideoInfoHeader2 en VMR. La VMR rellenará las imágenes de 4x3 en 16x9 si tienen el \_ Panel AMCONTROL \_ en \_ 16x9 establecido.
    2.  Rellene la imagen de salida a una imagen de 16x9 y quite el panel de AMCONTROL \_ \_ a \_ 16x9 bit.

La mayoría de los descodificadores deben usar **GetMediaType** para detectar un cambio de medios en el PIN de entrada y copiar el contenido de **VIDEOINFOHEADER2** (contenido en **MPEG2INFOHEADER**) en el terminal de salida. Probablemente solo procesarán el bit PanScan.

En el ejemplo de código siguiente se muestra cómo copiar el contenido de **VIDEOINFOHEADER2** de un PIN de entrada en un terminal de salida.


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



