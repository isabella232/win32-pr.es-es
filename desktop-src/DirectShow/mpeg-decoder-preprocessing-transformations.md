---
description: Transformaciones de preprocesamiento del descodificador MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Transformaciones de preprocesamiento del descodificador MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908903"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a>Transformaciones de preprocesamiento del descodificador MPEG

**Letterbox y PanScan**

La imagen de 4x3 se puede formar mediante el relleno de la parte superior e inferior de la imagen (denominada imagen letterbox) o mediante la extracción de una parte 4x3 de la imagen (denominada imagen de PanScan). Los menús y las secuencias de subimagen se sobrelagen encima de la imagen de vídeo final. Las imágenes de proporción de 16 x 9 se almacenan en un formato anamórfico de 4x3. La extensión del vídeo de origen anamórfico de relación de aspecto 4x3 de 720 x 480 a una relación de aspecto de 16 x 9 forma la imagen de aspecto original de 16 x 9.

A continuación se muestra una descripción de cómo mostrar correctamente cada uno de los modos y sus aspectos destacados:

-   **Widescreen:** El vídeo de origen se extendió en el área más grande de 16 x 9 de la ventana de salida. Los resaltados son relativos al interior del área 16x9. Las barras negras se deben agregar a la parte superior e inferior o a los lados para mantener un área de 16 x 9.
-   **Examen de panorámica:** En el vídeo de 16x9, use el desplazamiento horizontal proporcionado en la secuencia MPEG2 para extraer una subventana 4x3. Coloque la subventana 4x3 en el área 4x3 más grande de la ventana del cliente de salida. Las coordenadas del resaltado son relativas a la ventana de salida 4x3 y no tienen ninguna relación con el vídeo de origen 16x9. Las barras negras se deben agregar a la parte superior e inferior o a los lados para mantener un área de 4x3.
-   **Cuadro de letras:** Calcule el área 4x3 más grande de la ventana de salida. Las barras negras se deben agregar a la parte superior e inferior o a los lados para mantener un área de 4x3. El vídeo anamórfico de origen 4x3 (que representa una imagen de 16 x 9) se coloca en la subventana 16x9 más grande dentro del área 4x3. Las barras negras se deben agregar a la parte superior e inferior de la subventana para mantener un área de 16 x 9. Las coordenadas del resaltado son relativas al área 4x3 y no tienen ninguna relación con el vídeo de origen 16x9. Es posible que un disco especifique un resaltado que se encuentra fuera del área 16x9 (pero todavía en la ventana 4x3). Para el vídeo 4x3, el vídeo se coloca en el área de salida 4x3 más grande de la ventana del cliente de salida. Las barras negras se deben agregar a la parte superior e inferior o a los lados para mantener un área de 4x3.

**Preprocesamiento MPEG con DVD Navigator y VMR**

