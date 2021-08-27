---
title: Atributo WM/Language
description: El atributo WM/Language es el idioma del elemento.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- Atributo WM/Language Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8902d36ebe9e8227d22f55273e8351d7ed09c592953b44a31e45c06b838f9871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122655"
---
# <a name="wmlanguage-attribute"></a>Atributo WM/Language

El **atributo WM/Language** es el idioma del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

Este atributo puede tener varios valores. Para recuperar todos los valores de un atributo con varios valores, debe usar el método **Media.getItemInfoByType,** no el **método Media.getItemInfo.**

**Language** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMLanguage.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior (el elemento de radio solo se admite en Reproductor de Windows Media serie 9)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





