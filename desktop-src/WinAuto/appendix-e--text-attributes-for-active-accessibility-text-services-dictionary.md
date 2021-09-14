---
title: Apéndice E Atributos de texto para el diccionario Active Accessibility Text Services
description: En este apéndice se proporciona información sobre los atributos de texto que se definen en IAccDictionary.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588c827764d17c2576efaa5e3117527e23d1da26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070712"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Apéndice E: Atributos de texto para el diccionario Active Accessibility Text Services

En este apéndice se proporciona información sobre los atributos de texto que se definen en [**IAccDictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary). Se organiza como una serie de tablas. Cada tabla incluye información sobre una categoría específica de atributos. Estas categorías están anidadas, pero están separadas a continuación para que pueda ver los atributos.

> [!Note]  
> Active Accessibility Text Services está en desuso. Consulte Microsoft Windows Text Services Framework más [información](../tsf/text-services-framework.md) sobre la entrada de texto avanzada y las tecnologías de lenguaje natural.

 

Cada entrada de una tabla proporciona un nombre de atributo y un nombre descriptivo, tipo, equivalente Hojas de estilo CSS (CSS), equivalente al Modelo de objetos de texto (TOM) y cualquier comentario adicional cuando corresponda. La columna equivalente de TOM proporciona información sobre el método TOM utilizado con el atributo (parte de las interfaces [**ITextFont,**](/windows/desktop/api/tom/nn-tom-itextfont) [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)o [**ITextPara).**](/windows/desktop/api/tom/nn-tom-itextpara) La información anterior a cada tabla indica qué interfaz admite los atributos; la información de la tabla equivalente de TOM indica el nombre del método. Cada entrada de la columna equivalente de TOM está asociada a dos métodos. Por ejemplo, la entrada Name está asociada a los **métodos GetName** **y SetName.**

Para obtener más información sobre estas interfaces, consulte [la](../controls/text-object-model.md) documentación del modelo de objetos de texto en Windows Software Development Kit (SDK).

## <a name="font"></a>Fuente

