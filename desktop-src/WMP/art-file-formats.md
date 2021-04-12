---
title: Formatos de archivo de imagen
description: Formatos de archivo de imagen
ms.assetid: 803479e8-0e00-4724-80b7-9d86709c43db
keywords:
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, formatos de archivo
- Máscaras de Windows Media Player, formatos de archivo para arte
- máscaras, formatos de archivo para arte
- formatos de archivo para la piel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35af72fd502cb23e81063fe9513b4a9311f9557
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357712"
---
# <a name="art-file-formats"></a>Formatos de archivo de imagen

Windows Media Player reconoce los siguientes formatos de archivo de imagen para las máscaras:



| Formato                                  | Extensión   | Descripción                                                                                        |
|-----------------------------------------|-------------|----------------------------------------------------------------------------------------------------|
| Bitmap                                  | .bmp        | Se recomiendan las imágenes de mapa de bits porque ofrecen el máximo control sobre la imagen y los colores exactos. |
| Formato de intercambio de gráficos (GIF)       | .gif        | Formato de imagen comprimido usado para las páginas Web. Se admiten los archivos GIF animados.                            |
| Formato JPEG (Joint Photographic Experts Group) | .jpeg, .jpg | Formato de imagen comprimido usado para las páginas Web.                                                         |
| Formato PNG (Portable Network Graphics)         | .png        | Formato de imagen comprimido usado para las páginas Web.                                                         |



 

Si usa uno de los formatos de archivo comprimidos que define un color como transparente para un explorador Web, no defina un color como transparente en el archivo de imagen. Use un color visible para representar las áreas transparentes de la imagen y, a continuación, defina ese color como transparente en el archivo de definición de máscara. Por ejemplo, si crea un archivo GIF con algunas áreas transparentes, no serán transparentes en la imagen final y no podrá usar el color que establezca como transparente en el archivo GIF para el color de transparencia de la máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de imagen**](art-files.md)
</dt> </dl>

 

 




