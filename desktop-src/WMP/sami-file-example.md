---
title: Ejemplo de archivo SAMI
description: Ejemplo de archivo SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Modelo de objetos de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player Mobile, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX de Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX móvil de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- Control ActiveX, intercambio de multimedia accesible sincronizado (SAMI)
- Intercambio de contenido multimedia accesible sincronizado (SAMI), archivos
- SAMI (intercambio de multimedia accesible sincronizado), archivos
- Intercambio de multimedia accesible sincronizado (SAMI), código de ejemplo
- SAMI (intercambio de multimedia accesible sincronizado), código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103914005"
---
# <a name="sami-file-example"></a>Ejemplo de archivo SAMI

El código de ejemplo siguiente es un archivo SAMI completo con un conjunto de texto de subtítulos y varias declaraciones de clase para el estilo de texto y el idioma del título.


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



Los estilos definidos dentro de un archivo SAMI se ajustan a la sintaxis de selector de CSS estándar para elementos, clases e identificadores. En el elemento BODY, todos los elementos P tienen el estilo definido para el selector de elementos P en el elemento STYLE. El atributo class de un elemento especifica el idioma de ese elemento tal y como se define en los selectores de clase en el elemento STYLE (los selectores que comienzan con puntos). Los nombres de idioma especificados por los selectores de clase pueden ser cualquier cadena. Los elementos con el atributo ID especificado tienen un estilo adicional aplicado según lo indicado por los selectores de identificador en el elemento STYLE (los selectores precedidos de \# caracteres).

Cuando se usa junto con el modelo de objetos de Media Player de Windows, los selectores de clase corresponden a *ClosedCaption*. Propiedad **SAMILang** , que se puede usar para especificar el idioma de los títulos. Los selectores de identificador corresponden a *ClosedCaption*. Propiedad **SAMIStyle** , que se puede usar para especificar el estilo en el que aparecerán los títulos.

Para obtener más información acerca de la creación de archivos SAMI, vea Descripción de SAMI 1,0 en el [sitio web de Microsoft](/documentation/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 