---
description: La codificación de dos pases se puede usar para la velocidad de bits constante (CBR) y para la codificación de velocidad de bits variable (VBR) con algunos de los códecs Windows media.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Usar Two-Pass codificación (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363647"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Usar Two-Pass codificación (Microsoft Media Foundation)

La codificación de dos pases se puede usar para la velocidad de bits constante (CBR) y para la codificación de velocidad de bits variable (VBR) con algunos de los códecs Windows media. Puede encontrar el número máximo de pases de codificación admitidos por un códec mediante la recuperación de la propiedad [ \_ MFPKEY PASSESRECOMMENDED.](mfpkey-passesrecommendedproperty.md) Ninguno de los códecs admite más de dos pases. Configure el DMO para usar dos pases estableciendo la propiedad [ \_ MFPKEY PASSESUSED](mfpkey-passesusedproperty.md) en 2.

Entregue los ejemplos al codificador DMO de uno en uno, como lo haría en un modo de paso único. Al procesar los ejemplos de entrada para el paso de preprocesamiento, las llamadas a [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) o [**IMFTransform::P processInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) **devolverán S \_ FALSE**, para indicar que no se genera ninguna salida.

Al final del primer paso (después de que la última entrada se procese por primera vez), debe establecer la propiedad [ \_ MFPKEY ENDOFPASS](mfpkey-endofpassproperty.md) para notificar al códec que la siguiente entrada procesada es la primera entrada del segundo paso. No se requiere ningún valor para esta propiedad, por lo que debe usar una estructura **VARIANT** vacía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
