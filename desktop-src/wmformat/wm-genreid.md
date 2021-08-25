---
title: WM/GenreID
description: El atributo WM/GenreID contiene un identificador de género compatible con el contenido de la etiqueta TCON en ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Formato multimedia de Windows WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9355a16196d386d4ec3f2a98588eced2981f8e62a3df96a9c0d094551a10a733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930445"
---
# <a name="wmgenreid"></a>WM/GenreID

El **atributo WM/GenreID** contiene un identificador de género compatible con el contenido de la etiqueta TCON en ID3v2. Debe contener el identificador de género entre paréntesis, seguido opcionalmente de un refinamiento que describa aún más el género. Para obtener más información, consulte la especificación ID3v2.

## <a name="global-constant"></a>Constante global

g \_ wszWMGenreID

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

El atributo preferido para especificar un género es [**WM/Genre.**](wm-genre.md) Úsese en preferencia a este atributo.

Si cambia **WM/Genre** o **WM/GenreID** en un archivo MP3, el otro atributo se cambiará para que coincida.

### <a name="example"></a>Ejemplo



| Tipo de archivo | Valor de ejemplo   |
|-----------|-----------------|
| Audio     | "(4) Eurodisco" |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




