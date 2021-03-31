---
title: Apéndice E atributos de texto para Active Accessibility Diccionario de servicios de texto
description: Este apéndice proporciona información sobre los atributos de texto que se definen en IAccDictionary.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588c827764d17c2576efaa5e3117527e23d1da26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078316"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Apéndice E: atributos de texto para Active Accessibility Diccionario de servicios de texto

Este apéndice proporciona información sobre los atributos de texto que se definen en [**IAccDictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary). Está organizada como una serie de tablas. Cada tabla incluye información acerca de una categoría específica de atributos. Estas categorías están realmente anidadas, pero se separan a continuación para que pueda ver los atributos.

> [!Note]  
> Active Accessibility servicios de texto está en desuso. Consulte [Microsoft Windows Text Services Framework](../tsf/text-services-framework.md) para obtener más información sobre la entrada de texto avanzada y las tecnologías de lenguaje natural.

 

Cada entrada de una tabla proporciona un nombre de atributo y un nombre descriptivo, tipo, Hojas de estilo CSS (CSS) equivalente, modelo de objetos de texto (TOM) equivalente y cualquier comentario adicional cuando sea necesario. La columna TOM Equivalent proporciona información sobre el método TOM que se usa con el atributo (parte de las interfaces [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont), [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)o [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) ). La información anterior a cada tabla indica qué interfaz admite los atributos; la información de la tabla equivalente TOM indica el nombre del método. Cada entrada de la columna TOM Equivalent está asociada a dos métodos. Por ejemplo, la entrada Name está asociada a los métodos **GetName** y **setName** .

Para obtener más información acerca de estas interfaces, vea la documentación del [modelo de objetos de texto](../controls/text-object-model.md) en el kit de desarrollo de software (SDK) de Windows.

## <a name="font"></a>Fuente

