---
description: La aplicación puede usar el búfer de galería de símbolos para componer imágenes 2D o 3D en una escena 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composición (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888708"
---
# <a name="compositing-direct3d-9"></a>Composición (Direct3D 9)

La aplicación puede usar el búfer de galería de símbolos para componer imágenes 2D o 3D en una escena 3D. Se usa una máscara en el búfer de la galería de símbolos para occluir un área de la superficie de destino de representación. La información 2D almacenada, como texto o mapas de bits, se puede escribir en el área ocluida. Como alternativa, la aplicación puede representar primitivas 3D adicionales en la región enmascarada por galería de símbolos de la superficie de destino de representación. Incluso puede representar una escena completa.

Los juegos suelen componer varias escenas 3D juntas. Por ejemplo, los juegos de conducción suelen mostrar un reflejo de la vista trasera. El reflejo contiene la vista de la escena 3D detrás del controlador. Es básicamente una segunda escena 3D compuesta con la vista hacia delante del controlador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de galería de símbolos](stencil-buffer-techniques.md)
</dt> </dl>

 

 



