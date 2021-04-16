---
title: ClosedCaption.SAMIStyle
description: La propiedad SAMIStyle especifica o recupera el estilo de subtítulos (CC).
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption. SAMIStyle Windows Media Player
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
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699535"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption.SAMIStyle

La propiedad **SAMIStyle** especifica o recupera el estilo de subtítulos (CC).

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Un archivo SAMI puede contener varias definiciones de estilo de formato. Los estilos SAMI se definen entre las etiquetas <STYLE> y </STYLE> del archivo Sami. Un estilo se define con una cadena de texto precedida por un \# carácter. Por ejemplo:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Especifica un estilo que genera una fuente determinada.

Si no se especifica ningún estilo SAMI, se usa de forma predeterminada el primer estilo definido en el archivo SAMI.

**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se crea un elemento SELECT de HTML que usa *closedCaption*. **SAMIStyle** para cambiar la apariencia del texto de la leyenda cerrada. El objeto **Player** se creó con ID = "Player".


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



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 





