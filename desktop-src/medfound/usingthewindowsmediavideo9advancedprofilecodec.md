---
description: Uso del perfil avanzado Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Uso del perfil avanzado Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363658"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>Uso del perfil avanzado Windows Media Video 9

Los procedimientos de vídeo básicos descritos en la sección [Trabajar](workingwithvideo.md) con vídeo también se aplican directamente al perfil avanzado de Windows Media Video 9. No se requiere ningún procedimiento especial.

El Windows avanzado de Media Video 9 está asociado a los identificadores de clase CLSID \_ CWMV9EncMediaObject y CLSID \_ CWMVDecMediaObject. El valor de FOURCC para los tipos de medios que usan este códec es "WVC1".

El perfil avanzado de Windows Media Video 9 admite todos los modos de codificación comunes, así como codificación entrelazada, codificación entrelazada mixta y progresiva, resoluciones que son diferentes de las características de visualización y reducción de intervalos. Otra característica es la capacidad de almacenar metadatos de secuencia y marco en el propio flujo de bits. anteriormente, esto requería el uso de ASF y la API de extensiones de unidad de datos.

Las siguientes propiedades del perfil avanzado de Windows Media Video 9, que se pueden controlar mediante la configuración del Registro, no tienen las cadenas **IPropertyBag** o **IPropertyStore** correspondientes:

-   Opción Dquant.
-   Intensidad de Dquant.
-   Forzar superposición.
-   Método de costo de vector de movimiento.

## <a name="achieving-optimal-visual-quality"></a>Lograr una calidad visual óptima

Para la mayoría de los datos de vídeo, para lograr una calidad visual óptima mediante el perfil avanzado de Windows Media Video 9, puede establecer la propiedad [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) en 1.

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>Acerca de los códecs de perfil avanzado Windows Media Video 9 anterior

La versión actual del códec de perfil avanzado Windows Media Video 9 se basa en el estándar Society of Motion Picture and Tv Engineers (SMPTE) para el perfil avanzado VC-1 (SMPTE 421M). Este códec reemplaza el códec anterior de Windows también denominado códec de perfil avanzado de Windows Media Video 9 identificado por el código FOURCC "WMVA". La versión anterior del códec VC-1 se implementó antes de que se finalizara el estándar de perfil avanzado VC-1 y ya no se admite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> 
<dt>

[Uso de advanced Configuración del códec de perfil avanzado Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



