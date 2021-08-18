---
title: Elemento COPYRIGHT (Msfeeds.h)
description: El elemento COPYRIGHT define una cadena de texto que especifica la información de copyright de un elemento ASX o ENTRY.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Elemento COPYRIGHT Reproductor de Windows Media
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
ms.openlocfilehash: 8e5a01e97364aa47182e38e3e3066895c771e2d5edb6c480e8108cb168e7f8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997465"
---
# <a name="copyright-element"></a>Elemento COPYRIGHT

El **elemento COPYRIGHT** define una cadena de texto que especifica la información de copyright de un elemento **ASX** o **ENTRY.**

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
| Elementos primarios | **ASX**, **ENTRY** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define una cadena de texto que especifica la información de copyright de un **elemento ASX** o **ENTRY.**

Cuando este elemento aparece dentro de un **elemento ASX,** la cadena de copyright solo se muestra como **Mostrar** información. Cuando este elemento aparece dentro de un **elemento ENTRY,** el texto se muestra como información de recorte. Cada elemento **ASX y** **ENTRY** primario debe contener como máximo un elemento **secundario COPYRIGHT.** Varios **elementos COPYRIGHT** después de la primera se omitirán y no se mostrarán.

Es posible que los caracteres de los símbolos de registro de marca comercial y copyright ( o ) no se muestren correctamente si el metarchivo no está codificado mediante el esquema de codificación UTF-8. En este caso, para mostrar cualquiera de estos símbolos correctamente para todos los usuarios, puede usar los equivalentes ASCII (c) y (R) en su lugar.

Si el metarchivo está codificado mediante UTF-8, los símbolos de copyright y marca comercial se mostrarán correctamente.

## <a name="examples"></a>Ejemplos


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/>                                 |
| Header<br/>  | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar caracteres de copyright a metarchivos**](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





