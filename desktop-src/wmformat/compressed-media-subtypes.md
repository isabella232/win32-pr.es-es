---
title: Subtipos de medios comprimidos
description: Subtipos de medios comprimidos
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows SDK de formato multimedia, tipos multimedia
- Formato de sistemas avanzados (ASF), tipos de medios
- ASF (formato de sistemas avanzados), tipos de medios
- Windows SDK de formato multimedia, subtipos multimedia comprimidos
- Formato de sistemas avanzados (ASF), subtipos de medios comprimidos
- ASF (formato de sistemas avanzados), subtipos de medios comprimidos
- tipos de medios, subtipos multimedia comprimidos
- subtipos de medios comprimidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d92d192d04257f0375a618dda05aa97fd3f344b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571277"
---
# <a name="compressed-media-subtypes"></a>Subtipos de medios comprimidos

En la tabla siguiente se enumeran los subtipos multimedia comprimidos. Estos tipos se usan para identificar secuencias comprimidas en un archivo. Al configurar una secuencia de vídeo o audio, normalmente usará estos tipos.



| Subtipo de medio comprimido          | Descripción                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ ACELPnet          | Audio codificado con el códec ACELP de Sipro Labs. Normalmente, este audio son datos de voz. (Ya no se admite para la codificación).                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ MP43              | Vídeo codificado por el códec Microsoft MPEG 4 versión 3. Este códec ya no es compatible con el SDK Windows Media Format. Si este códec ya está instalado en un equipo, la instalación del SDK de formato multimedia de Windows o el paquete de redistribución en un equipo no quitará este códec. |
| WMMEDIASUBTYPE \_ MP4S              | Vídeo codificado con el códec ISO MPEG 4 versión 1.                                                                                                                                                                                                                                         |
| WMMEDIASUBTYPE \_ MPEG2 \_ VIDEO      | Vídeo codificado según las especificaciones de MPEG 2.                                                                                                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ MSS1              | Vídeo codificado con el códec Windows Media Screen versión 1.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ MSS2              | Vídeo codificado con el códec Windows Media Video 9 Screen.                                                                                                                                                                                                                                  |
| WMMEDIASUBTYPE \_ WMVP              | Vídeo codificado con el códec Windows imagen de Media Video 9 para transformar mapas de bits y desasociados datos en una secuencia de vídeo.                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ WVP2              | Vídeo codificado con el códec Windows Media Video 9 Image v2.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ Lossless | Audio codificado con el códec sin Windows Media Audio 9 o el códec Windows Media Audio 9.1.                                                                                                                                                                                           |
| WMMEDIASUBTYPE \_ WMAudioV2         | Audio codificado con el códec Windows Media Audio versión 2. Este valor es idéntico a WMMEDIASUBTYPE \_ WMAudioV7 y WMMEDIASUBTYPE WMAudioV8, ya que las secuencias de bits de estas versiones de \_ códec son compatibles.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV7         | Audio codificado con el códec Windows Media Audio versión 7. Este valor es idéntico a WMMEDIASUBTYPE \_ WMAudioV2 y WMMEDIASUBTYPE WMAudioV8, ya que las secuencias de bits de estas versiones de \_ códec son compatibles.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV8         | Audio codificado con el códec Windows Media Audio 8, el códec Windows Media Audio 9 o el códec Windows Media Audio 9.1. Este valor es idéntico a WMMEDIASUBTYPE \_ WMAudioV2 y WMMEDIASUBTYPE WMAudioV7, ya que las secuencias de bits de estas versiones de \_ códec son compatibles.              |
| WMMEDIASUBTYPE \_ WMAudioV9         | Audio codificado con el códec Windows Media Audio 9 o el códec Professional Media Audio 9.1 Windows media 9. Professional 1.                                                                                                                                                                          |
| WMMEDIASUBTYPE \_ M4S2              | Vídeo codificado con el códec ISO MPEG4 v1.1.                                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMSP1             | Audio codificado con el códec Windows Media Audio 9 Voice.                                                                                                                                                                                                                                   |
| WMMEDIASUBTYPE \_ WMV1              | Vídeo codificado con el códec Windows Media Video versión 7.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMV2              | Vídeo codificado mediante el códec Windows Media Video 8.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMV3              | Vídeo codificado con el códec Windows Media Video 9.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMVA              | Vídeo codificado con la versión del códec de perfil avanzado Windows Media Video 9 que se publicó con el SDK de la serie Windows Media Format 9.                                                                                                                                           |
| WMMEDIASUBTYPE \_ WVC1              | Vídeo codificado con la versión del códec de perfil avanzado Windows Media Video 9 que se publicó con el SDK Windows Media Format 11. Este subtipo identifica un flujo de bits que es compatible con el estándar SMPTE VC-1.                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de tipo de medio**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de medios**](media-types.md)
</dt> <dt>

[**Subtipos de medios sin comprimir**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




