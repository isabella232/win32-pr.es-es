---
description: La codificación de dos pasos se puede usar para la velocidad de bits constante (CBR) y para la codificación de velocidad de bits variable (VBR) con algunos de los códecs de Windows Media.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Uso de la codificación de Two-Pass (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687304"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Uso de la codificación de Two-Pass (Microsoft Media Foundation)

La codificación de dos pasos se puede usar para la velocidad de bits constante (CBR) y para la codificación de velocidad de bits variable (VBR) con algunos de los códecs de Windows Media. Puede encontrar el número máximo de pasos de codificación admitidos por un códec mediante la recuperación de la propiedad [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) . Ninguno de los códecs admite más de dos pasos. Configure el DMO para que use dos pasos mediante el establecimiento de la propiedad [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) en 2.

Entregue los ejemplos al codificador DMO de uno en uno, como lo haría en un modo de un solo paso. Al procesar los ejemplos de entrada para el paso de preprocesamiento, las llamadas a [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) o [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) devolverán **S \_ false** para indicar que no se produce ninguna salida.

Al final del primer paso (después de procesar la última entrada por primera vez), debe establecer la propiedad [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) para notificar al códec que la siguiente entrada procesada es la primera entrada del segundo paso. No se requiere ningún valor para esta propiedad, por lo que debe usar una estructura de **variante** vacía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
