---
title: Subtipos de medios comprimidos
description: Subtipos de medios comprimidos
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows Media Format SDK, tipos de medios
- Advanced Systems Format (ASF), tipos de medios
- ASF (formato de sistemas avanzados), tipos de medios
- SDK de Windows Media Format, subtipos de medios comprimidos
- Formato de sistemas avanzados (ASF), subtipos de medios comprimidos
- ASF (formato de sistemas avanzados), subtipos de medios comprimidos
- tipos de medios, subtipos de medios comprimidos
- subtipos de medios comprimidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d92d192d04257f0375a618dda05aa97fd3f344b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148775"
---
# <a name="compressed-media-subtypes"></a>Subtipos de medios comprimidos

En la tabla siguiente se enumeran los subtipos de medios comprimidos. Estos tipos se utilizan para identificar las secuencias comprimidas en un archivo. Al configurar un flujo de vídeo o audio, normalmente usará estos tipos.



| Subtipo de medios comprimidos          | Descripción                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ ACELPnet          | Audio codificado con el códec ACELP de SIPRO Labs. Este audio suele ser datos de voz. (Ya no se admite para la codificación).                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ mp43              | Vídeo codificado por el códec Microsoft MPEG 4, versión 3. Este códec ya no es compatible con el SDK de Windows Media Format. Si este códec ya está instalado en un equipo, al instalar el SDK de Windows Media Format o el paquete de redistribución en un equipo no se quitará este códec. |
| WMMEDIASUBTYPE \_ MP4              | Vídeo codificado mediante la versión 1 del códec ISO MPEG 4.                                                                                                                                                                                                                                         |
| \_Vídeo MPEG2 de WMMEDIASUBTYPE \_      | Vídeo codificado con especificaciones de MPEG 2.                                                                                                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ MSS1              | Vídeo codificado con la versión 1 del códec de pantalla de Windows Media.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ MSS2              | Vídeo codificado con el códec de pantalla de Windows Media Video 9.                                                                                                                                                                                                                                  |
| WMMEDIASUBTYPE \_ WMVP              | Vídeo codificado con el códec de imagen de Windows Media Video 9 para transformar mapas de bits y datos de desformación en una secuencia de vídeo.                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ WVP2              | Vídeo codificado con el códec Windows Media Video 9 Image V2.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ Lossless | Audio codificado con el códec Windows Media Audio 9 Lossless o el códec Windows Media Audio 9,1.                                                                                                                                                                                           |
| WMMEDIASUBTYPE \_ WMAudioV2         | Audio codificado con el códec Windows Media Audio versión 2. Este valor es idéntico a WMMEDIASUBTYPE \_ WMAudioV7 y WMMEDIASUBTYPE \_ WMAudioV8, ya que los bitstreams de estas versiones de códec son compatibles.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV7         | Audio codificado con la versión 7 de Windows Media Audio Codec. Este valor es idéntico a WMMEDIASUBTYPE \_ WMAudioV2 y WMMEDIASUBTYPE \_ WMAudioV8, ya que los bitstreams de estas versiones de códec son compatibles.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV8         | Audio codificado con el códec Windows Media Audio 8, el códec Windows Media Audio 9 o el códec Windows Media Audio 9,1. Este valor es idéntico a WMMEDIASUBTYPE \_ WMAudioV2 y WMMEDIASUBTYPE \_ WMAudioV7, ya que los bitstreams de estas versiones de códec son compatibles.              |
| WMMEDIASUBTYPE \_ WMAudioV9         | Audio codificado con el códec Windows Media Audio 9 Professional o el códec Windows Media Audio 9,1 Professional.                                                                                                                                                                          |
| WMMEDIASUBTYPE \_ M4S2              | Vídeo codificado con el códec ISO MPEG4 v 1.1.                                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMSP1             | Audio codificado con el códec de voz de Windows Media Audio 9.                                                                                                                                                                                                                                   |
| WMMEDIASUBTYPE \_ WMV1              | Vídeo codificado con la versión 7 de Windows Media Video Codec.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ wmv2              | Vídeo codificado mediante el códec Windows Media Video 8.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ Wmv3              | Vídeo codificado mediante el códec Windows Media Video 9.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMVA              | Vídeo codificado con la versión del códec de perfil avanzado de Windows Media Video 9 que se lanzó con el SDK de Windows Media Format 9 series.                                                                                                                                           |
| WMMEDIASUBTYPE \_ Wvc1              | Vídeo codificado con la versión del códec de perfil avanzado de Windows Media Video 9 que se lanzó con el SDK de Windows Media Format 11. Este subtipo identifica un flujo de bits que es compatible con el estándar SMPTE VC-1.                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de tipo de medio**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de medios**](media-types.md)
</dt> <dt>

[**Subtipos de medios sin comprimir**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




