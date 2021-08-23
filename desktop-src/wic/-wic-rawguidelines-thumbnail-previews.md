---
description: Miniaturas y vistas previas
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniaturas y vistas previas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 110b0f4da08eaf2b17582dabec1ff7bd6d4f3ab4389c6bcf7654cdb5ca3198a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086888"
---
# <a name="thumbnails-and-previews"></a>Miniaturas y vistas previas

Windows Vista y el Windows Galería de fotos se basan en Windows Imaging Component (WIC) para representar miniaturas rápidas y vistas previas de imágenes. Para admitir la representación rápida de miniaturas y vista previa, los códecs RAW deben implementar las interfaces [**WIC GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) y [**GetPreview.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) Para admitir una experiencia de usuario con capacidad de respuesta, es muy deseable que estas interfaces devuelvan un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) al autor de la llamada en 200 milisegundos o menos.

Microsoft recomienda encarecidamente que los propietarios de formato de archivo RAW generen una vista previa representada previamente y la almacenarán en caché en el archivo de imagen. En el caso de un formato en el dispositivo, esto suele hacerse en tiempo de captura. Sin embargo, las vistas previas también se pueden regenerar y almacenar en el archivo de imagen siempre que se cambien las propiedades de la interfaz [**IWICDevelopRaw,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) si no se necesita demasiado trabajo para hacerlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Directrices de WIC para formatos de imagen sin formato de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



