---
description: Trabajar con tipos DMO multimedia
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Trabajar con tipos DMO multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a75d7eb65e92a89d5d413d8cc04a7dbb9f1891d6b23a9cc3c1242fbae46f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100927"
---
# <a name="working-with-dmo-media-types"></a>Trabajar con tipos DMO multimedia

Los tipos de medios de entrada y salida que usan las DDO de códec se definen mediante DMO [**\_ estructura MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Esta estructura es idéntica a [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), que se define en el SDK de formato multimedia de Windows y [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), que se define en Microsoft DirectShow®. En función de la aplicación, puede usar variables definidas como cualquiera de estos tres tipos. Es seguro convertir un puntero a una de las estructuras de tipo de medio como otra. Por ejemplo:


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



Los tipos de formato que usan los códecs suelen limitarse a los descritos por las estructuras **VIDEOINFOHEADER** **y MPEGATEX.** Para mayor comodidad, las constantes para estos tipos de formato se incluyen en el archivo de encabezado wmcodecconst.h. Los nombres constantes son WMCFORMAT \_ VideoInfo y WMCFORMAT \_ WaveFormatEx, respectivamente. Los códecs de audio pueden funcionar con la **estructura MPEGATEXTENSIBLE** en algunas circunstancias y deben usarlo en otras. Sin **embargo, DMO \_ media \_ type.formattype** se establece en el mismo valor que para **LA MARCA DE ONDAATEX**. Para obtener más información sobre el uso **de WAVEFORMATEXTENSIBLE**, vea [Using High-Definition Audio](usinghighdefinitionaudio.md).

> [!Note]  
>    Debe incluir la estructura de tipo de formato utilizada como salida del codificador en cualquier contenedor que use para almacenar los datos comprimidos. Los descodificadores requieren la estructura de formato original para descomprimir el contenido. Además de los miembros de la estructura , los tipos comprimidos Windows audio multimedia y vídeo requieren información de formato adicional, que se anexa a la estructura . Para obtener más información, [vea Trabajar con audio](workingwithaudio.md) y Trabajar con [vídeo.](workingwithvideo.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con DDO de códec](workingwithcodecdmos.md)
</dt> </dl>

 

 
