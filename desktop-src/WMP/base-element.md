---
title: ELEMENTO BASE
description: El elemento BASE define una cadena de dirección URL anexada al frente de las direcciones URL enviadas a Reproductor de Windows Media.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Base Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889601"
---
# <a name="base-element"></a>ELEMENTO BASE

El **elemento BASE** define una cadena de dirección URL anexada al frente de las direcciones URL enviadas a Reproductor de Windows Media.

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**HREF** (obligatorio)

Cadena anexada al frente a las direcciones URL enviadas a Reproductor de Windows Media. El valor predeterminado es la cadena null ("").

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ASX**, **ENTRY** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define una cadena de dirección URL anexada al frente de las direcciones URL que se envían a Reproductor de Windows Media. El cambio de dirección URL es un mecanismo de scripting que hace Reproductor de Windows Media abrir una nueva dirección URL en un explorador o marco del explorador cuando recibe un comando de script.

El **elemento BASE** es similar a un directorio principal para vínculos relativos. Solo afecta a las direcciones URL enviadas mediante comandos de script como parte de la secuencia de contenido que se reproduce en Reproductor de Windows Media.

Un **elemento BASE** definido como elemento secundario de un elemento **ASX** se convierte en el valor predeterminado para todo el metarchivo. Un **elemento BASE** definido en un elemento **ENTRY** invalida cualquier elemento **BASE** del elemento **ASX** primario (solo para ese **elemento ENTRY).**

> [!Note]  
> Si el **atributo HREF** no termina con un carácter / , Reproductor de Windows Media anexa uno al final de la cadena.

 

## <a name="examples"></a>Ejemplos


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





