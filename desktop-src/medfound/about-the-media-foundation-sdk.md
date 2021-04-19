---
description: Microsoft Media Foundation es la plataforma multimedia de próxima generación para Windows que permite a los desarrolladores, consumidores y proveedores de contenido adoptar la nueva ola de contenido premium con una robustez mejorada, una calidad sin parangón y una interoperabilidad perfecta.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Acerca de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707525"
---
# <a name="about-media-foundation"></a>Acerca de Media Foundation

Microsoft Media Foundation es la plataforma multimedia de próxima generación para Windows que permite a los desarrolladores, consumidores y proveedores de contenido adoptar la nueva ola de contenido premium con una robustez mejorada, una calidad sin parangón y una interoperabilidad perfecta.

Media Foundation requiere Windows Vista o posterior. Utiliza el modelo de objetos componentes (COM) y requiere C/C++. Microsoft no proporciona una API administrada para Media Foundation.

Las API de Media Foundation forman parte de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Para desarrollar una aplicación Media Foundation, instale la versión más reciente de la Windows SDK.

## <a name="audio-and-video-quality"></a>Calidad de audio y vídeo

Media Foundation se ha diseñado para satisfacer los desafíos planteados por el contenido de alta definición. Las mejoras de calidad de audio y vídeo realizadas en toda la plataforma ahora permiten ofrecer una gran experiencia para el contenido de alta definición de próxima generación.

-   DirectX video Acceleration (DXVA) 2,0 ofrece una aceleración de vídeo más eficaz, en comparación con DXVA 1,0, con descodificación de vídeo más sólida y simplificada y uso extendido de hardware en el procesamiento de vídeo. Con DXVA 2,0, Windows puede controlar algunos de los contenidos más exigentes de alta definición con alta calidad y resistencia ante problemas mejorados.

-   La información del espacio de colores se conserva a lo largo de la canalización de vídeo. Los usuarios pueden disfrutar de contenido de vídeo con plena fidelidad. La información de color y las imágenes entrelazadas se pasan ahora al hardware para las composiciones de un solo paso. Conservar la información del espacio de colores también reduce las conversiones de espacio de color innecesarias, lo que libera más ciclos para procesar contenido HD exigente.
-   El representador de vídeo mejorado (EVR) ofrece una mejor compatibilidad con el control de tiempo, el procesamiento de vídeo mejorado y la resistencia de problemas mejorada. Se ha mejorado la compatibilidad con la reproducción de pantalla completa y se ha minimizado el desgaste de vídeo en el modo de ventana.
-   Media Foundation usa el servicio Programador de clases multimedia (MMCSS), un nuevo servicio de sistema en Windows Vista. MMCSS permite a las aplicaciones multimedia asegurarse de que su procesamiento dependiente del tiempo recibe el acceso prioritario a los recursos de la CPU.

## <a name="content-access"></a>Acceso al contenido

A medida que el entretenimiento digital se traslada a la era de alta definición y el contenido es más portátil y omnipresente, la protección de contenido se convierte en una parte integral de los productos multimedia digitales. La extensibilidad de Media Foundation garantiza que puede admitir estas tendencias.

Además, la extensibilidad de Media Foundation permite que distintos sistemas de protección de contenido funcionen juntos.

## <a name="about-media-foundation"></a>Acerca de Media Foundation

Esta sección contiene información general sobre las API de Media Foundation. Puede encontrar información de programación detallada en la [Guía de programación de Media Foundation](media-foundation-programming-guide.md).



| Sección                                                                              | Descripción                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Novedades de Media Foundation](whats-new-for-media-foundation.md)                | Describe las nuevas características de Media Foundation.                               |
| [Media Foundation encabezados y bibliotecas](media-foundation-headers-and-libraries.md) | Enumera los archivos de encabezado y de biblioteca que definen las API de Media Foundation. |
| [Herramientas de Media Foundation](media-foundation-tools.md)                                 | Describe las herramientas de desarrollo que están disponibles para Media Foundation.  |



 

Media Foundation no se incluye con las ediciones N y KN de Windows 8. Para obtener más información, consulte [Microsoft Windows Media Feature Pack para las versiones N y kN de todas las ediciones de Windows 8](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



