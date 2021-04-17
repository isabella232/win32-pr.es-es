---
title: Elemento COPYRIGHT (msfeeds. h)
description: El elemento COPYRIGHT define una cadena de texto que especifica la información de copyright de un elemento ASX o ENTRY.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Elemento COPYRIGHT de Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699926"
---
# <a name="copyright-element"></a>Elemento COPYRIGHT

El elemento **Copyright** define una cadena de texto que especifica la información de copyright de un elemento **ASX** o **entry** .

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ASX**, **entrada** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define una cadena de texto que especifica la información de copyright para un elemento **ASX** o **entry** .

Cuando este elemento aparece dentro de un elemento **ASX** , la cadena de copyright solo se muestra como **Mostrar** información. Cuando este elemento aparece dentro de un elemento de **entrada** , el texto se muestra como información de recorte. Cada elemento **ASX** y **entry** primarios debe contener como máximo un elemento secundario de **Copyright** . Varios elementos de **Copyright** después del primero se omitirán y no se mostrarán.

Es posible que los caracteres de los símbolos de copyright y de registro de marcas comerciales (o) no se muestren correctamente si el metarchivo no se codifica con el esquema de codificación UTF-8. En este caso, para mostrar correctamente cualquiera de estos símbolos para todos los usuarios, puede usar en su lugar los equivalentes ASCII (c) y (R).

Si el metarchivo está codificado con UTF-8, los símbolos de copyright y marca comercial se mostrarán correctamente.

## <a name="examples"></a>Ejemplos


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/>                                 |
| Encabezado<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar caracteres de copyright a los metaarchivos**](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





