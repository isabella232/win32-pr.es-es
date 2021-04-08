---
title: Compatibilidad con ID3
description: ID3 es una organización que ha definido un conjunto de estándares para incluir metadatos en archivos de audio MPEG Layer-3 (MP3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- SDK de Windows Media Format, compatibilidad con ID3
- Advanced Systems Format (ASF), compatibilidad con ID3
- ASF (formato de sistemas avanzados), compatibilidad con ID3
- metadatos, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778906"
---
# <a name="id3-support"></a>Compatibilidad con ID3

ID3 es una organización que ha definido un conjunto de estándares para incluir metadatos en archivos de audio MPEG Layer-3 (MP3). Los objetos del SDK de Windows Media Format proporcionan compatibilidad con atributos compatibles con ID3. Se admiten tres versiones diferentes de ID3: ID3v1. x, ID3v 2.2 y ID3v 2.3/V2, 4. Para obtener una lista de los atributos que son equivalentes a los fotogramas ID3, consulte [compatibilidad con etiquetas ID3](id3-tag-support.md).

A menos que se indique lo contrario, los objetos de este SDK no realizan la validación de los datos de los fotogramas ID3. Por ejemplo, el atributo de metadatos de [**WM/letra \_ sincronizado**](wm-lyrics-synchronised.md) almacena la letra de la canción con las marcas de tiempo correspondientes. Al escribir un atributo de **WM/letra \_ sincronizado** , los objetos de este SDK no comprobarán para asegurarse de que las marcas de tiempo están en orden cronológico o realizan la validación de cualquier tipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Características de metadatos**](metadata-features.md)
</dt> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




