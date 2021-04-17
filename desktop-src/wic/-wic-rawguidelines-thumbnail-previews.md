---
description: Miniaturas y vistas previas
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniaturas y vistas previas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659940"
---
# <a name="thumbnails-and-previews"></a>Miniaturas y vistas previas

Windows Vista y la Galería fotográfica de Windows se basan en Windows Imaging Component (WIC) para representar miniaturas rápidas y vistas previas de las imágenes. Para admitir la representación rápida en miniatura y vista previa, los códecs sin formato deben implementar las interfaces WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) y [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) . Para admitir una experiencia de usuario con capacidad de respuesta, es muy conveniente que estas interfaces devuelvan un valor de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) al llamador en 200 milisegundos o menos.

Microsoft recomienda encarecidamente que los propietarios de formato de archivo sin formato generen una vista previa preprocesada y la almacenen en la memoria caché en el archivo de imagen. En el caso de un formato en el dispositivo, esto suele realizarse en el momento de la captura. Sin embargo, las vistas previas también se pueden volver a generar y almacenar en el archivo de imagen cada vez que se modifican las propiedades de la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , si no se tarda demasiado en realizarse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Instrucciones de WIC para formatos de imagen RAW de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



