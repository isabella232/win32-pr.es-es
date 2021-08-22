---
description: Puede usar el búfer de galería de símbolos para efectos más abstractos, como la delineación y la silación.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Contornos y sobresalciones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b5fcf26b3f3cbbe6e051e1a7d8517cc6d69044beb6eaed7f54baef3509a748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563415"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a>Contornos y sobresalciones (Direct3D 9)

Puede usar el búfer de galería de símbolos para efectos más abstractos, como la delineación y la silación.

Si la aplicación aplica una máscara de galería de símbolos a la imagen de una primitiva que tiene la misma forma pero ligeramente más pequeña, la imagen resultante solo contiene el contorno de la primitiva. A continuación, la aplicación puede rellenar el área enmascarada de la galería de símbolos de la imagen con un color sólido, lo que da a la primitiva una apariencia con relieve.

Si la máscara de galería de símbolos tiene el mismo tamaño y forma que la primitiva que está representando, la imagen resultante contiene un hueco donde debe estar la primitiva. A continuación, la aplicación puede rellenar el hueco con negro para producir una consondía de la primitiva.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de galería de símbolos](stencil-buffer-techniques.md)
</dt> </dl>

 

 



