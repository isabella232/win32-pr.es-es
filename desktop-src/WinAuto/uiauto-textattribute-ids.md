---
title: Identificadores de atributo de texto (UIAutomationClient.h)
description: En este tema se describen las constantes con nombre que se usan para identificar los atributos de texto de un intervalo Automatización de la interfaz de usuario texto de Microsoft.
ms.assetid: 67d86817-6a3f-4047-88d9-34f33f52a563
topic_type:
- apiref
api_name:
- UIA_AfterParagraphSpacingAttributeId
- UIA_AnimationStyleAttributeId
- UIA_AnnotationObjectsAttributeId
- UIA_AnnotationTypesAttributeId
- UIA_BackgroundColorAttributeId
- UIA_BeforeParagraphSpacingAttributeId
- UIA_BulletStyleAttributeId
- UIA_CapStyleAttributeId
- UIA_CaretBidiModeAttributeId
- UIA_CaretPositionAttributeId
- UIA_CultureAttributeId
- UIA_FontNameAttributeId
- UIA_FontSizeAttributeId
- UIA_FontWeightAttributeId
- UIA_ForegroundColorAttributeId
- UIA_HorizontalTextAlignmentAttributeId
- UIA_IndentationFirstLineAttributeId
- UIA_IndentationLeadingAttributeId
- UIA_IndentationTrailingAttributeId
- UIA_IsActiveAttributeId
- UIA_IsHiddenAttributeId
- UIA_IsItalicAttributeId
- UIA_IsReadOnlyAttributeId
- UIA_IsSubscriptAttributeId
- UIA_IsSuperscriptAttributeId
- UIA_LineSpacingAttributeId
- UIA_LinkAttributeId
- UIA_MarginBottomAttributeId
- UIA_MarginLeadingAttributeId
- UIA_MarginTopAttributeId
- UIA_MarginTrailingAttributeId
- UIA_OutlineStylesAttributeId
- UIA_OverlineColorAttributeId
- UIA_OverlineStyleAttributeId
- UIA_SelectionActiveEndAttributeId
- UIA_StrikethroughColorAttributeId
- UIA_StrikethroughStyleAttributeId
- UIA_StyleIdAttributeId
- UIA_StyleNameAttributeId
- UIA_TabsAttributeId
- UIA_TextFlowDirectionsAttributeId
- UIA_UnderlineColorAttributeId
- UIA_UnderlineStyleAttributeId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e84ba97b387097233b7a838fbe192585b9676b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465990"
---
# <a name="text-attribute-identifiers"></a>Identificadores de atributo de texto

En este tema se describen las constantes con nombre que se usan para identificar los atributos de texto de un intervalo Automatización de la interfaz de usuario texto de Microsoft. Estas constantes se usan con los métodos siguientes:

