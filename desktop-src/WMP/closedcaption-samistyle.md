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
ms.openlocfilehash: 6bd45977e3d433239e74aee21def913b640fad12
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882173"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption.SAMIStyle

La **propiedad SAMIStyle** especifica o recupera el estilo de subtítulos.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

Un archivo SAMI puede contener varias definiciones de estilo de formato. Los estilos SAMI se definen entre &lt; style &gt; y </STYLE> etiquetas en el archivo SAMI. Un estilo se define con una cadena de texto precedida de un \# carácter. Por ejemplo:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Especifica un estilo que genera una fuente determinada.

Si no se especifica ningún estilo SAMI, el primer estilo definido en el archivo SAMI se usa de forma predeterminada.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="examples"></a>Ejemplos

En el JScript siguiente se crea un elemento SELECT HTML que usa *closedCaption*. **SAMIStyle para** cambiar la apariencia del texto del título cerrado. El **objeto Player** se creó con id. = "Player".


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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption (objeto)**](closedcaption-object.md)
</dt> </dl>

 

 