Los atributos de la tabla siguiente están asociados a atributos de fuente generales. El equivalente de TOM es la [**interfaz ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nombre del atributo, nombre descriptivo       | Tipo     | Equivalente de CSS       | EQUIVALENTE DE TOM | Comentario           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| Font \_ FaceName, facename<br/> | VT \_ BSTR | Familia de fuentes: Verdana | Nombre           |                   |
| Tamaño \_ de fuentePts, sizePts<br/>   | VT \_ I4   | Tamaño de fuente: Xpt       | Size           | El tamaño está en puntos |



 

## <a name="font_style"></a>Estilo de \_ fuente

Los atributos de la tabla siguiente direcciona los atributos de estilo de fuente (por ejemplo, si el texto está establecido en negrita o en cursiva). El equivalente de TOM es la [**interfaz ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nombre del atributo, nombre descriptivo                             | Tipo     | Equivalente de CSS              | EQUIVALENTE DE TOM                                            | Comentario                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| Estilo de \_ fuente \_ negrita, negrita<br/>                        | VT \_ BOOL | Peso de fuente: negrita           | Negrita                                                      |                           |
| Estilo de \_ fuente \_ cursiva, cursiva<br/>                    | VT \_ BOOL | Estilo de fuente: cursiva          | Cursiva                                                    |                           |
| Estilo \_ de \_ fuente SmallCaps, smallcaps<br/>              | VT \_ BOOL | Font-variant: small-caps    | SmallCaps                                                 |                           |
| Estilo \_ de fuente en \_ mayúsculas y mayúsculas<br/>             | VT \_ BOOL | Transformación de texto: en mayúsculas  | No compatible                                             |                           |
| Estilo \_ de \_ fuente Mayúsculas, mayúsculas<br/>               | VT \_ BOOL | Transformación de texto: mayúsculas   | AllCaps                                                   |                           |
| Estilo \_ de fuente en \_ minúsculas, minúscula<br/>               | VT \_ BOOL | Transformación de texto: minúscula   | No compatible                                             |                           |
| Estilo \_ de \_ fuente relieves,relieves<br/>                     | VT \_ BOOL | No compatible               | Emboss                                                    |                           |
| Estilo \_ de fuente En style en \_ style,en style<br/>                   | VT \_ BOOL | No compatible               | Grabar                                                   |                           |
| Estilo de \_ fuente \_ oculto                                       | VT \_ BOOL | No compatible               | Hidden                                                    |                           |
| \_Kerning de estilo de \_ fuente, kerning<br/>                   | VT \_ R4   | No compatible               | Kerning                                                   | Los mismos valores que GetKerning |
| Estilo \_ de \_ fuente esquemateado, con contorno<br/>                 | VT \_ BOOL | No compatible               | Descrito                                                  |                           |
| Posición \_ de estilo de \_ fuente, posición<br/>                 | VT \_ R4   | No compatible               | Posición                                                  |                           |
| Estilo \_ de fuente \_ protegido                                    | VT \_ BOOL | No compatible               | Protegido                                                 |                           |
| Sombra \_ de estilo de \_ fuente, sombra<br/>                     | VT \_ BOOL | Alto de línea (menos números) | Shadow                                                    |                           |
| Espaciado \_ de estilo de \_ fuente, espaciado<br/>                   | VT \_ R4   | Espaciado de letras              | Espaciado                                                   | En puntos                 |
| Grosor \_ del estilo de \_ fuente, peso<br/>                     | VT \_ I4   | Peso de fuente                 | Valores weightSame como font-weight y GetWeight<br/> |                           |
| Font \_ Style \_ Height,height<br/>                     | VT \_ R4   | Line-height                 | No compatible                                             | En puntos                 |
| \_Parpadeo de estilo de \_ fuente, parpadeo<br/>                       | VT \_ BOOL | Decoración de texto: parpadeo      | No compatible                                             |                           |
| \_Subíndice de estilo de \_ fuente, subíndice<br/>               | VT \_ BOOL | Alineación vertical: sub         | Subíndice (también Posición)                                 |                           |
| \_Superíndice de estilo de \_ fuente, superíndice<br/>           | VT \_ BOOL | Alineación vertical: super       | Superíndice (también Posición)                               |                           |
| Color \_ de estilo de \_ fuente, color<br/>                       | VT \_ I4   | Color                       | ForeColor                                                 | Estilo COLORREF de RBG        |
| BackgroundColor \_ \_ de estilo de fuente, color de \_ fondo<br/> | VT \_ I4   | Color de fondo            | BackColor                                                 | Estilo COLORREF de RBG        |



 

## <a name="font_style_animation"></a>Animación \_ de estilo de \_ fuente

Los atributos de la siguiente animación de fuente de dirección de tabla. El equivalente de TOM es la [**interfaz ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nombre del atributo, nombre descriptivo                                              | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| Animaciones \_ de estilo de fuente \_ \_ LasVegasLights,LasVegas \_ lights<br/>         | VT \_ BOOL | No compatible  | Animación      |
| Animación \_ de estilo de fuente \_ \_ blinkingBackground, fondo \_ parpadeante<br/> | VT \_ BOOL | No compatible  | Animación      |
| \_SparkleText de animación de estilo de \_ \_ fuente, texto de \_ sparkle<br/>               | VT \_ BOOL | No compatible  | Animación      |
| Animación \_ de estilo de fuente \_ \_ MarchingBlackAnts,marching \_ black \_ ants<br/> | VT \_ BOOL | No compatible  | Animación      |
| Animación \_ de estilo de fuente \_ \_ MarchingRedAnts,marching \_ red \_ ants<br/>     | VT \_ BOOL | No compatible  | Animación      |
| Animación \_ de estilo de fuente \_ \_ Shimmer,Shimmer<br/>                         | VT \_ BOOL | No compatible  | Animación      |
| Font \_ Style \_ Animation \_ WipeDown,wipeDown<br/>                       | VT \_ BOOL | No compatible  | Animación      |
| Animación \_ de estilo de fuente \_ \_ WipeRight,wipeRight<br/>                     | VT \_ BOOL | No compatible  | Animación      |



 

## <a name="font_style_underline"></a>Subrayado \_ de estilo de \_ fuente

Los atributos de la tabla siguiente direcciona los estilos de subrayado de las fuentes. El equivalente de TOM es la [**interfaz ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nombre del atributo, nombre descriptivo                     | Tipo     | Equivalente de CSS                | EQUIVALENTE DE TOM |
|---------------------------------------------------|----------|-------------------------------|----------------|
| Subrayado \_ de estilo de fuente \_ \_ single,single<br/>  | VT \_ BOOL | Decoración de texto: subrayado    | Subrayado      |
| Subrayado \_ \_ double,double de estilo \_ de fuente<br/> | VT \_ BOOL | Decoración de texto: línea a través | StrikeThrough  |



 

## <a name="font_style_strikethrough"></a>\_Tachado de estilo de \_ fuente

Los atributos de la tabla siguiente direccionan los estilos de tachado para las fuentes.



| Nombre del atributo, nombre descriptivo                                         | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| Estilo \_ de fuente \_ \_ tachado single,strike \_ through \_ single<br/> | VT \_ BOOL | No compatible  | No compatible  |
| Estilo \_ de fuente \_ \_ tachado doble, \_ tachado a \_ doble<br/> | VT \_ BOOL | No compatible  | No compatible  |



 

## <a name="font_style_overline"></a>Estilo de \_ fuente \_ sobrelínea

Los atributos de la tabla siguiente direcciona los estilos de línea para las fuentes.



| Nombre del atributo, nombre descriptivo                             | Tipo     | Equivalente de CSS            | EQUIVALENTE DE TOM |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| Estilo \_ de fuente \_ \_ sobrelineado single,overline \_ single<br/> | VT \_ BOOL | Decoración de texto: sobrelínea | No compatible  |
| Estilo \_ de fuente \_ \_ sobrelínea doble, línea doble \_ sobrelínea<br/> | VT \_ BOOL | Decoración de texto: sobrelínea | No compatible  |



 

## <a name="text"></a>Texto

Los atributos de la tabla siguiente direcciona los atributos generales de formato de texto.



| Nombre del atributo, nombre descriptivo                     | Tipo        | Equivalente de CSS | EQUIVALENTE DE TOM                                       | Comentario                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| Text \_ VerticalWriting, escritura vertical<br/> | VT \_ BOOL    | No compatible  | no admitido                                        | Como se usa en chino/japonés                                                           |
| Texto \_ RightToLeft,righttoleft<br/>          | VT \_ BOOL    | Dirección      | No compatible                                        |                                                                                       |
| Text \_ ReadOnly,read only<br/>               | VT \_ BOOL    | No compatible  | ITextFont::CanChange, ITextRange::CanEdit            | La propiedad editable del documento tiene prioridad                                     |
| Idioma \_ de texto, idioma<br/>                | VT \_ I4      | No compatible  | ITextFont::GetLanguageID, ITextFont::SetLanguageID   | LANGID                                                                                |
| Orientación \_ del texto, orientación<br/>          | VT \_ I4      | No compatible  | No compatible                                        | 10??? de un grado                                                                     |
| Text \_ EmbeddedObject, objeto \_ incrustado<br/>  | VT \_ BOOL    | No compatible  | No compatible                                        | Permite buscar objetos incrustados                                                 |
| Vínculo \_ de texto, vínculo<br/>                        | VT \_ UNKNOWN | Vínculo           | No compatible                                        | Puntero de interfaz al objeto ; llamar a QueryInterface para cualquier interfaz de interés |
| Guiones \_ de texto, guiones<br/>          | VT \_ BOOL    | No compatible  | ITextPara::GetHyphenation, ITextPara::SetHyphenation |                                                                                       |



 

## <a name="text_alignment"></a>Alineación de \_ texto

Los atributos de la siguiente tabla direcciona la alineación del texto. El equivalente de TOM es la [**interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo               | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM |
|---------------------------------------------|----------|----------------|----------------|
| Alineación \_ de \_ texto izquierda,izquierda<br/>       | VT \_ BOOL | Alineación de texto     | Alineación      |
| Alineación \_ de \_ texto derecha,derecha<br/>     | VT \_ BOOL | Alineación de texto     | Alineación      |
| Text \_ Alignment \_ Center,center<br/>   | VT \_ BOOL | Alineación de texto     | Alineación      |
| Justificación \_ de \_ alineación de texto, justificación<br/> | VT \_ BOOL | Alineación de texto     | Alineación      |



 

## <a name="text_para"></a>Text \_ Para

Los atributos de la tabla siguiente tienen formato de dirección para párrafos. El equivalente de TOM es la [**interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo                              | Tipo   | Equivalente de CSS | EQUIVALENTE DE TOM  | Comentario |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| Text \_ Para \_ FirstLineIndent, primera \_ sangría de \_ línea<br/> | VT \_ R4 | No compatible  | FirstLineIndent | En pts  |
| Text \_ Para \_ LeftIndent,left \_ indent<br/>             | VT \_ R4 | No compatible  | LeftIndent      | En pts  |
| Text \_ Para \_ RightIndent,right \_ indent<br/>           | VT \_ R4 | No compatible  | RightIndent     | En pts  |
| Text \_ Para \_ SpaceAfter,space \_ after<br/>             | VT \_ R4 | No compatible  | SpaceAfter      | En pts  |
| Text \_ Para \_ SpaceBefore,space \_ after<br/>            | VT \_ R4 | No compatible  | SpaceAfter      | En pts  |



 

## <a name="text_para_linespacing"></a>Text \_ Para \_ lineSpacing

Los atributos de la tabla siguiente direcciona el espaciado de línea en párrafos. El equivalente de TOM es [**la interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo                               | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM | Comentario  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| Text \_ Para \_ lineSpacing \_ Single,single<br/>           | VT \_ BOOL | No compatible  | LineSpacing    |          |
| Text \_ Para \_ lineSpacing \_ OnePtFive,one \_ pt \_ five<br/> | VT \_ BOOL | No compatible  | LineSpacing    |          |
| Text \_ Para \_ lineSpacing \_ Double,double<br/>           | VT \_ BOOL | No compatible  | LineSpacing    |          |
| Text \_ Para \_ lineSpacing \_ AtLeast,at \_ least<br/>       | VT \_ R4   | No compatible  | LineSpacing    | En líneas |
| Text \_ Para \_ lineSpacing \_ Exactly,exactly<br/>         | VT \_ R4   | No compatible  | LineSpacing    | En líneas |
| Text \_ Para \_ lineSpacing \_ Mutiple,multiple<br/>        | VT \_ R4   | No compatible  | LineSpacing    | En líneas |



 

## <a name="text_list"></a>Lista de \_ texto

Los atributos de las siguientes listas de direcciones de tabla y niveles de listas de texto. El equivalente de TOM es [**la interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo | Tipo   | Equivalente de CSS | EQUIVALENTE DE TOM | Comentario                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| Text \_ List \_ LevelIndex,       | VT \_ I4 | No compatible  | ListLevelIndex | Donde 1 es la lista más externa, 2 es el siguiente nivel, y así sucesivamente |



 

## <a name="text_list_type"></a>Tipo de \_ lista de \_ texto

Los atributos de los siguientes estilos de lista de direcciones de tabla para texto. El equivalente de TOM es [**la interfaz ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nombre del atributo, nombre descriptivo                          | Tipo     | Equivalente de CSS  | EQUIVALENTE DE TOM |
|--------------------------------------------------------|----------|-----------------|----------------|
| Tipo \_ de lista de texto \_ \_ bullet,bullet<br/>             | VT \_ BOOL | Tipo de lista       | ListType       |
| Tipo \_ de lista de texto \_ \_ árabe,árabe<br/>             | VT \_ BOOL | Tipo de estilo de lista | ListType       |
| Tipo \_ de lista de texto \_ \_ LowerLetter, letra \_ inferior<br/> | VT \_ BOOL | Tipo de estilo de lista | ListType       |
| Tipo \_ de lista de texto \_ \_ UpperLetter, letra \_ superior<br/> | VT \_ BOOL | Tipo de estilo de lista | ListType       |
| Tipo \_ de lista de texto \_ \_ LowerRoman,lower \_ roman<br/>   | VT \_ BOOL | Tipo de estilo de lista | ListType       |
| Tipo \_ de lista de texto \_ \_ UpperRoman,upper \_ roman<br/>   | VT \_ BOOL | Tipo de estilo de lista | ListType       |



 

## <a name="app"></a>Aplicación



| Nombre del atributo, nombre descriptivo                         | Tipo     | Equivalente de CSS | EQUIVALENTE DE TOM |
|-------------------------------------------------------|----------|----------------|----------------|
| Corrección \_ incorrecta de la aplicación, ortografía \_ incorrecta<br/> | VT \_ BOOL |                | No compatible  |
| Aplicación \_ IncorrectGrammar, gramática \_ incorrecta<br/>   | VT \_ BOOL |                | No compatibles  |



 

 