-   [**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
-   [**ITextRangeProvider::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
-   [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
-   [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="UIA_AfterParagraphSpacingAttributeId"></span><span id="uia_afterparagraphspacingattributeid"></span><span id="UIA_AFTERPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_AfterParagraphSpacingAttributeId</strong></dt><dt>40042</dt></dl> | Identifica el atributo de texto <strong>AfterParagraphSpacing,</strong> que especifica el tamaño del espaciado después del párrafo.<br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_AnimationStyleAttributeId"></span><span id="uia_animationstyleattributeid"></span><span id="UIA_ANIMATIONSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_AnimationStyleAttributeId</strong></dt><dt>40000</dt></dl> | Identifica el atributo de texto <strong>AnimationStyle,</strong> que especifica el tipo de animación aplicada al texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"><strong>AnimationStyle.</strong></a> <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"> <strong>AnimationStyle_None</strong></a><br /> | 
| <span id="UIA_AnnotationObjectsAttributeId"></span><span id="uia_annotationobjectsattributeid"></span><span id="UIA_ANNOTATIONOBJECTSATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationObjectsAttributeId</strong></dt><dt>40032</dt></dl> | Identifica el atributo de texto <strong>AnnotationObjects,</strong> que mantiene una matriz de interfaces <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2"><strong>IUIAutomationElement2,</strong></a> una para cada elemento del intervalo de texto actual que implementa el patrón de control <a href="uiauto-implementingannotation.md">Annotation.</a> Cada elemento también podría implementar otros patrones de control según sea necesario para describir la anotación. Por ejemplo, una anotación que sea un comentario también admitiría el patrón <a href="uiauto-implementingtextandtextrange.md">de</a> control Texto. Se admite a partir de Windows 8.<br /> Tipo de variante: <strong>VT_UNKNOWN</strong><br /> Valor predeterminado: matriz vacía <br /> | 
| <span id="UIA_AnnotationTypesAttributeId"></span><span id="uia_annotationtypesattributeid"></span><span id="UIA_ANNOTATIONTYPESATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationTypesAttributeId</strong></dt><dt>40031</dt></dl> | Identifica el atributo <strong>de texto AnnotationTypes,</strong> que mantiene una lista de identificadores de tipo de anotación para un intervalo de texto. Para obtener una lista de valores posibles, vea <a href="uiauto-annotation-type-identifiers.md"><strong>Identificadores de tipo de anotación</strong></a>. Se admite a partir de Windows 8.<br /> Tipo de variante: <strong>VT_ARRAY</strong> | <strong>VT_I4</strong><br /> Valor predeterminado: matriz vacía <br /> | 
| <span id="UIA_BackgroundColorAttributeId"></span><span id="uia_backgroundcolorattributeid"></span><span id="UIA_BACKGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_BackgroundColorAttributeId</strong></dt><dt>40001</dt></dl> | Identifica el atributo <strong>de texto BackgroundColor,</strong> que especifica el color de fondo del texto. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF</a>; un valor de 32 bits utilizado para especificar un color RGB o RGBA. <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: 0 <br /> | 
| <span id="UIA_BeforeParagraphSpacingAttributeId"></span><span id="uia_beforeparagraphspacingattributeid"></span><span id="UIA_BEFOREPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_BeforeParagraphSpacingAttributeId</strong></dt><dt>40041</dt></dl> | Identifica el atributo de texto <strong>BeforeParagraphSpacing,</strong> que especifica el tamaño del espaciado antes del párrafo.<br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_BulletStyleAttributeId"></span><span id="uia_bulletstyleattributeid"></span><span id="UIA_BULLETSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_BulletStyleAttributeId</strong></dt><dt>40002</dt></dl> | Identifica el atributo de texto <strong>BulletStyle,</strong> que especifica el estilo de las viñetas usadas en el intervalo de texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"><strong>BulletStyle.</strong></a><br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"> <strong>BulletStyle_None</strong></a><br /> | 
| <span id="UIA_CapStyleAttributeId"></span><span id="uia_capstyleattributeid"></span><span id="UIA_CAPSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_CapStyleAttributeId</strong></dt><dt>40003</dt></dl> | Identifica el atributo <strong>de texto CapStyle,</strong> que especifica el estilo de mayúsculas para el texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"><strong>CapStyle.</strong></a> <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"> <strong>CapStyle_None</strong></a><br /> | 
| <span id="UIA_CaretBidiModeAttributeId"></span><span id="uia_caretbidimodeattributeid"></span><span id="UIA_CARETBIDIMODEATTRIBUTEID"></span><dl><dt><strong>UIA_CaretBidiModeAttributeId</strong></dt><dt>40039</dt></dl> | Identifica el atributo <strong>de texto CaretBidiMode,</strong> que indica la dirección del flujo de texto en el intervalo de texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"><strong>CaretBidiMode.</strong></a> Se admite a partir de Windows 8.<br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"> <strong>CaretBidiMode_LTR</strong></a><br /> | 
| <span id="UIA_CaretPositionAttributeId"></span><span id="uia_caretpositionattributeid"></span><span id="UIA_CARETPOSITIONATTRIBUTEID"></span><dl><dt><strong>UIA_CaretPositionAttributeId</strong></dt><dt>40038</dt></dl> | Identifica el <strong>atributo de texto CaretPosition,</strong> que indica si el elemento de referencia está al principio o al final de una línea de texto en el intervalo de texto. Este atributo se especifica como un valor del <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"><strong>tipo enumerado CaretPosition.</strong></a> Se admite a partir de Windows 8.<br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"> <strong>CaretPosition_Unknown</strong></a><br /> | 
| <span id="UIA_CultureAttributeId"></span><span id="uia_cultureattributeid"></span><span id="UIA_CULTUREATTRIBUTEID"></span><dl><dt><strong>UIA_CultureAttributeId</strong></dt><dt>40004</dt></dl> | Identifica el atributo de texto <strong>Culture,</strong> que especifica la configuración regional del texto por identificador de configuración regional (LCID). <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: configuración regional de la interfaz de usuario de la aplicación<br /> | 
| <span id="UIA_FontNameAttributeId"></span><span id="uia_fontnameattributeid"></span><span id="UIA_FONTNAMEATTRIBUTEID"></span><dl><dt><strong>UIA_FontNameAttributeId</strong></dt><dt>40005</dt></dl> | Identifica el atributo <strong>de texto FontName,</strong> que especifica el nombre de la fuente. Ejemplos: "Arial Black"; "Arial Narrow". La cadena de nombre de fuente no está localizada. <br /> Tipo de variante: <strong>VT_BSTR</strong><br /> Valor predeterminado: cadena vacía<br /> | 
| <span id="UIA_FontSizeAttributeId"></span><span id="uia_fontsizeattributeid"></span><span id="UIA_FONTSIZEATTRIBUTEID"></span><dl><dt><strong>UIA_FontSizeAttributeId</strong></dt><dt>40006</dt></dl> | Identifica el atributo <strong>de texto FontSize,</strong> que especifica el tamaño de punto de la fuente. <br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_FontWeightAttributeId"></span><span id="uia_fontweightattributeid"></span><span id="UIA_FONTWEIGHTATTRIBUTEID"></span><dl><dt><strong>UIA_FontWeightAttributeId</strong></dt><dt>40007</dt></dl> | Identifica el atributo <strong>de texto FontWeight,</strong> que especifica el trazo relativo, grosor o negrita de la fuente. El <strong>atributo FontWeight</strong> se modela después del miembro <strong>lfWeight</strong> de la estructura <a href="/windows/win32/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> de GDI y los estándares relacionados, y puede ser uno de los valores siguientes:<ul><li>0 = <strong>DontCare</strong></li><li>100 = <strong>Fino</strong></li><li>200 = <strong>ExtraLight</strong> o <strong>UltraLight</strong></li><li>300 = <strong>Claro</strong></li><li>400 = <strong>Normal</strong> o <strong>Normal</strong></li><li>500 = <strong>Medio</strong></li><li>600 = <strong>SemiBold</strong></li><li>700 = <strong>Negrita</strong></li><li>800 = <strong>ExtraBold</strong> <strong>o UltraBold</strong></li><li>900 = <strong>Heavy</strong> o <strong>Black</strong></li></ul><br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_ForegroundColorAttributeId"></span><span id="uia_foregroundcolorattributeid"></span><span id="UIA_FOREGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_ForegroundColorAttributeId</strong></dt><dt>40008</dt></dl> | Identifica el atributo <strong>de texto ForegroundColor,</strong> que especifica el color de primer plano del texto. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valor de 32 bits que se usa para especificar un color RGB o RGBA. <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_HorizontalTextAlignmentAttributeId"></span><span id="uia_horizontaltextalignmentattributeid"></span><span id="UIA_HORIZONTALTEXTALIGNMENTATTRIBUTEID"></span><dl><dt><strong>UIA_HorizontalTextAlignmentAttributeId</strong></dt><dt>40009</dt></dl> | Identifica el <strong>atributo de texto HorizontalTextAlignment,</strong> que especifica cómo se alinea horizontalmente el texto. Este atributo se especifica como un valor del tipo enumerado <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"><strong>HorizontalTextAlignmentEnum.</strong></a> <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"> <strong>HorizontalTextAlignment_Left</strong></a><br /> | 
| <span id="UIA_IndentationFirstLineAttributeId"></span><span id="uia_indentationfirstlineattributeid"></span><span id="UIA_INDENTATIONFIRSTLINEATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationFirstLineAttributeId</strong></dt><dt>40010</dt></dl> | Identifica el atributo de texto <strong>IndentationFirstLine,</strong> que especifica hasta qué punto, en puntos, se aplica sangría a la primera línea de un párrafo. <br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_IndentationLeadingAttributeId"></span><span id="uia_indentationleadingattributeid"></span><span id="UIA_INDENTATIONLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationLeadingAttributeId</strong></dt><dt>40011</dt></dl> | Identifica el atributo <strong>de texto IndentationLeading,</strong> que especifica la sangría inicial, en puntos. <br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_IndentationTrailingAttributeId"></span><span id="uia_indentationtrailingattributeid"></span><span id="UIA_INDENTATIONTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationTrailingAttributeId</strong></dt><dt>40012</dt></dl> | Identifica el atributo <strong>de texto IndentationTrailing,</strong> que especifica la sangría final, en puntos. <br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_IsActiveAttributeId"></span><span id="uia_isactiveattributeid"></span><span id="UIA_ISACTIVEATTRIBUTEID"></span><dl><dt><strong>UIA_IsActiveAttributeId</strong></dt><dt>40036</dt></dl> | Identifica el atributo de texto <strong>IsActive,</strong> que indica si el control que contiene el intervalo de texto tiene el foco del teclado (<strong>TRUE</strong>) o no (<strong>FALSE</strong>). Se admite a partir de Windows 8.<br /> Tipo de variante: <strong>VT_BOOL</strong><br /> Valor predeterminado: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsHiddenAttributeId"></span><span id="uia_ishiddenattributeid"></span><span id="UIA_ISHIDDENATTRIBUTEID"></span><dl><dt><strong>UIA_IsHiddenAttributeId</strong></dt><dt>40013</dt></dl> | Identifica el <strong>atributo de texto IsHidden,</strong> que indica si el texto está oculto<strong>(TRUE</strong>) o visible<strong>(FALSE).</strong> <br /> Tipo de variante: <strong>VT_BOOL</strong><br /> Valor predeterminado: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsItalicAttributeId"></span><span id="uia_isitalicattributeid"></span><span id="UIA_ISITALICATTRIBUTEID"></span><dl><dt><strong>UIA_IsItalicAttributeId</strong></dt><dt>40014</dt></dl> | Identifica el <strong>atributo de texto IsItalic,</strong> que indica si el texto está en cursiva (<strong>TRUE</strong>) o no (<strong>FALSE</strong>). <br /> Tipo de variante: <strong>VT_BOOL</strong><br /> Valor predeterminado: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsReadOnlyAttributeId"></span><span id="uia_isreadonlyattributeid"></span><span id="UIA_ISREADONLYATTRIBUTEID"></span><dl><dt><strong>UIA_IsReadOnlyAttributeId</strong></dt><dt>40015</dt></dl> | Identifica el atributo de texto <strong>IsReadOnly,</strong> que indica si el texto es de solo lectura (<strong>TRUE</strong>) o se puede modificar (<strong>FALSE</strong>). <br /> Tipo de variante: <strong>VT_BOOL</strong><br /> Valor predeterminado: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsSubscriptAttributeId"></span><span id="uia_issubscriptattributeid"></span><span id="UIA_ISSUBSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSubscriptAttributeId</strong></dt><dt>40016</dt></dl> | Identifica el <strong>atributo de texto IsSubscript,</strong> que indica si el texto es subíndice (<strong>TRUE</strong>) o no (<strong>FALSE</strong>). <br /> Tipo de variante: <strong>VT_BOOL</strong><br /> Valor predeterminado: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsSuperscriptAttributeId"></span><span id="uia_issuperscriptattributeid"></span><span id="UIA_ISSUPERSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSuperscriptAttributeId</strong></dt><dt>40017</dt></dl> | Identifica el <strong>atributo de texto IsSuperscript,</strong> que indica si el texto es subíndice (<strong>TRUE</strong>) o no (<strong>FALSE</strong>). <br /> Tipo de variante: <strong>VT_BOOL</strong><br /> Valor predeterminado: <strong>FALSE</strong><br /> | 
| <span id="UIA_LineSpacingAttributeId"></span><span id="uia_linespacingattributeid"></span><span id="UIA_LINESPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_LineSpacingAttributeId</strong></dt><dt>40040</dt></dl> | Identifica el atributo <strong>de texto LineSpacing,</strong> que especifica el espaciado entre líneas de texto.<br /> Tipo de variante: <strong>VT_BSTR</strong><br /> Valor predeterminado: "LineSpacingAttributeDefault"<br /> | 
| <span id="UIA_LinkAttributeId"></span><span id="uia_linkattributeid"></span><span id="UIA_LINKATTRIBUTEID"></span><dl><dt><strong>UIA_LinkAttributeId</strong></dt><dt>40035</dt></dl> | Identifica el atributo de texto <strong>Link,</strong> que contiene la interfaz <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange"><strong>IUIAutomationTextRange</strong></a> del intervalo de texto que es el destino de un vínculo interno en un documento. Se admite a partir de Windows 8.<br /> Tipo de variante: <strong>VT_UNKNOWN</strong><br /> Valor predeterminado: <strong>NULL</strong><br /> | 
| <span id="UIA_MarginBottomAttributeId"></span><span id="uia_marginbottomattributeid"></span><span id="UIA_MARGINBOTTOMATTRIBUTEID"></span><dl><dt><strong>UIA_MarginBottomAttributeId</strong></dt><dt>40018</dt></dl> | Identifica el atributo <strong>de texto MarginBottom,</strong> que especifica el tamaño, en puntos, del margen inferior aplicado a la página asociada al intervalo de texto. <br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_MarginLeadingAttributeId"></span><span id="uia_marginleadingattributeid"></span><span id="UIA_MARGINLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginLeadingAttributeId</strong></dt><dt>40019</dt></dl> | Identifica el atributo de texto <strong>MarginLeading,</strong> que especifica el tamaño, en puntos, del margen inicial aplicado a la página asociada al intervalo de texto. <br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_MarginTopAttributeId"></span><span id="uia_margintopattributeid"></span><span id="UIA_MARGINTOPATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTopAttributeId</strong></dt><dt>40020</dt></dl> | Identifica el <strong>atributo de texto MarginTop,</strong> que especifica el tamaño, en puntos, del margen superior aplicado a la página asociada al intervalo de texto. <br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_MarginTrailingAttributeId"></span><span id="uia_margintrailingattributeid"></span><span id="UIA_MARGINTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTrailingAttributeId</strong></dt><dt>40021</dt></dl> | Identifica el <strong>atributo de texto MarginTrailing,</strong> que especifica el tamaño, en puntos, del margen final aplicado a la página asociada al intervalo de texto. <br /> Tipo de variante: <strong>VT_R8</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_OutlineStylesAttributeId"></span><span id="uia_outlinestylesattributeid"></span><span id="UIA_OUTLINESTYLESATTRIBUTEID"></span><dl><dt><strong>UIA_OutlineStylesAttributeId</strong></dt><dt>40022</dt></dl> | Identifica el atributo de texto <strong>OutlineStyles,</strong> que especifica el estilo de esquema del texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"><strong>OutlineStyles.</strong></a> <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"> <strong>OutlineStyles_None</strong></a><br /> | 
| <span id="UIA_OverlineColorAttributeId"></span><span id="uia_overlinecolorattributeid"></span><span id="UIA_OVERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineColorAttributeId</strong></dt><dt>40023</dt></dl> | Identifica el atributo <strong>de texto OverlineColor,</strong> que especifica el color de la decoración de texto sobre línea. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF,</a>un valor de 32 bits que se usa para especificar un color RGB o RGBA. <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_OverlineStyleAttributeId"></span><span id="uia_overlinestyleattributeid"></span><span id="UIA_OVERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineStyleAttributeId</strong></dt><dt>40024</dt></dl> | Identifica el atributo <strong>de texto OverlineStyle,</strong> que especifica el estilo de la decoración de texto sobre línea. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum.</strong></a> <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_SelectionActiveEndAttributeId"></span><span id="uia_selectionactiveendattributeid"></span><span id="UIA_SELECTIONACTIVEENDATTRIBUTEID"></span><dl><dt><strong>UIA_SelectionActiveEndAttributeId</strong></dt><dt>40037</dt></dl> | Identifica el atributo de texto <strong>SelectionActiveEnd,</strong> que indica la ubicación del carácter de diálogo en relación con un intervalo de texto que representa el texto seleccionado actualmente. Este atributo se especifica como un valor de la <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"><strong>enumeración ActiveEnd.</strong></a> Se admite a partir de Windows 8.<br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"> <strong>ActiveEnd_None</strong></a><br /> | 
| <span id="UIA_StrikethroughColorAttributeId"></span><span id="uia_strikethroughcolorattributeid"></span><span id="UIA_STRIKETHROUGHCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughColorAttributeId</strong></dt><dt>40025</dt></dl> | Identifica el atributo <strong>de texto StrikethroughColor,</strong> que especifica el color de la decoración de texto tachado. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF,</a>un valor de 32 bits que se usa para especificar un color RGB o RGBA. <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_StrikethroughStyleAttributeId"></span><span id="uia_strikethroughstyleattributeid"></span><span id="UIA_STRIKETHROUGHSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughStyleAttributeId</strong></dt><dt>40026</dt></dl> | Identifica el atributo de texto <strong>StrikethroughStyle,</strong> que especifica el estilo de la decoración de texto tachado. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum.</strong></a> <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_StyleIdAttributeId"></span><span id="uia_styleidattributeid"></span><span id="UIA_STYLEIDATTRIBUTEID"></span><dl><dt><strong>UIA_StyleIdAttributeId</strong></dt><dt>40034</dt></dl> | Identifica el atributo <strong>de texto StyleId,</strong> que indica los estilos de texto en uso para un intervalo de texto. Para obtener una lista de valores <a href="uiauto-style-identifiers.md"><strong>posibles,</strong></a>vea Identificadores de estilo . Se admite a partir de Windows 8.<br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: 0 <br /> | 
| <span id="UIA_StyleNameAttributeId"></span><span id="uia_stylenameattributeid"></span><span id="UIA_STYLENAMEATTRIBUTEID"></span><dl><dt><strong>UIA_StyleNameAttributeId</strong></dt><dt>40033</dt></dl> | Identifica el atributo <strong>de texto StyleName,</strong> que identifica el nombre localizado del estilo de texto en uso para un intervalo de texto. Se admite a partir de Windows 8.<br /> Tipo de variante: <strong>VT_BSTR</strong><br /> Valor predeterminado: cadena vacía<br /> | 
| <span id="UIA_TabsAttributeId"></span><span id="uia_tabsattributeid"></span><span id="UIA_TABSATTRIBUTEID"></span><dl><dt><strong>UIA_TabsAttributeId</strong></dt><dt>40027</dt></dl> | Identifica el atributo <strong>de texto Tabs,</strong> que es una matriz que especifica las tabulaciones para el intervalo de texto. Cada elemento de matriz especifica una distancia, en puntos, del margen inicial. <br /> Tipo de variante: <strong> VT_ARRAY | VT_R8</strong><br /> Valor predeterminado: matriz vacía<br /> | 
| <span id="UIA_TextFlowDirectionsAttributeId"></span><span id="uia_textflowdirectionsattributeid"></span><span id="UIA_TEXTFLOWDIRECTIONSATTRIBUTEID"></span><dl><dt><strong>UIA_TextFlowDirectionsAttributeId</strong></dt><dt>40028</dt></dl> | Identifica el atributo de texto <strong>TextFlowDirections,</strong> que especifica la dirección del flujo de texto. Este atributo se especifica como una combinación de valores del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"><strong>FlowDirections.</strong></a> <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"> <strong>FlowDirections_Default</strong></a><br /> | 
| <span id="UIA_UnderlineColorAttributeId"></span><span id="uia_underlinecolorattributeid"></span><span id="UIA_UNDERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineColorAttributeId</strong></dt><dt>40029</dt></dl> | Identifica el atributo <strong>de texto UnderlineColor,</strong> que especifica el color de la decoración de texto subrayado. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valor de 32 bits que se usa para especificar un color RGB o RGBA. <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: 0<br /> | 
| <span id="UIA_UnderlineStyleAttributeId"></span><span id="uia_underlinestyleattributeid"></span><span id="UIA_UNDERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineStyleAttributeId</strong></dt><dt>40030</dt></dl> | Identifica el atributo <strong>de texto UnderlineStyle,</strong> que especifica el estilo de la decoración de texto subrayado. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum.</strong></a> <br /> Tipo de variante: <strong>VT_I4</strong><br /> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones \[ de escritorio XP para aplicaciones para \| UWP\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2003 \[ \| aplicaciones para UWP\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>UIAutomationClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
</dt> <dt>

[**ITextRangeProvider::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
</dt> <dt>

[**IUIAutomation::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
</dt> <dt>

[**IUIAutomation::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>
