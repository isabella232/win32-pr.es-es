---
title: Ejemplo de archivo SAMI
description: Ejemplo de archivo SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Reproductor de Windows Media,Synchronized Accessible Media Interchange (SAMI)
- Reproductor de Windows Media de objetos, Intercambio de medios accesibles sincronizado (SAMI)
- object model,Synchronized Accessible Media Interchange (SAMI)
- Reproductor de Windows Media Intercambio multimedia accesible móvil y sincronizado (SAMI)
- control Reproductor de Windows Media ActiveX, Intercambio multimedia accesible sincronizado (SAMI)
- Reproductor de Windows Media Control de ActiveX móviles, intercambio multimedia accesible sincronizado (SAMI)
- ActiveX control, Intercambio de medios accesibles sincronizado (SAMI)
- Intercambio multimedia accesible sincronizado (SAMI), archivos
- SAMI (intercambio multimedia accesible sincronizado), archivos
- Intercambio multimedia accesible sincronizado (SAMI), código de ejemplo
- SAMI (Synchronized Accessible Media Interchange), código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476174"
---
# <a name="sami-file-example"></a>Ejemplo de archivo SAMI

El código de ejemplo siguiente es un archivo SAMI completo con un conjunto de texto de título cerrado y varias declaraciones de clase para el estilo de texto y el lenguaje de subtítulos.


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



Los estilos definidos dentro de un archivo SAMI se ajustan a la sintaxis del selector CSS estándar para elementos, clases e IDs. En el elemento BODY, todos los elementos P tienen el estilo definido para el selector de elementos P en el elemento STYLE. El atributo class de un elemento especifica el idioma de ese elemento tal como lo definen los selectores de clase en el elemento STYLE (los selectores que comienzan por puntos). Los nombres de idioma especificados por los selectores de clases pueden ser cualquier cadena. Los elementos con el atributo ID especificado tienen un estilo adicional aplicado según lo indicado por los selectores de identificador en el elemento STYLE (los selectores con el prefijo \# de caracteres).

Cuando se usa junto con el Reproductor de Windows Media de objetos, los selectores de clase corresponden a *ClosedCaption*. **Propiedad SAMILang,** que se puede usar para especificar el idioma de los títulos. Los selectores de identificador corresponden a *ClosedCaption*. **Propiedad SAMIStyle,** que se puede usar para especificar el estilo en el que aparecerán los títulos.

Para obtener más información sobre cómo crear archivos SAMI, vea Understanding SAMI 1.0 (Descripción de SAMI 1.0) en el sitio [web de Microsoft.](/documentation/)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 