Actualmente, al descodificador se le pasa un tipo de medio FORMAT \_ MPEG2 \_ VIDEO (cuyo bloque de formato apunta a una [**estructura MPEG2VIDEOINFO).**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) En los pines de salida, el descodificador genera un tipo de medio FORMAT VideoInfo2, cuyo bloque de formato apunta \_ a una [**estructura VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Se ha cambiado el nombre del **campo dwReserved de** la estructura a **marcas dwControls.**

El **miembro dwControlFlags** ahora contendrá los nuevos bits.



| Etiqueta | Value |
|--------------------------|------------|
| AMCONTROL \_ USADO          | 0x00000001 |
| AMCONTROL \_ PAD \_ TO \_ 4x3  | 0x00000002 |
| AMCONTROL \_ PAD \_ TO \_ 16x9 | 0x00000004 |



 

AMCONTROL \_ USED se usa para probar si se admiten estas nuevas marcas. Un filtro de origen debe establecer la marca AMCONTROL USED y ver si QueryAccept(MediaType) se realiza correctamente \_ en la marca de nivel inferior. Si se rechaza, no se pueden usar las marcas AMCONTROL y dwReserved1 debe establecerse en 0.

AMCONTROL PAD TO 4x3 indica que la imagen se debe agregar y \_ mostrar en un área de \_ \_ 4x3.

AMCONTROL PAD TO 16x9 indica que la imagen se debe agregar y \_ mostrar en un área de \_ \_ 16 x 9.

El descodificador debe copiar o procesar los bits de forma invidente. Si el descodificador realiza la conversión de letras por sí mismo, debe modificar la relación de aspecto de los píxeles, agregar la imagen y quitar los bits de AMCONTROL \_ \* correspondientes.

MPEG2VIDEOINFO.dwFlags ahora contiene tres marcas para controlar cómo se debe mostrar el contenido:

-   `AMMPEG2_DoPanScan (0x00000001)`: si se establece esta marca, el descodificador de vídeo MPEG-2 debe recortar la imagen de salida en función de los vectores de examen pan en la extensión de visualización de imagen y cambiar la relación de aspecto de la imagen a \_ \_ 4x3. El VMR no debe recibir un ejemplo de 16 x 9 con esta marca. Una implementación simple podría modificar el rectángulo de origen para indicar una región de origen de 540 anchos con un borde izquierdo igual al desplazamiento de presentación en la extensión de visualización \_ de \_ imagen.
-   `AMMPEG2_LetterboxAnalogOut (0x00000020)`: cuando un descodificador de hardware muestra esta secuencia en una salida de vídeo (normalmente un conector SVIDEO en la tarjeta), debe aplicar las reglas para mostrar un ejemplo de 16x9 en una pantalla de 4x3.

    Un descodificador de software (o un descodificador de hardware que genera la salida enviada al VMR) tiene dos opciones al procesar imágenes:

    1.  Ignore esta marca y pase el contenido de VideoInfoHeader2 a VMR (la marca AMCONTROL \_ PAD \_ TO \_ 4x3 [](dvd-navigator-filter.md) ya la establecerá el navegador de DVD en el ejemplo). El VMR encontrará un ejemplo de vídeo de 16 x 9 con la marca AMCONTROL PAD TO 4x3 establecida y una secuencia \_ \_ de \_ subapicture 4x3. La aplicación debe establecer los rectángulos de destino normalizados de salida de las dos secuencias para que sean del mismo ancho.
    2.  Convierta la secuencia anamórfica en una imagen de 4x3 mediante el relleno de la parte superior e inferior de la imagen y el establecimiento de la relación de aspecto de la imagen en 4x3 (consulte Letterbox más arriba) y quitando el PANEL DE AMCONTROL a \_ \_ \_ 4x3 bits de VIDEOINFOHEADER2.

    Los descodificadores de DirectXVA que mezclan los flujos de vídeo y subpicture tendrán que procesar esta marca. Si el hardware no puede escalar la subaspección mezclada, el descodificador debe generar una secuencia de subimagen independiente para que vmr se mezcle con el vídeo.

-   `AMMPEG2_WidescreenAnalogOut (0x00000200)`: cuando un descodificador de hardware muestra esta secuencia en una salida de vídeo (normalmente un conector SVIDEO en la tarjeta), debe suponer una pantalla 16x9 (anamórfica).

    Un descodificador de software (o un descodificador de hardware que genera la salida enviada al VMR) tiene dos opciones al procesar una imagen anamórfica:

    1.  Ignore esta marca y copie el contenido de VideoInfoHeader2 en vmr. La VMR va a usar imágenes de 4 x 3 a 16 x 9 si tienen establecido AMCONTROL \_ PAD \_ TO \_ 16x9.
    2.  Ajádala a una imagen de 16 x 9 y quite el PAD DE AMCONTROL \_ \_ A \_ 16 x 9 bits.

La mayoría de los descodificadores deben usar **GetMediaType** para detectar un cambio multimedia en el pin de entrada y copiar el contenido **de VIDEOINFOHEADER2** (incluido en **MPEG2INFOHEADER)** en el pin de salida. Probablemente solo procesarán el bit PanScan.

En el código de ejemplo siguiente se muestra cómo copiar el contenido **de VIDEOINFOHEADER2** de un pin de entrada a un pin de salida.


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



 

 



