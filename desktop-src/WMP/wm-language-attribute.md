---
title: Atributo WM/Language
description: El atributo WM/Language es el idioma del elemento.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- Windows atributo WM/idioma Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708716"
---
# <a name="wmlanguage-attribute"></a>Atributo WM/Language

El atributo **WM/Language** es el idioma del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

Este atributo puede tener varios valores. Para recuperar todos los valores de un atributo con varios valores, debe usar el método **media. getItemInfoByType** , no el método **media. getItemInfo** .

**Language** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMLanguage.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior (el elemento de radio solo se admite en Windows Media Player 9 series)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





