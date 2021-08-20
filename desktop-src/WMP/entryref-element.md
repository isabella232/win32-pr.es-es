---
title: ELEMENTO ENTRYREF
description: El elemento ENTRYREF apunta a los elementos ENTRY de un metarchivo externo.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Elemento ENTRYREF Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61fa3403fc56c6a02f97330b3c2f62d1c3e3c723f50672520ea42fb4a2018705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996675"
---
# <a name="entryref-element"></a>ELEMENTO ENTRYREF

El **elemento ENTRYREF** apunta a los **elementos ENTRY** de un metarchivo externo.

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**HREF** (obligatorio)

Dirección URL a un metarchivo al que se hace referencia.

**CLIENTBIND**

Este atributo ya no se admite.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                       |
|-----------------|--------------------------------|
| Elementos primarios | **ASX**, **EVENT**, **REPEAT** |
| Elementos secundarios  | Ninguno                           |



 

## <a name="remarks"></a>Observaciones

Este elemento apunta al contenido de un metarchivo externo. Reproductor de Windows Media procesa los elementos **ENTRY** del metarchivo al que se hace referencia como si estuvieran incluidos en el metarchivo principal en la posición del **elemento ENTRYREF.** Sin embargo, omite los elementos **ENTRY** del metarchivo al que se hace referencia que tienen el atributo **SKIPIFREF** establecido en YES.

Reproductor de Windows Media 7.0, 7.1 y Reproductor de Windows Media para Windows XP omiten los elementos **ENTRYREF** del metarchivo al que se hace referencia. Por lo tanto, los metarchivos solo se pueden anidar un nivel de profundidad cuando se usan estas versiones del reproductor. Reproductor de Windows Media omite también el elemento **ASX** del archivo al que se hace referencia junto con sus atributos. Reproductor de Windows Media serie 9 o posterior admite el anidamiento de metarchivos de hasta cinco niveles de profundidad.

La dirección URL especificada en el **atributo HREF** se convierte en la dirección URL base de las direcciones URL relativas del metarchivo externo. Esta dirección URL se usa cuando se reproduce una entrada del metarchivo externo y el usuario la agrega a la biblioteca.

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
| Versión<br/> | Reproductor de Windows Media versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





