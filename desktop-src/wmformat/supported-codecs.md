---
title: Códecs admitidos
description: Códecs admitidos
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- Windows SDK de formato multimedia, códecs admitidos
- Windows SDK de formato multimedia, interfaz IWMCodecInfo3
- códecs, admitidos
- IWMCodecInfo3,about
- codecs,IWMCodecInfo3 (interfaz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d202470e2fd430025c5c1e75d0677e4504189e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359905"
---
# <a name="supported-codecs"></a>Códecs admitidos

El SDK Windows Media Format proporciona compatibilidad con los códecs siguientes que se incluyen al instalar el SDK.




| Códec | Descripción | 
|-------|-------------|
| Windows Media Audio | Códec de audio para uso general en la codificación de audio complejo, como la música. Las versiones más recientes de este códec son el códec Windows Media Audio 9 y el códec Windows Media Audio 9.1.<br /> | 
| Windows Audio multimedia Professional | Códec de audio para audio complejo, como música. Admite la codificación multicanal y de 24 bits. Hay dos versiones de este códec:<br /><ul><li>Windows Audio multimedia 9 Professional</li><li>Windows Audio multimedia 9.1 Professional</li></ul> | 
| Windows Audio multimedia sin pérdida de datos | Códec de audio para codificación sin pérdida de datos. Hay dos versiones de este códec:<br /><ul><li>Windows Audio multimedia 9 sin pérdida</li><li>Windows Audio multimedia 9.1 sin pérdida</li></ul> | 
| Windows Audio multimedia 9 Voz | Códec de audio optimizado para codificar la voz humana en relaciones de compresión elevadas. Este es el códec preferido para las secuencias que constan principalmente de palabras habladas. En el caso del contenido que mezcla música y voz, este códec puede cambiar dinámicamente el algoritmo de codificación que se usa para obtener una calidad óptima. | 
| Windows Vídeo multimedia 9 | Códec de vídeo para su uso general en la codificación de vídeo complejo, como películas. | 
| Windows Perfil avanzado de Media Video 9 | Códec de vídeo que incorpora características avanzadas de codificación, incluida la codificación entrelazada. | 
| Windows Pantalla vídeo multimedia 9 | Códec de vídeo optimizado para codificar capturas de pantalla secuenciales. Este códec se usa a menudo para el entrenamiento o la compatibilidad con software mediante la grabación de imágenes de monitor a medida que se usan aplicaciones de equipo. | 
| Windows Imagen de vídeo multimedia | Códec de vídeo para convertir imágenes de mapa de bits con información de degradación en vídeo comprimido. Hay dos versiones de este códec:<br /><ul><li>Windows Imagen de Vídeo multimedia 9</li><li>Windows Vídeo multimedia 9 Imagen v2</li></ul> | 




 

Hay diferentes versiones de los códecs Windows Media Audio y Video disponibles para la codificación en función de la versión del SDK de formato multimedia de Windows que instale. Cuando se usan los métodos si la interfaz [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) para enumerar códecs y formatos de códec, solo se enumeran las versiones más recientes admitidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elegir un método de codificación**](choosing-an-encoding-method.md)
</dt> <dt>

[**Características del códec**](codec-features.md)
</dt> </dl>

 

 





