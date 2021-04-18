---
title: Elemento ENTRY
description: El elemento ENTRY especifica un archivo de Windows Media para representarlo como un clip.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Elemento de entrada de Windows Media Player
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700323"
---
# <a name="entry-element"></a>Elemento ENTRY

El elemento **entry** especifica un archivo de Windows Media para representarlo como un clip.

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a>Atributos

**CLIENTSKIP**

Valor que indica si el usuario puede saltar hacia delante después del clip.

Estos son algunos de los valores posibles.



| Value | Descripción                                   |
|-------|-----------------------------------------------|
| SÍ   | Predeterminada. El usuario puede saltar adelante más allá del clip. |
| No    | El usuario no puede saltar adelante más allá del clip.       |



 

**SKIPIFREF**

Valor que indica si Windows Media Player debe omitir este clip cuando el elemento de **entrada** está incluido en un segundo metarchivo mediante el uso de un elemento **ENTRYREF** .

Estos son algunos de los valores posibles.



| Value | Descripción                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| SÍ   | Windows Media Player omitirá esta entrada, si se hace referencia a ella a través de un elemento **ENTRYREF** . |
| No    | Predeterminada. Windows Media Player no omitirá esta entrada.                                   |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios | **ASX**, **evento**, **repetición**                                                                                                                                                               |
| Elementos secundarios  | **abstract**, **Author**, **banner**, **base**, **Copyright**, **Duration**, **ENDMARKER**, **MOREINFO**, **param**, **PREVIEWDURATION**, **ref**, **STARTMARKER**, **STARTTIME**, **title** |



 

## <a name="remarks"></a>Observaciones

Este elemento es la construcción fundamental en un metarchivo de Windows Media. El elemento de **entrada** y sus atributos asociados definen la metainformación de una única parte lógica de contenido, denominada clip. Los elementos secundarios dentro del ámbito de un elemento de **entrada** definen el contenido multimedia para Windows Media Player que se va a abrir (**ref**), información sobre el clip que Windows Media Player mostrará como texto (**autor**, **Copyright**, **título**) y otras opciones relacionadas con el clip. El elemento secundario **ref** vincula el contenido que se va a transmitir para el elemento de **entrada** primario. Aunque el script no se interrumpirá, la **entrada** no tiene sentido sin un elemento secundario **ref** .

Si el valor del atributo **CLIENTSKIP** es no, el usuario no puede saltar adelante más allá del contenido definido por el elemento **entry** . Esto no funciona si el elemento **ref** secundario hace referencia a otro metarchivo. Se debe hacer referencia a los metaarchivos anidados mediante el elemento **ENTRYREF** .

El atributo **SKIPIFREF** solo pertenece a los elementos de **entrada** que se incluyen en un segundo metarchivo mediante el uso de un elemento **ENTRYREF** . El elemento **ENTRYREF** hace referencia a otro metarchivo para la inclusión lógica en el archivo actual. Si el valor del atributo **SKIPIFREF** de un elemento de **entrada** del archivo de metarchivo al que se hace referencia es sí, Windows Media Player omitirá esta entrada extraída y pasará al siguiente elemento de **entrada** , si existe. El siguiente elemento de **entrada** puede ser la siguiente entrada en el archivo original o la entrada siguiente en el metarchivo al que se hace referencia en el elemento **ENTRYREF** .

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
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





