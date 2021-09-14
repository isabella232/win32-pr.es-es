---
description: Información general de DXVA 2 y su relación con DXVA 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: Acerca de DXVA 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f622c863f433be44bbce6460024ffb06bb1b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269436"
---
# <a name="about-dxva-20"></a>Acerca de DXVA 2.0

DirectX Video Acceleration (DXVA) es una API y un DDI correspondiente para usar la aceleración de hardware para acelerar el procesamiento de vídeo. Los códecs de software y los procesadores de vídeo de software pueden usar DXVA para descargar determinadas operaciones que consumen mucha CPU en la GPU. Por ejemplo, un descodificador de software puede descargar la transformación inversa de coseno discreto (iDCT) en la GPU.

En DXVA, algunas operaciones de decodificación se implementan mediante el controlador de hardware gráfico. Este conjunto de funcionalidades se denomina *acelerador*. Otras operaciones de descodificación se implementan mediante software de aplicación en modo de usuario, denominado descodificador *de host* o *descodificador de software*. (Los términos *descodificador de* *host y descodificador de software* son equivalentes). El procesamiento realizado por el acelerador se denomina *procesamiento fuera del host.* Normalmente, el acelerador usa la GPU para acelerar algunas operaciones. Cada vez que el acelerador realiza una operación de descodificación, el descodificador host debe transmitir a los búferes del acelerador que contienen la información necesaria para realizar la operación.

La API de DXVA 2 requiere Windows Vista o posterior. La API DXVA 1 todavía se admite en Windows Vista por compatibilidad con versiones anteriores. Se proporciona una capa de emulación que convierte entre cualquiera de las versiones de la API y la versión opuesta del DDI:

-   Si el controlador de gráficos se ajusta Windows modelo de controlador de pantalla (WDDM), las llamadas API de DXVA 1 se convierten en llamadas DDI de DXVA 2.
-   Si los controladores de gráficos usan el modelo Windows XP Display Driver Model (XPDM), las llamadas API de DXVA 2 se convierten en llamadas DDI de DXVA 1.

En la tabla siguiente se muestran los requisitos del sistema operativo y los representadores de vídeo admitidos para cada versión de la API de DXVA.



| Versión de la API | Requisitos          | Compatibilidad con el representador de vídeo                        |
|-------------|-----------------------|-----------------------------------------------|
| DXVA 1      | Windows 2000 o posterior | Overlay Mixer, VMR-7, VMR-9 (solo DirectShow) |
| DXVA 2      | Windows Vista         | EVR (DirectShow y Media Foundation)         |



 

En DXVA 1, el descodificador de software debe acceder a la API a través del representador de vídeo. No hay ninguna manera de usar la API dxva 1 sin llamar al representador de vídeo. Esta limitación se ha eliminado con DXVA 2. Con DXVA 2, el descodificador de host (o cualquier aplicación) puede acceder directamente a la API a través de la interfaz [**IDirectXVideoDecoderService.**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)

En la documentación de DXVA 1 se describen las estructuras decoding que se usan para los siguientes estándares de vídeo:

-   ITU-T Rec. H.261
-   ITU-T Rec. H.263
-   Vídeo MPEG-1
-   Vídeo del perfil principal de MPEG-2

Las especificaciones siguientes definen extensiones DXVA para otros estándares de vídeo:

-   [Especificación de DXVA para lacodización H.264/AVC](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [Especificación DXVA para codificación de vídeo multivista (MVC) de AVC H.264/MPEG-4, incluido el perfil alto estéreo](https://www.microsoft.com/download/details.aspx?id=25200)
-   [Especificación DXVA para MPEG-1 VLD y la codificación de vídeo VLD MPEG-1/MPEG-2 combinada.](https://www.microsoft.com/download/details.aspx?id=9374)
-   [Especificación DXVA Off-Host modo VLD para la codificación de vídeo MPEG-4, parte 2](https://www.microsoft.com/download/details.aspx?id=21100)
-   [Especificación de DXVA para Windows Media Video® v8, v9 y la decodización de vA (incluido SMPTE 421M "VC-1")](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [Especificación de aceleración de vídeo directX (DXVA) para codificación de vídeo escalable (SVC) de H.264/MPEG-4 Off-Host de modo VLD](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [Especificación de aceleración de vídeo de DirectX para codificación de vídeo VP8 y VP9](https://www.microsoft.com/download/details.aspx?id=49188)

DXVA 1 y DXVA 2 usan las mismas estructuras de datos para la decodificación. Sin embargo, el procedimiento para configurar la sesión de decoding ha cambiado. DXVA 1 usa un mecanismo de "sondeo y bloqueo", en el que el descodificador de host puede probar varias configuraciones antes de establecer la configuración deseada en el acelerador. En DXVA 2, el acelerador devuelve una lista de configuraciones admitidas y el descodificador de host selecciona una de la lista. En las secciones siguientes se proporciona información detallada:

-   [Compatibilidad con DXVA 2.0 en DirectShow](supporting-dxva-2-0-in-directshow.md)
-   [Compatibilidad con DXVA 2.0 en Media Foundation](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Especificación dxva 1.0](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
