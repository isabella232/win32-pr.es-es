---
title: Compatibilidad con ID3
description: ID3 es una organización que ha definido un conjunto de estándares para incluir metadatos en archivos de audio MPEG Layer-3 (MP3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows SDK de formato multimedia, compatibilidad con ID3
- Formato de sistemas avanzados (ASF), compatibilidad con ID3
- ASF (formato de sistemas avanzados), compatibilidad con ID3
- metadata,ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c92fb9282483b6fd01b1149220e5f30421c3c1285bd533d64afef91709314e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702986"
---
# <a name="id3-support"></a>Compatibilidad con ID3

ID3 es una organización que ha definido un conjunto de estándares para incluir metadatos en archivos de audio MPEG Layer-3 (MP3). Los objetos del SDK Windows Media Format proporcionan compatibilidad con atributos compatibles con ID3. Se admiten tres versiones distintas de ID3: ID3v1.x, ID3v2.2 e ID3v2.3/v2,4. Para obtener una lista de los atributos que equivalen a fotogramas ID3, vea [Compatibilidad con etiquetas ID3.](id3-tag-support.md)

A menos que se indique lo contrario, los objetos de este SDK no realizan ninguna validación de los datos del marco ID3. Por ejemplo, el atributo de metadatos [**WM/La sincronización Desastroso almacena \_**](wm-lyrics-synchronised.md) la canción con las marcas de tiempo correspondientes. Al escribir un atributo **WM/Desastroso \_** sincronizado, los objetos de este SDK no comprobarán que las marcas de tiempo estén en orden cronológico ni realicen la validación de ningún tipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Características de metadatos**](metadata-features.md)
</dt> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




