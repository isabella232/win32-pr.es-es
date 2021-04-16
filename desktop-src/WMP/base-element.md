---
title: Elemento BASE
description: El elemento BASE define una cadena de dirección URL anexada al principio de las direcciones URL enviadas a Windows Media Player.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Windows Media Player de elementos BASE
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700007"
---
# <a name="base-element"></a>Elemento BASE

El elemento **base** define una cadena de dirección URL anexada al principio de las direcciones URL enviadas a Windows Media Player.

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obligatorio)

Cadena anexada al frente a las direcciones URL enviadas a Windows Media Player. El valor predeterminado es la cadena nula ("").

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ASX**, **entrada** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define una cadena de dirección URL anexada al principio de las direcciones URL de volteo de URL enviadas a Windows Media Player. URL: el volteo es un mecanismo de scripting que hace que Windows Media Player abra una nueva dirección URL en un explorador o marco del explorador cuando recibe un comando de script.

El elemento **base** es similar a un directorio particular para los vínculos relativos. Solo afecta a las direcciones URL enviadas mediante comandos de script como parte del flujo de contenido que se reproduce en Windows Media Player.

Un elemento **base** definido como elemento secundario de un elemento **ASX** se convierte en el valor predeterminado para todo el metarchivo. Un elemento **base** definido en un elemento **entry** reemplaza cualquier elemento **base** del elemento **ASX** primario (solo para ese elemento **entry** ).

> [!Note]  
> Si el atributo **href** no termina con un carácter/, Windows Media Player anexa uno al final de la cadena.

 

## <a name="examples"></a>Ejemplos


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





