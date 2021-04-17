---
title: Identificadores de atributos de texto (UIAutomationClient. h)
description: En este tema se describen las constantes con nombre que se usan para identificar atributos de texto de un intervalo de texto de automatización de la interfaz de usuario de Microsoft.
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
ms.openlocfilehash: 9b81c1829c36501b7c0ba4f3862dd9617acfea9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422247"
---
# <a name="text-attribute-identifiers"></a>Identificadores de atributos de texto

En este tema se describen las constantes con nombre que se usan para identificar atributos de texto de un intervalo de texto de automatización de la interfaz de usuario de Microsoft. Estas constantes se utilizan con los métodos siguientes:

-   [**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
-   [**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
-   [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
-   [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AfterParagraphSpacingAttributeId"></span><span id="uia_afterparagraphspacingattributeid"></span><span id="UIA_AFTERPARAGRAPHSPACINGATTRIBUTEID"></span><dl> <dt><strong>UIA_AfterParagraphSpacingAttributeId</strong></dt> <dt>40042</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>AfterParagraphSpacing</strong> , que especifica el tamaño del espaciado después del párrafo.<br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnimationStyleAttributeId"></span><span id="uia_animationstyleattributeid"></span><span id="UIA_ANIMATIONSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_AnimationStyleAttributeId</strong></dt> <dt>40000</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>AnimationStyle</strong> , que especifica el tipo de animación que se aplica al texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"><strong>AnimationStyle</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"> <strong>AnimationStyle_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AnnotationObjectsAttributeId"></span><span id="uia_annotationobjectsattributeid"></span><span id="UIA_ANNOTATIONOBJECTSATTRIBUTEID"></span><dl> <dt><strong>UIA_AnnotationObjectsAttributeId</strong></dt> <dt>40032</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>AnnotationObjects</strong> , que mantiene una matriz de interfaces <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2"><strong>IUIAutomationElement2</strong></a> , una por cada elemento del intervalo de texto actual que implementa el patrón de control <a href="uiauto-implementingannotation.md">Annotation</a> . Cada elemento también puede implementar otros patrones de control según sea necesario para describir la anotación. Por ejemplo, una anotación que es un comentario también admitiría el patrón de control <a href="uiauto-implementingtextandtextrange.md">Text</a> . Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_UNKNOWN</strong><br/> Valor predeterminado: matriz vacía <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnnotationTypesAttributeId"></span><span id="uia_annotationtypesattributeid"></span><span id="UIA_ANNOTATIONTYPESATTRIBUTEID"></span><dl> <dt><strong>UIA_AnnotationTypesAttributeId</strong></dt> <dt>40031</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>AnnotationTypes</strong> , que mantiene una lista de identificadores de tipo de anotación para un intervalo de texto. Para obtener una lista de los valores posibles, vea <a href="uiauto-annotation-type-identifiers.md"><strong>identificadores de tipo de anotación</strong></a>. Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_ARRAY</strong>  |  <strong>VT_I4</strong><br/> Valor predeterminado: matriz vacía <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_BackgroundColorAttributeId"></span><span id="uia_backgroundcolorattributeid"></span><span id="UIA_BACKGROUNDCOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_BackgroundColorAttributeId</strong></dt> <dt>40001</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>BackgroundColor</strong> , que especifica el color de fondo del texto. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF</a>; valor de 32 bits que se usa para especificar un color RGB o RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_BeforeParagraphSpacingAttributeId"></span><span id="uia_beforeparagraphspacingattributeid"></span><span id="UIA_BEFOREPARAGRAPHSPACINGATTRIBUTEID"></span><dl> <dt><strong>UIA_BeforeParagraphSpacingAttributeId</strong></dt> <dt>40041</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>BeforeParagraphSpacing</strong> , que especifica el tamaño del espaciado antes del párrafo.<br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_BulletStyleAttributeId"></span><span id="uia_bulletstyleattributeid"></span><span id="UIA_BULLETSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_BulletStyleAttributeId</strong></dt> <dt>40002</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>BulletStyle</strong> , que especifica el estilo de las viñetas usadas en el intervalo de texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"><strong>BulletStyle</strong></a> .<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"> <strong>BulletStyle_None</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CapStyleAttributeId"></span><span id="uia_capstyleattributeid"></span><span id="UIA_CAPSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_CapStyleAttributeId</strong></dt> <dt>40003</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>CapStyle</strong> , que especifica el estilo de capitalización del texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"><strong>CapStyle</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"> <strong>CapStyle_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CaretBidiModeAttributeId"></span><span id="uia_caretbidimodeattributeid"></span><span id="UIA_CARETBIDIMODEATTRIBUTEID"></span><dl> <dt><strong>UIA_CaretBidiModeAttributeId</strong></dt> <dt>40039</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>CaretBidiMode</strong> , que indica la dirección del flujo de texto en el intervalo de texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"><strong>CaretBidiMode</strong></a> . Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"> <strong>CaretBidiMode_LTR</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CaretPositionAttributeId"></span><span id="uia_caretpositionattributeid"></span><span id="UIA_CARETPOSITIONATTRIBUTEID"></span><dl> <dt><strong>UIA_CaretPositionAttributeId</strong></dt> <dt>40038</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>CaretPosition</strong> , que indica si el símbolo de intercalación está al principio o al final de una línea de texto en el intervalo de texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"><strong>CaretPosition</strong></a> . Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"> <strong>CaretPosition_Unknown</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CultureAttributeId"></span><span id="uia_cultureattributeid"></span><span id="UIA_CULTUREATTRIBUTEID"></span><dl> <dt><strong>UIA_CultureAttributeId</strong></dt> <dt>40004</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto de <strong>referencia cultural</strong> , que especifica la configuración regional del texto mediante el identificador de configuración regional (LCID). <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: configuración regional de la interfaz de usuario de la aplicación<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FontNameAttributeId"></span><span id="uia_fontnameattributeid"></span><span id="UIA_FONTNAMEATTRIBUTEID"></span><dl> <dt><strong>UIA_FontNameAttributeId</strong></dt> <dt>40005</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>FontName</strong> , que especifica el nombre de la fuente. Ejemplos: &quot; Arial Black &quot; ; &quot; Arial Narrow &quot; . La cadena del nombre de fuente no está localizada. <br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FontSizeAttributeId"></span><span id="uia_fontsizeattributeid"></span><span id="UIA_FONTSIZEATTRIBUTEID"></span><dl> <dt><strong>UIA_FontSizeAttributeId</strong></dt> <dt>40006</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>FontSize</strong> , que especifica el tamaño de punto de la fuente. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FontWeightAttributeId"></span><span id="uia_fontweightattributeid"></span><span id="UIA_FONTWEIGHTATTRIBUTEID"></span><dl> <dt><strong>UIA_FontWeightAttributeId</strong></dt> <dt>40007</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>FontWeight</strong> , que especifica el trazo relativo, el grosor o el tipo de negrita de la fuente. El atributo <strong>FontWeight</strong> se modela después del miembro <strong>lfWeight</strong> de la estructura de <a href="/windows/win32/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> de GDI y de los estándares relacionados, y puede tener uno de los valores siguientes:
<ul>
<li>0 = <strong>DontCare</strong></li>
<li>100 = <strong>fino</strong></li>
<li>200 = <strong>extralight</strong> o <strong>Ultralight</strong></li>
<li>300 = <strong>claro</strong></li>
<li>400 = <strong>normal</strong> o <strong>normal</strong></li>
<li>500 = <strong>medio</strong></li>
<li>600 = <strong>seminegrita</strong></li>
<li>700 = <strong>negrita</strong></li>
<li>800 = <strong>ExtraBold</strong> o <strong>ultrabold</strong></li>
<li>900 = <strong>pesado</strong> o <strong>negro</strong></li>
</ul>
<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ForegroundColorAttributeId"></span><span id="uia_foregroundcolorattributeid"></span><span id="UIA_FOREGROUNDCOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_ForegroundColorAttributeId</strong></dt> <dt>40008</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>foregroundcolor</strong> , que especifica el color de primer plano del texto. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valor de 32 bits que se usa para especificar un color RGB o RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HorizontalTextAlignmentAttributeId"></span><span id="uia_horizontaltextalignmentattributeid"></span><span id="UIA_HORIZONTALTEXTALIGNMENTATTRIBUTEID"></span><dl> <dt><strong>UIA_HorizontalTextAlignmentAttributeId</strong></dt> <dt>40009</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>HorizontalTextAlignment</strong> , que especifica cómo se alinea el texto horizontalmente. Este atributo se especifica como un valor del tipo enumerado <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"><strong>HorizontalTextAlignmentEnum</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"> <strong>HorizontalTextAlignment_Left</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IndentationFirstLineAttributeId"></span><span id="uia_indentationfirstlineattributeid"></span><span id="UIA_INDENTATIONFIRSTLINEATTRIBUTEID"></span><dl> <dt><strong>UIA_IndentationFirstLineAttributeId</strong></dt> <dt>40010</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>IndentationFirstLine</strong> , que especifica hasta qué punto, en puntos, va a aplicar sangría a la primera línea de un párrafo. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IndentationLeadingAttributeId"></span><span id="uia_indentationleadingattributeid"></span><span id="UIA_INDENTATIONLEADINGATTRIBUTEID"></span><dl> <dt><strong>UIA_IndentationLeadingAttributeId</strong></dt> <dt>40011</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>IndentationLeading</strong> , que especifica la sangría inicial, en puntos. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IndentationTrailingAttributeId"></span><span id="uia_indentationtrailingattributeid"></span><span id="UIA_INDENTATIONTRAILINGATTRIBUTEID"></span><dl> <dt><strong>UIA_IndentationTrailingAttributeId</strong></dt> <dt>40012</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>IndentationTrailing</strong> , que especifica la sangría final, en puntos. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsActiveAttributeId"></span><span id="uia_isactiveattributeid"></span><span id="UIA_ISACTIVEATTRIBUTEID"></span><dl> <dt><strong>UIA_IsActiveAttributeId</strong></dt> <dt>40036</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>isActive</strong> , que indica si el control que contiene el intervalo de texto tiene el foco de teclado (<strong>true</strong>) o no (<strong>false</strong>). Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsHiddenAttributeId"></span><span id="uia_ishiddenattributeid"></span><span id="UIA_ISHIDDENATTRIBUTEID"></span><dl> <dt><strong>UIA_IsHiddenAttributeId</strong></dt> <dt>40013</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>IsHidden</strong> , que indica si el texto está oculto (<strong>true</strong>) o visible (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsItalicAttributeId"></span><span id="uia_isitalicattributeid"></span><span id="UIA_ISITALICATTRIBUTEID"></span><dl> <dt><strong>UIA_IsItalicAttributeId</strong></dt> <dt>40014</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>IsItalic</strong> , que indica si el texto está en cursiva (<strong>true</strong>) o no (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsReadOnlyAttributeId"></span><span id="uia_isreadonlyattributeid"></span><span id="UIA_ISREADONLYATTRIBUTEID"></span><dl> <dt><strong>UIA_IsReadOnlyAttributeId</strong></dt> <dt>40015</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>IsReadOnly</strong> , que indica si el texto es de solo lectura (<strong>true</strong>) o si se puede modificar (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsSubscriptAttributeId"></span><span id="uia_issubscriptattributeid"></span><span id="UIA_ISSUBSCRIPTATTRIBUTEID"></span><dl> <dt><strong>UIA_IsSubscriptAttributeId</strong></dt> <dt>40016</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>IsSubscript</strong> , que indica si el texto es un subíndice (<strong>true</strong>) o no (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsSuperscriptAttributeId"></span><span id="uia_issuperscriptattributeid"></span><span id="UIA_ISSUPERSCRIPTATTRIBUTEID"></span><dl> <dt><strong>UIA_IsSuperscriptAttributeId</strong></dt> <dt>40017</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>IsSuperscript</strong> , que indica si el texto es un subíndice (<strong>true</strong>) o no (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LineSpacingAttributeId"></span><span id="uia_linespacingattributeid"></span><span id="UIA_LINESPACINGATTRIBUTEID"></span><dl> <dt><strong>UIA_LineSpacingAttributeId</strong></dt> <dt>40040</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>LineSpacing</strong> , que especifica el espaciado entre las líneas de texto.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: &quot; LineSpacingAttributeDefault&quot;<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LinkAttributeId"></span><span id="uia_linkattributeid"></span><span id="UIA_LINKATTRIBUTEID"></span><dl> <dt><strong>UIA_LinkAttributeId</strong></dt> <dt>40035</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto del <strong>vínculo</strong> , que contiene la interfaz <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange"><strong>IUIAutomationTextRange</strong></a> del intervalo de texto que es el destino de un vínculo interno de un documento. Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_UNKNOWN</strong><br/> Valor predeterminado: <strong>null</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_MarginBottomAttributeId"></span><span id="uia_marginbottomattributeid"></span><span id="UIA_MARGINBOTTOMATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginBottomAttributeId</strong></dt> <dt>40018</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>MarginBottom</strong> , que especifica el tamaño, en puntos, del margen inferior aplicado a la página asociada al intervalo de texto. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_MarginLeadingAttributeId"></span><span id="uia_marginleadingattributeid"></span><span id="UIA_MARGINLEADINGATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginLeadingAttributeId</strong></dt> <dt>40019</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>MarginLeading</strong> , que especifica el tamaño, en puntos, del margen inicial aplicado a la página asociada al intervalo de texto. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_MarginTopAttributeId"></span><span id="uia_margintopattributeid"></span><span id="UIA_MARGINTOPATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginTopAttributeId</strong></dt> <dt>40020</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo <strong>marginTop</strong> Text, que especifica el tamaño, en puntos, del margen superior aplicado a la página asociada al intervalo de texto. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor de Ddefault: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_MarginTrailingAttributeId"></span><span id="uia_margintrailingattributeid"></span><span id="UIA_MARGINTRAILINGATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginTrailingAttributeId</strong></dt> <dt>40021</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>MarginTrailing</strong> , que especifica el tamaño, en puntos, del margen final aplicado a la página asociada al intervalo de texto. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OutlineStylesAttributeId"></span><span id="uia_outlinestylesattributeid"></span><span id="UIA_OUTLINESTYLESATTRIBUTEID"></span><dl> <dt><strong>UIA_OutlineStylesAttributeId</strong></dt> <dt>40022</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>OutlineStyles</strong> , que especifica el estilo de contorno del texto. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"><strong>OutlineStyles</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"> <strong>OutlineStyles_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OverlineColorAttributeId"></span><span id="uia_overlinecolorattributeid"></span><span id="UIA_OVERLINECOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_OverlineColorAttributeId</strong></dt> <dt>40023</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>OverlineColor</strong> , que especifica el color de la decoración de texto en línea. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valor de 32 bits que se usa para especificar un color RGB o RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OverlineStyleAttributeId"></span><span id="uia_overlinestyleattributeid"></span><span id="UIA_OVERLINESTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_OverlineStyleAttributeId</strong></dt> <dt>40024</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>OverlineStyle</strong> , que especifica el estilo de la decoración de texto en línea. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_SelectionActiveEndAttributeId"></span><span id="uia_selectionactiveendattributeid"></span><span id="UIA_SELECTIONACTIVEENDATTRIBUTEID"></span><dl> <dt><strong>UIA_SelectionActiveEndAttributeId</strong></dt> <dt>40037</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>SelectionActiveEnd</strong> , que indica la ubicación del símbolo de intercalación con respecto a un intervalo de texto que representa el texto seleccionado actualmente. Este atributo se especifica como un valor de la enumeración <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"><strong>ActiveEnd</strong></a> . Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"> <strong>ActiveEnd_None</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_StrikethroughColorAttributeId"></span><span id="uia_strikethroughcolorattributeid"></span><span id="UIA_STRIKETHROUGHCOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_StrikethroughColorAttributeId</strong></dt> <dt>40025</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>StrikethroughColor</strong> , que especifica el color de la decoración de texto tachado. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valor de 32 bits que se usa para especificar un color RGB o RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_StrikethroughStyleAttributeId"></span><span id="uia_strikethroughstyleattributeid"></span><span id="UIA_STRIKETHROUGHSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_StrikethroughStyleAttributeId</strong></dt> <dt>40026</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>StrikethroughStyle</strong> , que especifica el estilo de la decoración de texto tachado. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_StyleIdAttributeId"></span><span id="uia_styleidattributeid"></span><span id="UIA_STYLEIDATTRIBUTEID"></span><dl> <dt><strong>UIA_StyleIdAttributeId</strong></dt> <dt>40034</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>StyleId</strong> , que indica los estilos de texto que se usan para un intervalo de texto. Para obtener una lista de los valores posibles, vea <a href="uiauto-style-identifiers.md"><strong>identificadores de estilo</strong></a>. Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0 <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_StyleNameAttributeId"></span><span id="uia_stylenameattributeid"></span><span id="UIA_STYLENAMEATTRIBUTEID"></span><dl> <dt><strong>UIA_StyleNameAttributeId</strong></dt> <dt>40033</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto de <strong>StyleName</strong> , que identifica el nombre localizado del estilo de texto que se usa para un intervalo de texto. Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_TabsAttributeId"></span><span id="uia_tabsattributeid"></span><span id="UIA_TABSATTRIBUTEID"></span><dl> <dt><strong>UIA_TabsAttributeId</strong></dt> <dt>40027</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>Tabs</strong> , que es una matriz que especifica las tabulaciones del intervalo de texto. Cada elemento de la matriz especifica una distancia, en puntos, desde el margen inicial. <br/> Tipo de variante: <strong>VT_ARRAY | VT_R8</strong><br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_TextFlowDirectionsAttributeId"></span><span id="uia_textflowdirectionsattributeid"></span><span id="UIA_TEXTFLOWDIRECTIONSATTRIBUTEID"></span><dl> <dt><strong>UIA_TextFlowDirectionsAttributeId</strong></dt> <dt>40028</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>TextFlowDirections</strong> , que especifica la dirección del flujo de texto. Este atributo se especifica como una combinación de valores del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"><strong>FlowDirections</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"> <strong>FlowDirections_Default</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_UnderlineColorAttributeId"></span><span id="uia_underlinecolorattributeid"></span><span id="UIA_UNDERLINECOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_UnderlineColorAttributeId</strong></dt> <dt>40029</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>UnderlineColor</strong> , que especifica el color de la decoración de texto de subrayado. Este atributo se especifica como <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valor de 32 bits que se usa para especificar un color RGB o RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_UnderlineStyleAttributeId"></span><span id="uia_underlinestyleattributeid"></span><span id="UIA_UNDERLINESTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_UnderlineStyleAttributeId</strong></dt> <dt>40030</dt> </dl></td>
<td style="text-align: left;">Identifica el atributo de texto <strong>UnderlineStyle</strong> , que especifica el estilo de la decoración de texto de subrayado. Este atributo se especifica como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
</dt> <dt>

[**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
</dt> <dt>

[**IUIAutomation::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
</dt> <dt>

[**IUIAutomation:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)
</dt> <dt>

**Vista**
</dt> <dt>

[Compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>
