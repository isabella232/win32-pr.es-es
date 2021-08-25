---
description: Microsoft Media Foundation es la plataforma multimedia de próxima generación para Windows que permite a los desarrolladores, consumidores y proveedores de contenido adoptar la nueva ola de contenido Premium con una solidez mejorada, una calidad sin precedentes e interoperabilidad sin problemas.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Acerca de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2f8510cc6d967f7a3a809d395f032e277290074002399f9b54e6c54025c312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959655"
---
# <a name="about-media-foundation"></a>Acerca de Media Foundation

Microsoft Media Foundation es la plataforma multimedia de próxima generación para Windows que permite a los desarrolladores, consumidores y proveedores de contenido adoptar la nueva ola de contenido Premium con una solidez mejorada, una calidad sin precedentes e interoperabilidad sin problemas.

Media Foundation requiere Windows Vista o posterior. Usa el modelo de objetos componentes (COM) y requiere C/C++. Microsoft no proporciona una API administrada para Media Foundation.

Las MEDIA FOUNDATION api de datos forman parte del [SDK Windows .](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Para desarrollar una Media Foundation, instale la versión más reciente del SDK de Windows.

## <a name="audio-and-video-quality"></a>Calidad de audio y vídeo

Media Foundation se ha diseñado para satisfacer los desafíos que plantea el contenido de alta definición. Las mejoras de calidad de audio y vídeo realizadas en toda la plataforma ahora hacen posible ofrecer una excelente experiencia para el contenido de alta definición de próxima generación.

-   DirectX Video Acceleration (DXVA) 2.0 ofrece una aceleración de vídeo más eficaz, en comparación con DXVA 1.0, con una decodificación de vídeo más sólida y simplificada y un uso extendido del hardware en el procesamiento de vídeo. Con DXVA 2.0, Windows controlar algunos de los contenidos de alta definición más exigentes con alta calidad y resistencia a problemas mejorados.

-   La información de espacio de color se conserva en toda la canalización de vídeo. Los usuarios pueden disfrutar de contenido de vídeo con total fidelidad. La información de color y las imágenes entrelazadas ahora se pasan al hardware para las composiciones de paso único. La conservación de la información de espacio de color también reduce las conversiones innecesarias de espacio de color, lo que libera más ciclos para procesar contenido hd exigente.
-   El representador de vídeo mejorado (EVR) ofrece una mejor compatibilidad con el control de tiempo, un procesamiento de vídeo mejorado y una mejor resistencia a los problemas. Se ha mejorado la compatibilidad con la reproducción a pantalla completa y se ha minimizado el desgarro de vídeo en modo de ventana.
-   Media Foundation usa el servicio Programador de clases multimedia (MMCSS), un nuevo servicio del sistema en Windows Vista. MMCSS permite que las aplicaciones multimedia se aseguren de que su procesamiento sensible al tiempo recibe acceso priorizado a los recursos de CPU.

## <a name="content-access"></a>Acceso al contenido

A medida que el entretenimiento digital se mueve a la era de alta definición y el contenido se vuelve más portátil y ubicuo, la protección del contenido se convertirá en una parte integral de los productos multimedia digitales. La extensibilidad de Media Foundation garantiza que puede admitir estas tendencias.

Además, Media Foundation extensibilidad permite que distintos sistemas de protección de contenido funcionen juntos.

## <a name="about-media-foundation"></a>Acerca de Media Foundation

Esta sección contiene información general sobre Media Foundation API. Puede encontrar información de programación detallada en la guía [Media Foundation programación de .](media-foundation-programming-guide.md)



| Sección                                                                              | Descripción                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Novedades de Media Foundation](whats-new-for-media-foundation.md)                | Describe las nuevas características de Media Foundation.                               |
| [Media Foundation encabezados y bibliotecas](media-foundation-headers-and-libraries.md) | Enumera los archivos de encabezado y biblioteca que definen Media Foundation API. |
| [Media Foundation Tools](media-foundation-tools.md)                                 | Describe las herramientas de desarrollo que están disponibles para Media Foundation.  |



 

Media Foundation no se incluye con las ediciones N y KN de Windows 8. Para obtener más información, vea [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



