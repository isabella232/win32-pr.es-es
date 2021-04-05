---
title: WM/GenreID
description: El atributo WM/GenreID contiene un identificador de género compatible con el contenido de la etiqueta TCON en ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Formato de Windows Media WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419735"
---
# <a name="wmgenreid"></a>WM/GenreID

El atributo **WM/GenreID** contiene un identificador de género compatible con el contenido de la etiqueta TCON en ID3v2. Este debe contener el ID. de género entre paréntesis y, opcionalmente, un perfeccionamiento que describa el género. Para obtener más información, consulte la especificación ID3v2.

## <a name="global-constant"></a>Constante global

g \_ wszWMGenreID

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

El atributo preferido para especificar un género es [**WM/Genre**](wm-genre.md). Úselo en preferencia a este atributo.

Si cambia **WM/Genre** o **WM/GenreID** en un archivo mp3, se cambiará el otro atributo para que coincida.

### <a name="example"></a>Ejemplo



| Tipo de archivo | Valor de ejemplo   |
|-----------|-----------------|
| Audio     | "(4) Eurodisco" |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




