---
description: Uso del perfil avanzado de Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Uso del perfil avanzado de Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689632"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>Uso del perfil avanzado de Windows Media Video 9

Los procedimientos de vídeo básicos que se describen en la sección [trabajar con vídeo](workingwithvideo.md) también se aplican directamente al perfil avanzado de Windows Media Video 9. No se requiere ningún procedimiento especial.

El perfil avanzado de Windows Media Video 9 está asociado a los identificadores de clase CLSID \_ CWMV9EncMediaObject y CLSID \_ CWMVDecMediaObject. El valor FOURCC para los tipos de medios que usan este códec es "WVC1".

El perfil avanzado de Windows Media Video 9 es compatible con todos los modos de codificación comunes, como la codificación entrelazada, la codificación entrelazada y progresiva mixta, las resoluciones que son diferentes de las que se muestran y las características de reducción del intervalo. Otra característica es la capacidad de almacenar metadatos de secuencia y fotogramas en el propio flujo de bits; anteriormente, este tenía el uso de la API de extensiones de unidad de datos y ASF.

Las siguientes propiedades del perfil avanzado de Windows Media Video 9, que se puede controlar mediante la configuración del registro, no tienen las cadenas **IPropertyBag** o **IPropertyStore** correspondientes:

-   Opción Dquant.
-   Dquant.
-   Forzar la superposición.
-   Método de costo del vector de movimiento.

## <a name="achieving-optimal-visual-quality"></a>Obtención de una calidad visual óptima

Para la mayoría de los datos de vídeo, para lograr una calidad visual óptima mediante el perfil avanzado de Windows Media Video 9, puede establecer la propiedad [ \_ COMPRESSIONOPTIMIZATIONTYPE de MFPKEY](mfpkey-compressionoptimizationtypeproperty.md) en 1.

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>Acerca de los códecs de perfil avanzado de Windows Media Video 9 anteriores

La versión actual del códec de perfil avanzado de Windows Media Video 9 se basa en la sociedad del estándar de ingeniería de películas y televisión (SMPTE) para el perfil avanzado VC-1 (SMPTE 421M). Este códec reemplaza el códec anterior de Windows también llamado códec de perfil avanzado de Windows Media Video 9 que se identificó mediante el código FOURCC "WMVA". La versión anterior del códec VC-1 se implementó antes de finalizar el estándar de perfil avanzado de VC-1 y ya no se admite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> 
<dt>

[Uso de la configuración avanzada del códec de perfil avanzado de Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



