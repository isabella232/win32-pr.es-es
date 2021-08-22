---
title: Apéndice E Atributos de texto para Active Accessibility diccionario de Text Services
description: En este apéndice se proporciona información sobre los atributos de texto definidos en IAccDictionary.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539583f05e5140d96594490b0038b1a629f7760b13e4de223f6a8a3304c3901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134068"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Apéndice E: Atributos de texto para Active Accessibility diccionario de Text Services

En este apéndice se proporciona información sobre los atributos de texto definidos en [**IAccDictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary). Se organiza como una serie de tablas. Cada tabla incluye información sobre una categoría específica de atributos. Estas categorías están anidadas realmente, pero se separan a continuación para que pueda ver los atributos.

> [!Note]  
> Active Accessibility Text Services está en desuso. Consulte [Microsoft Windows Text Services Framework](../tsf/text-services-framework.md) para obtener más información sobre la entrada de texto avanzada y las tecnologías de lenguaje natural.

 

Cada entrada de una tabla proporciona un nombre de atributo y un nombre descriptivo, tipo, equivalente de Hojas de estilo CSS (CSS), equivalente de Text Object Model (TOM) y cualquier comentario adicional cuando corresponda. La columna equivalente de TOM proporciona información sobre el método TOM usado con el atributo (parte de las interfaces [**ITextFont,**](/windows/desktop/api/tom/nn-tom-itextfont) [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)o [**ITextPara).**](/windows/desktop/api/tom/nn-tom-itextpara) La información anterior a cada tabla indica qué interfaz admite los atributos; la información de la tabla equivalente de TOM indica el nombre del método. Cada entrada de la columna equivalente de TOM está asociada a dos métodos. Por ejemplo, la entrada Name está asociada a los **métodos GetName** **y SetName.**

Para obtener más información sobre [](../controls/text-object-model.md) estas interfaces, vea la documentación del modelo de objetos de texto en Windows Software Development Kit (SDK).

## <a name="font"></a>Fuente

