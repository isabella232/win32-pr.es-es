---
title: Elemento ENTRYREF
description: El elemento ENTRYREF apunta a los elementos de entrada de un metarchivo externo.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Elemento ENTRYREF Media Player Windows
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698719"
---
# <a name="entryref-element"></a>Elemento ENTRYREF

El elemento **ENTRYREF** apunta a los elementos de **entrada** de un metarchivo externo.

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obligatorio)

Dirección URL de un metarchivo al que se hace referencia.

**CLIENTBIND**

Este atributo ya no se admite.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                       |
|-----------------|--------------------------------|
| Elementos primarios | **ASX**, **evento**, **repetición** |
| Elementos secundarios  | Ninguno                           |



 

## <a name="remarks"></a>Observaciones

Este elemento apunta al contenido de un metarchivo externo. Windows Media Player procesa los elementos de **entrada** del metarchivo al que se hace referencia como si estuvieran incluidos en el metarchivo principal situado en la posición del elemento **ENTRYREF** . Sin embargo, omite cualquier elemento de **entrada** del metarchivo al que se hace referencia que tenga el atributo **SKIPIFREF** establecido en sí.

Windows Media Player 7,0, 7,1 y Windows Media Player para Windows XP omiten los elementos **ENTRYREF** del metarchivo al que se hace referencia. Por lo tanto, los metaarchivos solo se pueden anidar un nivel en profundidad al usar estas versiones del reproductor. Windows Media Player también omite el elemento **ASX** en el archivo al que se hace referencia junto con sus atributos. Windows Media Player 9 series o posterior admiten el anidamiento de metaarchivos hasta cinco niveles de profundidad.

La dirección URL especificada en el atributo **href** se convierte en la dirección URL base de las direcciones URL relativas del metarchivo externo. Esta dirección URL se usa cuando se está reproduciendo una entrada del metarchivo externo y el usuario la agrega a la biblioteca.

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------|
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





