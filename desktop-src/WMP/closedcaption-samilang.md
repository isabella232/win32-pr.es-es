---
title: ClosedCaption.SAMILang
description: La propiedad SAMILang especifica o recupera el idioma que se muestra para los subtítulos (CC).
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption. SAMILang Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699537"
---
# <a name="closedcaptionsamilang"></a>ClosedCaption.SAMILang

La propiedad **SAMILang** especifica o recupera el idioma que se muestra para los subtítulos (CC).

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Un archivo SAMI puede contener texto para uno o varios idiomas. Los idiomas disponibles para subtítulos (CC) se definen entre las etiquetas <STYLE> y </STYLE> del archivo Sami. Un identificador de idioma se especifica con una cadena alfanumérica única precedida de un punto (.). El nombre especificado para un idioma puede ser cualquier cadena. Por ejemplo, se puede utilizar lo siguiente para definir el Inglés de EE. UU.:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Si no se especifica ningún idioma SAMI, se usa de forma predeterminada el primer idioma definido en el archivo SAMI.

El valor que se pasa mediante *ClosedCaption*. **SAMILang** debe coincidir con el atributo **Name** del especificador de lenguaje.

**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *ClosedCaption*. **SAMILang** en un elemento Select de HTML para especificar el idioma de la leyenda cerrada. El objeto **Player** se creó con ID = "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
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

 

 





