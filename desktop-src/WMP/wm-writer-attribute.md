---
title: Atributo WM/Writer
description: El atributo WM/Writer es el nombre del escritor que escribió las palabras del contenido.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- Atributo WM/Writer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a239fd83c936a0712459307fbf08b01c4bfcc4f6fd4c6d32cddc12d8092f2b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332069"
---
# <a name="wmwriter-attribute"></a>Atributo WM/Writer

El **atributo WM/Writer** es el nombre del escritor que escribió las palabras del contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

Este atributo puede tener varios valores. Para recuperar todos los valores de un atributo con varios valores, debe usar el método **Media.getItemInfoByType,** no el método **Media.getItemInfo.**

**Writer** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMWriter.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





