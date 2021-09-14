---
title: ELEMENTO ENTRY
description: El elemento ENTRY especifica un Windows multimedia que se representará como un clip.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Elemento ENTRY Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241965"
---
# <a name="entry-element"></a>ELEMENTO ENTRY

El **elemento ENTRY** especifica un Windows multimedia que se representará como un clip.

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a>Atributos

**CLIENTSKIP**

Valor que indica si el usuario puede omitir el avance más allá del clip.

Estos son algunos de los valores posibles.



| Value | Descripción                                   |
|-------|-----------------------------------------------|
| SÍ   | Predeterminada. El usuario puede omitir el avance más allá del clip. |
| No    | El usuario no puede omitir el avance más allá del clip.       |



 

**SKIPIFREF**

Valor que indica si Reproductor de Windows Media omitir este clip cuando el elemento **ENTRY** se incluye en un segundo metarchivo mediante el uso de **un elemento ENTRYREF.**

Estos son algunos de los valores posibles.



| Value | Descripción                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| SÍ   | Reproductor de Windows Media omitirá esta entrada, si se hace referencia a través de un **elemento ENTRYREF.** |
| No    | Predeterminada. Reproductor de Windows Media omitirá esta entrada.                                   |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios | **ASX**, **EVENT**, **REPEAT**                                                                                                                                                               |
| Elementos secundarios  | **ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **DURATION**, **ENDMARKER**, **MOREINFO**, **PARAM**, **PREVIEWDURATION**, **REF**, **STARTMARKER**, **STARTTIME**, **TITLE** |



 

## <a name="remarks"></a>Observaciones

Este elemento es la construcción fundamental en un metarchivo Windows multimedia. El **elemento ENTRY** y sus atributos asociados definen la meta-información para un único fragmento lógico de contenido, denominado clip. Los elementos secundarios dentro del ámbito de un elemento **ENTRY** definen el contenido multimedia para que Reproductor de Windows Media se abra **(REF),** información sobre el clip que Reproductor de Windows Media mostrará como texto **(AUTHOR,** **COPYRIGHT**, **TITLE)** y otras configuraciones relacionadas con el clip. El elemento secundario **REF** vincula el contenido que se va a transmitir para el elemento **PRIMARIO ENTRY.** Aunque el script no se interrumpirá, **ENTRY** no tiene sentido sin un **elemento secundario REF.**

Si el valor del atributo **CLIENTSKIP** es NO, el usuario no puede omitir el fragmento de contenido definido por el **elemento ENTRY.** Esto no funciona si el elemento **SECUNDARIO REF hace** referencia a otro metarchivo. Se debe hacer referencia a los metarchivos anidados mediante **el elemento ENTRYREF.**

El **atributo SKIPIFREF** solo pertenece a los elementos **ENTRY** que se incluyen en un segundo metarchivo mediante el uso de un **elemento ENTRYREF.** El **elemento ENTRYREF** hace referencia a otro metarchivo para la inclusión lógica en el archivo actual. Si el valor del atributo **SKIPIFREF** para un elemento **ENTRY** del archivo de metarchivo al que se hace referencia es YES, Reproductor de Windows Media omite esta entrada de entrada y pasa al siguiente elemento **ENTRY,** si existe. El siguiente **elemento ENTRY** puede ser la siguiente entrada del archivo original o la siguiente entrada del metarchivo al que se hace referencia en el **elemento ENTRYREF.**

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
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

 

 





