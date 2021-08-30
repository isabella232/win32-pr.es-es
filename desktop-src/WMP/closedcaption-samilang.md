---
title: ClosedCaption.SAMILang
description: La propiedad SAMILang especifica o recupera el idioma que se muestra para los subtítulos.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption.SAMILang Reproductor de Windows Media
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
ms.openlocfilehash: 0edae5d9315bde8c6fc4d507518a335bfb37fd22
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880257"
---
# <a name="closedcaptionsamilang"></a>ClosedCaption.SAMILang

La **propiedad SAMILang** especifica o recupera el idioma que se muestra para los subtítulos.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

Un archivo SAMI puede contener texto para uno o varios idiomas. Los idiomas disponibles para los subtítulos se definen entre &lt; style &gt; y </STYLE> etiquetas en el archivo SAMI. Un identificador de idioma se especifica con una cadena alfanumérica única precedida de un punto (.). El nombre especificado para un idioma puede ser cualquier cadena. Por ejemplo, se podría usar lo siguiente para definir el inglés de EE. UU.:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Si no se especifica ningún lenguaje SAMI, se usa de forma predeterminada el primer idioma definido en el archivo SAMI.

Valor que se pasa mediante *ClosedCaption.* **SAMILang debe** coincidir con **el atributo Name** del especificador de lenguaje.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa ClosedCaption*. **SAMILang en** un elemento SELECT HTML para especificar el lenguaje de subtítulos. El **objeto Player** se creó con id. = "Player".


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

 

 