Los atributos de la tabla siguiente se asocian a los atributos de fuente generales. El equivalente TOM es la interfaz [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nombre del atributo, nombre descriptivo       | Tipo     | Equivalente de CSS       | TOM equivalente | Comentario           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| Font \_ FaceName, FaceName<br/> | VT \_ BSTR | Font-family: Verdana | Nombre           |                   |
| Font \_ SizePts, SizePts<br/>   | VT \_ I4   | Tamaño de fuente: XPT       | Tamaño           | El tamaño está en puntos |



 

## <a name="font_style"></a>Estilo de fuente \_

Los atributos de la siguiente tabla direccionan los atributos de estilo de fuente (por ejemplo, si el texto se establece en negrita o cursiva). El equivalente TOM es la interfaz [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nombre del atributo, nombre descriptivo                             | Tipo     | Equivalente de CSS              | TOM equivalente                                            | Comentario                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| \_Estilo de fuente en \_ negrita, negrita<br/>                        | VT \_ bool | Font-weight: negrita           | Bold                                                      |                           |
| \_Estilo \_ de fuente cursiva, cursiva<br/>                    | VT \_ bool | Estilo de fuente: cursiva          | Cursiva                                                    |                           |
| \_Estilo \_ de fuente SmallCaps, SmallCaps<br/>              | VT \_ bool | Font-variant: versalitas    | SmallCaps                                                 |                           |
| \_Estilo \_ de fuente mayúsculas, mayúsculas<br/>             | VT \_ bool | Text-Transform: mayúsculas  | No compatible                                             |                           |
| \_Estilo \_ de fuente mayúsculas, mayúsculas<br/>               | VT \_ bool | Texto-transformación: mayúsculas   | AllCaps                                                   |                           |
| \_Estilo de fuente en \_ minúsculas, minúsculas<br/>               | VT \_ bool | Text-Transform: minúsculas   | No compatible                                             |                           |
| \_Estilo \_ de fuente relieve, relieve<br/>                     | VT \_ bool | No compatible               | Emboss                                                    |                           |
| \_Estilo \_ de fuente grabado, grabado<br/>                   | VT \_ bool | No compatible               | Grabado                                                   |                           |
| Estilo de fuente \_ \_ oculto                                       | VT \_ bool | No compatible               | Hidden                                                    |                           |
| \_ \_ Kerning de estilo de fuente, kerning<br/>                   | VT \_ R4   | No compatible               | El interletraje                                                   | Los mismos valores que GetKerning |
| \_Estilo \_ de fuente descrito, descrito<br/>                 | VT \_ bool | No compatible               | Descritos                                                  |                           |
| \_Posición del estilo \_ de fuente, posición<br/>                 | VT \_ R4   | No compatible               | Posición                                                  |                           |
| Estilo de fuente \_ \_ protegido                                    | VT \_ bool | No compatible               | Protegido                                                 |                           |
| \_ \_ Sombra de estilo de fuente, sombra<br/>                     | VT \_ bool | Alto de línea (menos números) | Shadow                                                    |                           |
| \_ \_ Espaciado de estilo de fuente, espaciado<br/>                   | VT \_ R4   | Espaciado entre letras              | Espaciado                                                   | En puntos                 |
| \_ \_ Espesor de estilo de fuente, peso<br/>                     | VT \_ I4   | Espesor de fuente                 | WeightSame valores como font-weight y GetWeight<br/> |                           |
| \_ \_ Alto y alto del estilo de fuente<br/>                     | VT \_ R4   | Line-height                 | No compatible                                             | En puntos                 |
| \_Estilo \_ de fuente parpadeo, parpadeo<br/>                       | VT \_ bool | Texto: decoración: parpadeo      | No compatible                                             |                           |
| \_ \_ Subíndice de estilo de fuente, subíndice<br/>               | VT \_ bool | Vertical-align: sub         | Subíndice (también posición)                                 |                           |
| \_ \_ Superíndice de estilo de fuente, superíndice<br/>           | VT \_ bool | Vertical-align: Super       | Superíndice (también posición)                               |                           |
| \_ \_ Color de estilo de fuente, color<br/>                       | VT \_ I4   | Color                       | ForeColor                                                 | Estilo RBG COLORREF        |
| \_Estilo \_ de fuente BackgroundColor, \_ color de fondo<br/> | VT \_ I4   | Color de fondo            | BackColor                                                 | Estilo RBG COLORREF        |



 

## <a name="font_style_animation"></a>\_Animación de estilo de fuente \_

Los atributos de la siguiente tabla indican la animación de fuentes. El equivalente TOM es la interfaz [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nombre del atributo, nombre descriptivo                                              | Tipo     | Equivalente de CSS | TOM equivalente |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| \_ \_ Animación de estilo \_ de fuente LasVegasLights, LasVegas \_ Lights<br/>         | VT \_ bool | No compatible  | Animación      |
| \_ \_ Animación de estilo \_ de fuente BlinkingBackground, \_ fondo parpadeante<br/> | VT \_ bool | No compatible  | Animación      |
| \_ \_ Animación de estilo \_ de fuente SparkleText, \_ texto de destello<br/>               | VT \_ bool | No compatible  | Animación      |
| \_ \_ Animación de estilo \_ de fuente MarchingBlackAnts, \_ hormigas de marzo \_<br/> | VT \_ bool | No compatible  | Animación      |
| \_ \_ Animación de estilo \_ de fuente MarchingRedAnts, marzo de \_ \_ hormigas rojo<br/>     | VT \_ bool | No compatible  | Animación      |
| \_ \_ Animación de estilo \_ de fuente Shimmer, Shimmer<br/>                         | VT \_ bool | No compatible  | Animación      |
| \_ \_ Animación de estilo \_ de fuente WipeDown, WipeDown<br/>                       | VT \_ bool | No compatible  | Animación      |
| \_ \_ Animación de estilo \_ de fuente WipeRight, WipeRight<br/>                     | VT \_ bool | No compatible  | Animación      |



 

## <a name="font_style_underline"></a>Estilo de fuente \_ \_ subrayado

Los atributos de la siguiente tabla tratan los estilos de subrayado para las fuentes. El equivalente TOM es la interfaz [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nombre del atributo, nombre descriptivo                     | Tipo     | Equivalente de CSS                | TOM equivalente |
|---------------------------------------------------|----------|-------------------------------|----------------|
| \_Estilo \_ de fuente subrayado \_ único, único<br/>  | VT \_ bool | Text-decoration: underline    | Subrayado      |
| \_Estilo \_ de fuente subrayado \_ doble, doble<br/> | VT \_ bool | Text-decoration: línea a través | StrikeThrough  |



 

## <a name="font_style_strikethrough"></a>\_Tachado de estilo de fuente \_

Los atributos de la siguiente tabla direccionan los estilos de tachado para las fuentes.



| Nombre del atributo, nombre descriptivo                                         | Tipo     | Equivalente de CSS | TOM equivalente |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| \_Estilo \_ de fuente tachado \_ único, tachado \_ a través de \_ una sola<br/> | VT \_ bool | No compatible  | No compatible  |
| \_ \_ Tachado \_ de estilo de fuente doble, tachado \_ \_ doble<br/> | VT \_ bool | No compatible  | No compatible  |



 

## <a name="font_style_overline"></a>\_Línea de estilo de fuente \_

Los atributos de la siguiente tabla direccionan los estilos en línea para las fuentes.



| Nombre del atributo, nombre descriptivo                             | Tipo     | Equivalente de CSS            | TOM equivalente |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| \_Estilo \_ de fuente de línea simple lineal, línea \_ \_ única<br/> | VT \_ bool | Text-decoration: línea alta | No compatible  |
| \_Estilo \_ de fuente \_ , doble línea, \_ doble<br/> | VT \_ bool | Text-decoration: línea alta | No compatible  |



 

## <a name="text"></a>Texto

Los atributos de la siguiente tabla tratan los atributos de formato de texto general.



| Nombre del atributo, nombre descriptivo                     | Tipo        | Equivalente de CSS | TOM equivalente                                       | Comentario                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| Texto \_ VerticalWriting, escritura vertical<br/> | VT \_ bool    | No compatible  | no admitido                                        | Tal y como se usa en chino/japonés                                                           |
| Texto \_ RightToLeft, RightToLeft<br/>          | VT \_ bool    | Dirección      | No compatible                                        |                                                                                       |
| \_ReadOnly de texto, solo lectura<br/>               | VT \_ bool    | No compatible  | ITextFont:: CanChange, ITextRange:: CanEdit            | La propiedad editable del documento tiene prioridad                                     |
| \_Idioma de texto, idioma<br/>                | VT \_ I4      | No compatible  | ITextFont::GetLanguageID, ITextFont::SetLanguageID   | IDIDIOMA                                                                                |
| Orientación del texto \_ , orientación<br/>          | VT \_ I4      | No compatible  | No compatible                                        | 10??? de un grado                                                                     |
| \_EmbeddedObject de texto, \_ objeto incrustado<br/>  | VT \_ bool    | No compatible  | No compatible                                        | Permite buscar objetos incrustados                                                 |
| \_Vínculo de texto, vínculo<br/>                        | VT \_ desconocido | Link           | No compatible                                        | Puntero de interfaz al objeto; llamar a QueryInterface para cualquier interfaz de interés |
| \_Guiones de texto, guiones<br/>          | VT \_ bool    | No compatible  | ITextPara::GetHyphenation, ITextPara::SetHyphenation |                                                                                       |



 

## <a name="text_alignment"></a>Alineación del texto \_

Los atributos de la siguiente tabla indican la alineación del texto. El equivalente TOM es la interfaz [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nombre del atributo, nombre descriptivo               | Tipo     | Equivalente de CSS | TOM equivalente |
|---------------------------------------------|----------|----------------|----------------|
| Alineación del texto a la \_ \_ izquierda, izquierda<br/>       | VT \_ bool | Alineación de texto     | Alignment      |
| Alineación de texto a la derecha \_ \_ , derecha<br/>     | VT \_ bool | Alineación de texto     | Alignment      |
| \_ \_ Centro de alineación de texto, centro<br/>   | VT \_ bool | Alineación de texto     | Alignment      |
| \_Justificación de la alineación del texto \_ , justificar<br/> | VT \_ bool | Alineación de texto     | Alignment      |



 

## <a name="text_para"></a>Texto \_ para

Los atributos del siguiente formato de dirección de tabla para los párrafos. El equivalente TOM es la interfaz [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nombre del atributo, nombre descriptivo                              | Tipo   | Equivalente de CSS | TOM equivalente  | Comentario |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| Texto \_ para \_ FirstLineIndent, sangría de primera \_ línea \_<br/> | VT \_ R4 | No compatible  | FirstLineIndent | En PTS  |
| Texto \_ para \_ LeftIndent, \_ sangría izquierda<br/>             | VT \_ R4 | No compatible  | Property      | En PTS  |
| Texto \_ para \_ RightIndent, \_ sangría derecha<br/>           | VT \_ R4 | No compatible  | RightIndent     | En PTS  |
| Texto \_ para \_ SpaceAfter, espacio \_ después de<br/>             | VT \_ R4 | No compatible  | Property      | En PTS  |
| Texto \_ para \_ SpaceBefore, espacio \_ después de<br/>            | VT \_ R4 | No compatible  | Property      | En PTS  |



 

## <a name="text_para_linespacing"></a>Texto \_ para \_ LineSpacing

Los atributos de la tabla siguiente describen el interlineado de las líneas en los párrafos. El equivalente TOM es la interfaz [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nombre del atributo, nombre descriptivo                               | Tipo     | Equivalente de CSS | TOM equivalente | Comentario  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| Texto \_ para \_ LineSpacing \_ Single, single<br/>           | VT \_ bool | No compatible  | LineSpacing    |          |
| Text \_ para \_ LineSpacing \_ OnePtFive, un \_ PT \_ cinco<br/> | VT \_ bool | No compatible  | LineSpacing    |          |
| Texto \_ para \_ LineSpacing \_ Double, Double<br/>           | VT \_ bool | No compatible  | LineSpacing    |          |
| Texto \_ para \_ LineSpacing \_ como mínimo, \_ al menos<br/>       | VT \_ R4   | No compatible  | LineSpacing    | En líneas |
| Texto \_ para \_ LineSpacing \_ exactamente, exactamente<br/>         | VT \_ R4   | No compatible  | LineSpacing    | En líneas |
| Texto \_ para \_ LineSpacing \_ varias, varios<br/>        | VT \_ R4   | No compatible  | LineSpacing    | En líneas |



 

## <a name="text_list"></a>Lista de texto \_

Los atributos de la tabla siguiente enumeran listas y niveles de listas de texto. El equivalente TOM es la interfaz [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nombre del atributo, nombre descriptivo | Tipo   | Equivalente de CSS | TOM equivalente | Comentario                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| \_Lista \_ de texto LevelIndex,       | VT \_ I4 | No compatible  | ListLevelIndex | Donde 1 es la lista más externa, 2 es el nivel siguiente, etc. |



 

## <a name="text_list_type"></a>\_Tipo de lista de texto \_

Los atributos de la tabla siguiente indican los estilos de lista de direcciones para el texto. El equivalente TOM es la interfaz [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nombre del atributo, nombre descriptivo                          | Tipo     | Equivalente de CSS  | TOM equivalente |
|--------------------------------------------------------|----------|-----------------|----------------|
| \_ \_ Tipo de lista \_ de texto viñeta, viñeta<br/>             | VT \_ bool | Tipo de lista       | ListType       |
| \_ \_ Tipo de lista \_ de texto árabe, Árabe<br/>             | VT \_ bool | Tipo de estilo de lista | ListType       |
| \_ \_ Tipo de lista \_ de texto LowerLetter, \_ letra minúscula<br/> | VT \_ bool | Tipo de estilo de lista | ListType       |
| \_ \_ Tipo de lista \_ de texto UpperLetter, \_ letra superior<br/> | VT \_ bool | Tipo de estilo de lista | ListType       |
| \_ \_ Tipo de lista \_ de texto LowerRoman, \_ romano inferior<br/>   | VT \_ bool | Tipo de estilo de lista | ListType       |
| \_Tipo de lista \_ de texto \_ , perro, \_ romano superior<br/>   | VT \_ bool | Tipo de estilo de lista | ListType       |



 

## <a name="app"></a>Aplicación



| Nombre del atributo, nombre descriptivo                         | Tipo     | Equivalente de CSS | TOM equivalente |
|-------------------------------------------------------|----------|----------------|----------------|
| \_IncorrectSpelling de aplicación, \_ ortografía incorrecta<br/> | VT \_ bool |                | No compatible  |
| \_IncorrectGrammar de aplicación, \_ gramática incorrecta<br/>   | VT \_ bool |                | No compatibles  |



 

 