Los atributos de la tabla siguiente están asociados a atributos de fuente generales. El equivalente de TOM es la [**interfaz ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nombre del atributo, nombre descriptivo       | Tipo     | Equivalente de CSS       | EQUIVALENTE DE TOM | Comentario           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| Font \_ FaceName, facename<br/> | VT \_ BSTR | Familia de fuentes: Verdana | Nombre           |                   |
| Tamaño \_ de fuentePts, sizePts<br/>   | VT \_ I4   | Tamaño de fuente: Xpt       | Size           | El tamaño está en puntos |



 

## <a name="font_style"></a>Estilo de \_ fuente

Los atributos de la tabla siguiente direcciona los atributos de estilo de fuente (por ejemplo, si el texto está establecido en negrita o cursiva). El equivalente de TOM es la [**interfaz ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nombre del atributo, nombre descriptivo                             | Tipo     | Equivalente de CSS              | EQUIVALENTE DE TOM                                            | Comentario                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| Estilo \_ de fuente \_ negrita, negrita<br/>                        | VT \_ BOOL | Peso de fuente: negrita           | Negrita                                                      |                           |
| Estilo \_ de fuente \_ cursiva, cursiva<br/>                    | VT \_ BOOL | Estilo de fuente: cursiva          | Cursiva                                                    |                           |
| Estilo \_ de \_ fuente SmallCaps, smallcaps<br/>              | VT \_ BOOL | Font-variant: small-caps    | SmallCaps                                                 |                           |
| Font \_ Style \_ Capitalize,capitalize<br/>             | VT \_ BOOL | Transformación de texto: mayúsculas  | No compatible                                             |                           |
| Estilo \_ de fuente en \_ mayúsculas, mayúsculas<br/>               | VT \_ BOOL | Transformación de texto: en mayúsculas   | AllCaps                                                   |                           |
| Estilo \_ de fuente en \_ minúsculas, minúsculas<br/>               | VT \_ BOOL | Transformación de texto: minúscula   | No compatible                                             |                           |
| Relieves \_ \_ de estilo de fuente, relieves<br/>                     | VT \_ BOOL | No compatible               | Emboss                                                    |                           |
| Font \_ Style En style En \_ style,en style (Estilo de fuente)<br/>                   | VT \_ BOOL | No compatible               | Grabar                                                   |                           |
| Estilo \_ de fuente \_ oculto                                       | VT \_ BOOL | No compatible               | Hidden                                                    |                           |
| \_Kerning de estilo de \_ fuente, kerning<br/>                   | VT \_ R4   | No compatible               | Kerning                                                   | Mismos valores que GetKerning |
| Estilo \_ de \_ fuente esbozado, descrito<br/>                 | VT \_ BOOL | No compatible               | Descrito                                                  |                           |
| Posición \_ de estilo de \_ fuente, posición<br/>                 | VT \_ R4   | No compatible               | Posición                                                  |                           |
| Estilo \_ de fuente \_ protegido                                    | VT \_ BOOL | No compatible               | Protegido                                                 |                           |
| Sombra \_ de estilo de \_ fuente, sombra<br/>                     | VT \_ BOOL | Alto de línea (menos números) | Shadow                                                    |                           |
| Espaciado \_ de estilo de \_ fuente, espaciado<br/>                   | VT \_ R4   | Espaciado de letras              | Espaciado                                                   | En puntos                 |
| Peso \_ del estilo de \_ fuente, peso<br/>                     | VT \_ I4   | Peso de fuente                 | Valores weightSame como font-weight y GetWeight<br/> |                           |
| Altura, \_ altura del estilo de \_ fuente<br/>                     | VT \_ R4   | Line-height                 | No compatible                                             | En puntos                 |
| \_Parpadeo de estilo de \_ fuente, parpadeo<br/>                       | VT \_ BOOL | Decoración de texto: parpadeo      | No compatible                                             |                           |
| \_Subíndice de estilo de \_ fuente, subíndice<br/>               | VT \_ BOOL | Alineación vertical: sub         | Subíndice (también Position)                                 |                           |
| \_Superíndice de estilo de \_ fuente, superíndice<br/>           | VT \_ BOOL | Alineación vertical: super       | Superíndice (también Posición)                               |                           |
| Color \_ de estilo de \_ fuente, color<br/>                       | VT \_ I4   | Color                       | ForeColor                                                 | Estilo COLORREF de RBG        |
| Estilo de \_ fuente \_ BackgroundColor, color de \_ fondo<br/> | VT \_ I4   | Color de fondo            | BackColor                                                 | Estilo COLORREF de RBG        |



 

## <a name="font_style_animation"></a>Animación de \_ estilo \_ de fuente

Los atributos de la siguiente animación de fuente de dirección de tabla. El equivalente de TOM es la [**interfaz ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nombre del atributo, nombre descriptivo                                              | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| Animación \_ de estilo de fuente \_ \_ LasVegasLights,LasVegas \_ lights<br/>         | VT \_ BOOL | No compatible  | Animación      |
| Animación de \_ estilo \_ de fuente \_ BlinkingBackground, fondo \_ parpadeante<br/> | VT \_ BOOL | No compatible  | Animación      |
| \_SparkleText de animación de estilo de \_ \_ fuente, texto de \_ sparkle<br/>               | VT \_ BOOL | No compatible  | Animación      |
| Animación \_ de estilo de fuente \_ \_ MarchingBlackAnts,marching \_ black \_ ants<br/> | VT \_ BOOL | No compatible  | Animación      |
| Animación \_ de estilo de fuente \_ \_ MarchingRedAnts,marching \_ red \_ ants<br/>     | VT \_ BOOL | No compatible  | Animación      |
| Animación \_ de estilo de fuente \_ \_ Shimmer,Shimmer<br/>                         | VT \_ BOOL | No compatible  | Animación      |
| \_ \_ WipeDown,wipeDown de animación \_ de estilo de fuente<br/>                       | VT \_ BOOL | No compatible  | Animación      |
| Animación de \_ \_ estilo de fuente \_ WipeRight,wipeRight<br/>                     | VT \_ BOOL | No compatible  | Animación      |



 

## <a name="font_style_underline"></a>Subrayado de \_ estilo \_ de fuente

Los atributos de la tabla siguiente direcciona los estilos de subrayado de las fuentes. El equivalente de TOM es la [**interfaz ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nombre del atributo, nombre descriptivo                     | Tipo     | Equivalente de CSS                | EQUIVALENTE DE TOM |
|---------------------------------------------------|----------|-------------------------------|----------------|
| Subrayado \_ de estilo de fuente \_ \_ single,single<br/>  | VT \_ BOOL | Decoración de texto: subrayado    | Subrayado      |
| Subrayado \_ de estilo de fuente \_ \_ double,double<br/> | VT \_ BOOL | Decoración de texto: línea a través | StrikeThrough  |



 

## <a name="font_style_strikethrough"></a>\_Tachado de estilo de \_ fuente

Los atributos de la tabla siguiente abordan los estilos de tachado de las fuentes.



| Nombre del atributo, nombre descriptivo                                         | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| Estilo \_ de fuente \_ \_ tachado único, \_ tachado a \_ uno<br/> | VT \_ BOOL | No compatible  | No compatible  |
| Estilo \_ de fuente \_ \_ tachado doble, \_ tachado a \_ doble<br/> | VT \_ BOOL | No compatible  | No compatible  |



 

## <a name="font_style_overline"></a>Estilo de \_ fuente \_ sobrelineado

Los atributos de la tabla siguiente direcciona los estilos de línea overline para las fuentes.



| Nombre del atributo, nombre descriptivo                             | Tipo     | Equivalente de CSS            | EQUIVALENTE DE TOM |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| Estilo \_ de fuente \_ \_ sobrelínea única, \_ sobrelínea única<br/> | VT \_ BOOL | Decoración de texto: sobrelínea | No compatible  |
| Estilo \_ de fuente \_ overline \_ Double,overline \_ double<br/> | VT \_ BOOL | Decoración de texto: sobrelínea | No compatible  |



 

## <a name="text"></a>Texto

Los atributos de la tabla siguiente abordan los atributos generales de formato de texto.



| Nombre del atributo, nombre descriptivo                     | Tipo        | Equivalente de CSS | EQUIVALENTE DE TOM                                       | Comentario                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| Text \_ VerticalWriting, escritura vertical<br/> | VT \_ BOOL    | No compatible  | no admitido                                        | Como se usa en chino/japonés                                                           |
| Texto \_ RightToLeft,righttoleft<br/>          | VT \_ BOOL    | Dirección      | No compatible                                        |                                                                                       |
| \_ReadOnly de texto, solo lectura<br/>               | VT \_ BOOL    | No compatible  | ITextFont::CanChange, ITextRange::CanEdit            | La propiedad editable del documento tiene prioridad                                     |
| Idioma \_ de texto, idioma<br/>                | VT \_ I4      | No compatible  | ITextFont::GetLanguageID, ITextFont::SetLanguageID   | LANGID                                                                                |
| Orientación \_ del texto, orientación<br/>          | VT \_ I4      | No compatible  | No compatible                                        | 10??? de un grado                                                                     |
| Text \_ EmbeddedObject, objeto \_ incrustado<br/>  | VT \_ BOOL    | No compatible  | No compatible                                        | Permite buscar objetos incrustados                                                 |
| Vínculo \_ de texto, vínculo<br/>                        | VT \_ UNKNOWN | Vínculo           | No compatible                                        | Puntero de interfaz al objeto ; llamar a QueryInterface para cualquier interfaz de interés |
| Guiones \_ de texto, guiones<br/>          | VT \_ BOOL    | No compatible  | ITextPara::GetHyphenation, ITextPara::SetHyphenation |                                                                                       |



 

## <a name="text_alignment"></a>Alineación de \_ texto

Los atributos de la tabla siguiente direcciona la alineación del texto. El equivalente de TOM es [**la interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo               | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM |
|---------------------------------------------|----------|----------------|----------------|
| Alineación \_ de texto \_ izquierda,izquierda<br/>       | VT \_ BOOL | Alineación de texto     | Alignment      |
| Alineación \_ de texto a la \_ derecha, derecha<br/>     | VT \_ BOOL | Alineación de texto     | Alignment      |
| Centro \_ de \_ alineación de texto, centro<br/>   | VT \_ BOOL | Alineación de texto     | Alignment      |
| Justificación \_ de \_ alineación de texto, justificación<br/> | VT \_ BOOL | Alineación de texto     | Alignment      |



 

## <a name="text_para"></a>Text \_ Para

Los atributos de la tabla siguiente de formato de dirección para párrafos. El equivalente de TOM es [**la interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo                              | Tipo   | Equivalente de CSS | EQUIVALENTE DE TOM  | Comentario |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| Text \_ Para \_ FirstLineIndent, sangría \_ de primera \_ línea<br/> | VT \_ R4 | No compatible  | FirstLineIndent | En pts  |
| Text \_ Para \_ LeftIndent,left \_ indent<br/>             | VT \_ R4 | No compatible  | LeftIndent      | En pts  |
| Text \_ Para \_ RightIndent,right \_ indent<br/>           | VT \_ R4 | No compatible  | RightIndent     | En pts  |
| Text \_ Para \_ SpaceAfter,space \_ after<br/>             | VT \_ R4 | No compatible  | SpaceAfter      | En pts  |
| Text \_ Para \_ SpaceBefore,space \_ after<br/>            | VT \_ R4 | No compatible  | SpaceAfter      | En pts  |



 

## <a name="text_para_linespacing"></a>Text \_ Para \_ lineSpacing

Los atributos de la tabla siguiente direcciona el espaciado de línea en párrafos. El equivalente de TOM es la [**interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo                               | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM | Comentario  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| Text \_ Para \_ lineSpacing \_ Single,single<br/>           | VT \_ BOOL | No compatible  | LineSpacing    |          |
| Text \_ Para \_ lineSpacing \_ OnePtFive,one \_ pt \_ five<br/> | VT \_ BOOL | No compatible  | LineSpacing    |          |
| Text \_ Para \_ lineSpacing \_ Double,double<br/>           | VT \_ BOOL | No compatible  | LineSpacing    |          |
| Text \_ Para \_ lineSpacing \_ AtLeast, at \_ least<br/>       | VT \_ R4   | No compatible  | LineSpacing    | En líneas |
| Línea \_ de \_ parapase de \_ textoSpacing Exactly,exactly<br/>         | VT \_ R4   | No compatible  | LineSpacing    | En líneas |
| Text \_ Para \_ lineSpacing \_ Mutiple,multiple<br/>        | VT \_ R4   | No compatible  | LineSpacing    | En líneas |



 

## <a name="text_list"></a>Lista de \_ texto

Los atributos de las siguientes listas de direcciones de tabla y niveles de listas de texto. El equivalente de TOM es la [**interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo | Tipo   | Equivalente de CSS | EQUIVALENTE DE TOM | Comentario                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| Nivel \_ de lista de \_ textoIndex,       | VT \_ I4 | No compatible  | ListLevelIndex | Donde 1 es la lista más externa, 2 es el siguiente nivel, y así sucesivamente |



 

## <a name="text_list_type"></a>Tipo de \_ lista \_ de texto

Los atributos de los siguientes estilos de lista de direcciones de tabla para texto. El equivalente de TOM es la [**interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo                          | Tipo     | Equivalente de CSS  | EQUIVALENTE DE TOM |
|--------------------------------------------------------|----------|-----------------|----------------|
| Tipo \_ de lista de texto \_ \_ Bullet,bullet<br/>             | VT \_ BOOL | Tipo de lista       | ListType       |
| Tipo \_ de lista de texto \_ \_ árabe,árabe<br/>             | VT \_ BOOL | Tipo de estilo de lista | ListType       |
| Tipo \_ de lista de texto \_ \_ LowerLetter, letra \_ inferior<br/> | VT \_ BOOL | Tipo de estilo de lista | ListType       |
| Tipo \_ de lista de texto \_ \_ UpperLetter,upper \_ letter<br/> | VT \_ BOOL | Tipo de estilo de lista | ListType       |
| Tipo \_ de lista de texto \_ \_ LowerRoman,lower \_ roman<br/>   | VT \_ BOOL | Tipo de estilo de lista | ListType       |
| Tipo \_ de lista de texto \_ \_ UpperRoman,upper \_ roman<br/>   | VT \_ BOOL | Tipo de estilo de lista | ListType       |



 

## <a name="app"></a>Aplicación



| Nombre del atributo, nombre descriptivo                         | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM |
|-------------------------------------------------------|----------|----------------|----------------|
| \_Escritura incorrecta de la aplicación, ortografía \_ incorrecta<br/> | VT \_ BOOL |                | No compatible  |
| \_Aplicación IncorrectGrammar,gramática \_ incorrecta<br/>   | VT \_ BOOL |                | No compatibles  |



 

 

