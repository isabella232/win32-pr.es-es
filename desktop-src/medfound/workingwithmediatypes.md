---
description: Trabajar con tipos de medios DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Trabajar con tipos de medios DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003339"
---
# <a name="working-with-dmo-media-types"></a>Trabajar con tipos de medios DMO

Los tipos de medios de entrada y salida utilizados por el códec DMOs se definen mediante la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Esta estructura es idéntica a la de ambos [**\_ \_ tipos de medios de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), que se define en el SDK de Windows Media Format y el [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type), que se define en Microsoft DirectShow®. Dependiendo de la aplicación, puede usar variables definidas como cualquiera de estos tres tipos. Es seguro convertir un puntero a una de las estructuras de tipo de medio como otro. Por ejemplo:


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



Los tipos de formato que usan los códecs generalmente se limitan a los descritos por las estructuras **VIDEOINFOHEADER** y **WAVEFORMATEX** . Para mayor comodidad, las constantes para estos tipos de formato se incluyen en el archivo de encabezado wmcodecconst. h. Los nombres de constantes son WMCFORMAT \_ videoinfo y WMCFORMAT \_ WaveFormatEx, respectivamente. Los códecs de audio pueden trabajar con la estructura **WAVEFORMATEXTENSIBLE** en algunas circunstancias y deben usarlo en otras personas. Sin embargo, el **\_ tipo de medios DMO \_ . FormatType** se establece en el mismo valor que para **WAVEFORMATEX**. Para obtener más información sobre el uso de **WAVEFORMATEXTENSIBLE**, consulte [uso de High-Definition audio](usinghighdefinitionaudio.md).

> [!Note]  
>    Debe incluir la estructura de tipo de formato utilizada como salida del codificador en cualquier contenedor que use para almacenar los datos comprimidos. Los descodificadores requieren la estructura de formato original para descomprimir el contenido. Además de los miembros de la estructura, los tipos de vídeo y Windows Media Audio comprimidos requieren información de formato adicional, que se anexa a la estructura. Para obtener más información, consulte [trabajar con audio](workingwithaudio.md) y [trabajar con vídeo](workingwithvideo.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
