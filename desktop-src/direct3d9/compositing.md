---
description: La aplicación puede usar el búfer de galería de símbolos para componer imágenes 2D o 3D en una escena 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composición (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6d11f98a5913c32d8f71385ce9b15ab5e7047c4db8394d5b0decee87f7f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123392"
---
# <a name="compositing-direct3d-9"></a>Composición (Direct3D 9)

La aplicación puede usar el búfer de galería de símbolos para componer imágenes 2D o 3D en una escena 3D. Se usa una máscara en el búfer de la galería de símbolos para occluir un área de la superficie de destino de representación. La información 2D almacenada, como texto o mapas de bits, se puede escribir en el área ocluida. Como alternativa, la aplicación puede representar primitivas 3D adicionales en la región enmascarada por galería de símbolos de la superficie de destino de representación. Incluso puede representar una escena completa.

Los juegos suelen componer varias escenas 3D juntas. Por ejemplo, los juegos de conducción suelen mostrar un reflejo de la vista trasera. El reflejo contiene la vista de la escena 3D detrás del controlador. Es básicamente una segunda escena 3D compuesta con la vista hacia delante del controlador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de galería de símbolos](stencil-buffer-techniques.md)
</dt> </dl>

 

 



