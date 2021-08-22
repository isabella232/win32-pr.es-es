---
title: ClosedCaption.SAMIStyle
description: La propiedad SAMIStyle especifica o recupera el estilo de subtítulos.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption.SAMIStyle Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4a12671877cf0d4d8abdb77d169b0f13000bc564e6c1dc37e65bf6eccdf005
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580770"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption.SAMIStyle

La **propiedad SAMIStyle** especifica o recupera el estilo de subtítulos.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

Un archivo SAMI puede contener varias definiciones de estilo de formato. Los estilos SAMI se definen entre las <STYLE> etiquetas y </STYLE> del archivo SAMI. Un estilo se define con una cadena de texto precedida de un \# carácter. Por ejemplo:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Especifica un estilo que genera una fuente determinada.

Si no se especifica ningún estilo SAMI, el primer estilo definido en el archivo SAMI se usa de forma predeterminada.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se crea un elemento SELECT HTML que usa *closedCaption*. **SAMIStyle para** cambiar la apariencia del texto del título cerrado. El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption (objeto)**](closedcaption-object.md)
</dt> </dl>

 

 





