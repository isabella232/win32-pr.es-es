---
description: Puede usar el búfer de estarcido para efectos más abstractos, como la esquematización y la silhouetting.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Contornos y siluetas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805300"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a>Contornos y siluetas (Direct3D 9)

Puede usar el búfer de estarcido para efectos más abstractos, como la esquematización y la silhouetting.

Si la aplicación aplica una máscara de galería de símbolos a la imagen de un primitivo que tiene la misma forma pero ligeramente más pequeña, la imagen resultante contiene solo el contorno del primitivo. A continuación, la aplicación puede rellenar el área enmascarada de estarcido de la imagen con un color sólido, lo que proporciona al primitivo una apariencia en relieve.

Si la máscara de la galería de símbolos tiene el mismo tamaño y forma que la primitiva que se está representando, la imagen resultante contiene un hueco en el que el primitivo debe ser. A continuación, la aplicación puede rellenar el hueco con negro para producir una silueta de la primitiva.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de estarcido](stencil-buffer-techniques.md)
</dt> </dl>

 

 



