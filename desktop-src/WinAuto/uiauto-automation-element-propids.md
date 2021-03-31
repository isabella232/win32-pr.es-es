---
title: Identificadores de propiedad de elemento de automatización (UIAutomationClient. h)
description: En este tema se describen las constantes con nombre que identifican las propiedades de los elementos de automatización de la interfaz de usuario de Microsoft.
ms.assetid: f7613ad1-0b75-46fb-b9ac-b1ae9eea4193
topic_type:
- apiref
api_name:
- UIA_AcceleratorKeyPropertyId
- UIA_AccessKeyPropertyId
- UIA_AnnotationObjectsPropertyId
- UIA_AnnotationTypesPropertyId
- UIA_AriaPropertiesPropertyId
- UIA_AriaRolePropertyId
- UIA_AutomationIdPropertyId
- UIA_BoundingRectanglePropertyId
- UIA_CenterPointPropertyId
- UIA_ClassNamePropertyId
- UIA_ClickablePointPropertyId
- UIA_ControllerForPropertyId
- UIA_ControlTypePropertyId
- UIA_CulturePropertyId
- UIA_DescribedByPropertyId
- UIA_FillColorPropertyId
- UIA_FillTypePropertyId
- UIA_FlowsFromPropertyId
- UIA_FlowsToPropertyId
- UIA_FrameworkIdPropertyId
- UIA_FullDescriptionPropertyId
- UIA_HasKeyboardFocusPropertyId
- UIA_HeadingLevelPropertyId
- UIA_HelpTextPropertyId
- UIA_IsContentElementPropertyId
- UIA_IsControlElementPropertyId
- UIA_IsDataValidForFormPropertyId
- UIA_IsEnabledPropertyId
- UIA_IsKeyboardFocusablePropertyId
- UIA_IsOffscreenPropertyId
- UIA_IsPasswordPropertyId
- UIA_IsPeripheralPropertyId
- UIA_IsRequiredForFormPropertyId
- UIA_ItemStatusPropertyId
- UIA_ItemTypePropertyId
- UIA_LabeledByPropertyId
- UIA_LandmarkTypePropertyId
- UIA_LevelPropertyId
- UIA_LiveSettingPropertyId
- UIA_LocalizedControlTypePropertyId
- UIA_LocalizedLandmarkTypePropertyId
- UIA_NamePropertyId
- UIA_NativeWindowHandlePropertyId
- UIA_OptimizeForVisualContentPropertyId
- UIA_OrientationPropertyId
- UIA_OutlineColorPropertyId
- UIA_OutlineThicknessPropertyId
- UIA_PositionInSetPropertyId
- UIA_ProcessIdPropertyId
- UIA_ProviderDescriptionPropertyId
- UIA_RotationPropertyId
- UIA_RuntimeIdPropertyId
- UIA_SizePropertyId
- UIA_SizeOfSetPropertyId
- UIA_VisualEffectsPropertyId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c90b1a6d56fa62b6ddb241ce38c8cb2ae40afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150989"
---
# <a name="automation-element-property-identifiers"></a>Identificadores de propiedad de elemento de automatización

En este tema se describen las constantes con nombre que identifican las propiedades de los elementos de automatización de la interfaz de usuario de Microsoft.



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
<td style="text-align: left;"><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>AcceleratorKey</strong> , que es una cadena que contiene las combinaciones de tecla de aceleración (también llamadas teclas de método abreviado) para el elemento de automatización. <br/> Las combinaciones de teclas de método abreviado invocan una acción. Por ejemplo, CTRL + O a menudo se usa para invocar el cuadro de diálogo Abrir archivo común. Un elemento de automatización que tiene la propiedad <strong>AcceleratorKey</strong> puede implementar el patrón de control <a href="uiauto-implementinginvoke.md">Invoke</a> para la acción equivalente al comando de acceso directo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>accessKey</strong> , que es una cadena que contiene el carácter de tecla de acceso para el elemento de automatización.<br/> Una tecla de acceso (a veces denominada tecla de acceso) es un carácter en el texto de un menú, un elemento de menú o una etiqueta de un control, como un botón, que activa la función de menú asociada. Por ejemplo, para abrir el menú Archivo, para el que la tecla de acceso es normalmente F, el usuario presione ALT + F.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>AnnotationObjects</strong> , que es una lista de objetos Annotation de un documento, como comentario, encabezado, pie de página, etc.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>AnnotationTypes</strong> , que es una lista de los tipos de anotaciones de un documento, como comentario, encabezado, pie de página, etc.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>AriaProperties</strong> , que es una cadena con formato que contiene la información de la propiedad de aplicación de Internet enriquecida (Aria) accesible para el elemento de automatización. Para obtener más información sobre la asignación de Estados y propiedades de ARIA a las propiedades y las funciones de UI Automation, vea <a href="uiauto-ariaspecification.md">UI Automation for World Wide Internet accessible Application</a>.<br/> <strong>AriaProperties</strong> es una colección de pares de nombre/valor con delimitadores de <strong>=</strong> (es igual a) y <strong>;</strong> (punto y coma), por ejemplo, &quot; Checked = true; Disabled = false &quot; . <strong>\</strong>(Barra diagonal inversa) se utiliza como carácter de escape cuando estos caracteres delimitadores o <strong>\</strong> aparecen en los valores. Por motivos de seguridad y otras razones, la implementación del proveedor de esta propiedad puede tomar medidas para validar las propiedades ARIA originales. sin embargo, no es necesario.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>AriaRole</strong> , que es una cadena que contiene la información de rol de aplicación de Internet enriquecida (Aria) accesible para el elemento de automatización. Para obtener más información sobre la asignación de roles de ARIA a tipos de control de automatización de la interfaz de usuario, vea <a href="uiauto-ariaspecification.md">automatización de la interfaz de usuario para aplicaciones de Internet enriquecidas accesibles</a>.<br/>
<blockquote>
[!Note]<br />
Como opción, el agente de usuario también puede proporcionar una descripción localizada del rol ARIA del consorcio W3C en la propiedad <strong>LocalizedControlType</strong> . Cuando no se especifica la cadena localizada, el sistema proporcionará la cadena predeterminada de <strong>LocalizedControlType</strong> para el elemento.
</blockquote>
<br/> <br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>AutomationId</strong> , que es una cadena que contiene el identificador (ID.) de automatización de la interfaz de usuario para el elemento de automatización.<br/> Cuando está disponible, el <strong>AutomationId</strong> de un elemento debe ser el mismo en cualquier instancia de la aplicación, independientemente del idioma local. El valor debe ser único entre los elementos del mismo nivel, pero no necesariamente único en todo el escritorio. Por ejemplo, varias instancias de una aplicación o varias vistas de carpeta en el explorador de Microsoft Windows, pueden contener elementos con la misma propiedad <strong>AutomationId</strong> , como &quot; SystemMenuBar &quot; .<br/> Aunque la compatibilidad con <strong>AutomationId</strong> siempre es recomendable para mejorar la compatibilidad con las pruebas automatizadas, esta propiedad no es obligatoria. Cuando se admite, <strong>AutomationId</strong> es útil para crear un script de automatización de prueba que se ejecuta independientemente del idioma de la interfaz de usuario. Los clientes no deben hacer suposiciones sobre los valores de <strong>AutomationId</strong> expuestos por otras aplicaciones. No se garantiza que <strong>AutomationId</strong> sea estable en las distintas versiones o compilaciones de una aplicación.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>BoundingRectangle</strong> , que especifica las coordenadas del rectángulo que incluye completamente el elemento de automatización. El rectángulo se expresa en coordenadas de pantalla físicas. Puede contener puntos que no son seleccionables si la forma o región en la que se puede hacer clic del elemento de la interfaz de usuario es irregular, o si el elemento está oculto por otros elementos de la interfaz de usuario.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: [0, 0, 0, 0]<br/>
<blockquote>
[!Note]<br />
Esta propiedad es <strong>null</strong> si el elemento no está mostrando actualmente una interfaz de usuario.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>CenterPoint</strong> , que especifica las coordenadas de punto X e y del elemento de automatización. El espacio de coordenadas es lo que el proveedor considera lógicamente una página.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>className</strong> , que es una cadena que contiene el nombre de clase para el elemento Automation asignado por el desarrollador del control.<br/> El nombre de clase depende de la implementación del proveedor de automatización de la interfaz de usuario y, por tanto, no está siempre en un formato estándar. Sin embargo, si se conoce el nombre de clase, se puede usar para comprobar que una aplicación está funcionando con el elemento de automatización esperado.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>ClickablePoint</strong> , que es un punto del elemento de automatización en el que se puede hacer clic. No se puede hacer clic en un elemento si otra ventana lo oculta completamente o parcialmente.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>ControllerFor</strong> , que es una matriz de elementos de automatización manipulada por el elemento de automatización que admite esta propiedad.<br/> <strong>ControllerFor</strong> se usa cuando un elemento de automatización afecta a uno o varios segmentos de la interfaz de usuario de la aplicación o del escritorio. de lo contrario, es difícil asociar el impacto de la operación de control a los elementos de la interfaz de usuario.<br/> Este identificador se usa normalmente para la <a href="/windows/uwp/design/accessibility/accessible-text-requirements">accesibilidad de la sugerencia automática</a>.<br/> Tipo Variant para proveedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo Variant para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a> )<br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>ControlType</strong> , que es una clase que identifica el tipo del elemento de automatización. <strong>ControlType</strong> define características de los elementos de la interfaz de usuario mediante primitivos de control de interfaz de usuario conocidos, como un botón o una casilla. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
Use el valor predeterminado solo si el elemento de automatización representa un tipo de control completamente nuevo.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad de <strong>referencia cultural</strong> , que contiene un identificador de configuración regional para el elemento de automatización (por ejemplo, <code>0x0409</code> para &quot; en-US &quot; o inglés (Estados Unidos)).<br/> Cada configuración regional tiene un identificador único, un valor de 32 bits que consta de un identificador de idioma y un identificador de criterio de ordenación. El identificador de configuración regional es una abreviatura numérica internacional estándar y tiene los componentes necesarios para identificar de forma única una de las configuraciones regionales definidas por el sistema operativo instaladas. Para obtener más información, vea <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">constantes y cadenas de identificador de idioma</a>.<br/> Esta propiedad puede existir en cada control, pero normalmente solo está disponible en un nivel de aplicación.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>DescribedBy</strong> , que es una matriz de elementos que proporcionan más información sobre el elemento de automatización.<br/> <strong>DescribedBy</strong> se utiliza cuando un elemento de automatización lo explica otro segmento de la interfaz de usuario de la aplicación. Por ejemplo, la propiedad puede apuntar a un elemento de texto de &quot; 2.529 elementos en 85 grupos, 10 elementos seleccionados &quot; de un objeto de lista personalizado complejo. En lugar de utilizar el modelo de objetos para que los clientes puedan resumir información similar, la propiedad <strong>DescribedBy</strong> puede ofrecer un acceso rápido al elemento de la interfaz de usuario que ya puede ofrecer información útil del usuario final que describe el elemento de la interfaz de usuario.<br/> Tipo Variant para proveedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo Variant para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>colorderelleno</strong> , que especifica el color utilizado para rellenar el elemento de automatización. Este atributo se especifica como COLORREF, un valor de 32 bits que se usa para especificar un color RGB o RGBA.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>FillType</strong> , que especifica el patrón que se usa para rellenar el elemento de automatización, como ninguno, color, degradado, imagen, patrón, etc.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>FlowsFrom</strong> , que es una matriz de elementos de automatización que sugiere el orden de lectura antes del elemento de automatización actual. Se admite a partir de Windows 8.<br/> La propiedad <strong>FlowsFrom</strong> especifica el orden de lectura cuando los elementos de automatización no se exponen o estructuran en el mismo orden de lectura que percibe el usuario. Aunque la propiedad <strong>FlowsFrom</strong> puede especificar varios elementos anteriores, normalmente solo contiene el elemento anterior en el orden de lectura.<br/> Tipo Variant para proveedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo Variant para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>flowto</strong> , que es una matriz de elementos de automatización que sugiere el orden de lectura después del elemento de automatización actual.<br/> La propiedad <strong>flowas</strong> especifica el orden de lectura cuando los elementos de automatización no se exponen o estructuran en el mismo orden de lectura que percibe el usuario. Mientras que la propiedad <strong>flowto</strong> puede especificar varios elementos que se ejecutan correctamente, normalmente solo contiene el siguiente elemento en el orden de lectura.<br/> Tipo Variant para proveedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo Variant para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>FrameworkId</strong> , que es una cadena que contiene el nombre del marco de interfaz de usuario subyacente al que pertenece el elemento de automatización.<br/> <strong>FrameworkId</strong> permite a las aplicaciones cliente procesar los elementos de automatización de manera diferente en función del marco de trabajo de la interfaz de usuario determinado. Algunos ejemplos de valores de propiedad son &quot; Win32 &quot; , &quot; WinForm &quot; y &quot; DirectUI &quot; .<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td style="text-align: left;">La propiedad <strong>FullDescription</strong> expone una cadena traducida que puede contener texto de descripción extendida para un elemento. <strong>FullDescription</strong> puede contener una descripción más completa de un elemento que puede ser adecuada para el <strong>nombre</strong>del elemento.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>HasKeyboardFocus</strong> , que es un valor booleano que indica si el elemento de automatización tiene el foco de teclado.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>HeadingLevel</strong> , que indica el nivel de encabezado de un elemento de automatización de la interfaz de usuario.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>HelpText</strong> , que es una cadena de texto de ayuda asociada al elemento Automation.<br/> La propiedad <strong>HelpText</strong> puede ser compatible con el texto de marcador de posición que aparece en los controles de edición o de lista. Por ejemplo, &quot; Escriba aquí el texto de &quot; la búsqueda es una buena candidata a la propiedad <strong>HelpText</strong> de un control de edición que coloca el texto antes de la entrada real del usuario. Sin embargo, no es adecuado para la propiedad Name del control de edición.<br/> Cuando se admite <strong>HelpText</strong> , la cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con el idioma predeterminado de la interfaz de usuario del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsContentElement</strong> , que es un valor booleano que especifica si el elemento aparece en la vista de contenido del árbol de elementos de automatización. Para obtener más información, vea <a href="uiauto-treeoverview.md">UI Automation Tree Overview</a>.<br/>
<blockquote>
[!Note]<br />
Para que un elemento aparezca en la vista de contenido, tanto la propiedad <strong>IsContentElement</strong> como la propiedad <strong>IsControlElement</strong> deben ser <strong>true</strong>.
</blockquote>
<br/> <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>true</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsControlElement</strong> , que es un valor booleano que especifica si el elemento aparece en la vista de control del árbol de elementos de automatización. Para obtener más información, vea <a href="uiauto-treeoverview.md">UI Automation Tree Overview</a>.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>true</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsDataValidForForm</strong> , que es un valor booleano que indica si el valor especificado o seleccionado es válido para la regla de formulario asociada al elemento de automatización. Por ejemplo, si el usuario escribió &quot; 425-555-5555 &quot; para un campo de código postal que requiere 5 o 9 dígitos, la propiedad <strong>IsDataValidForForm</strong> se puede establecer en <strong>false</strong> para indicar que los datos no son válidos.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>

<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsDialog</strong> , que es un valor booleano que indica si el elemento de automatización es una ventana de cuadro de diálogo. Por ejemplo, la tecnología de ayuda, como los lectores de pantalla, normalmente hablan el título del cuadro de diálogo, el control centrado en el cuadro de diálogo y, a continuación, el contenido del cuadro de diálogo hasta el control centrado ( &quot; ¿desea guardar los cambios antes de cerrar &quot; ). En el caso de las ventanas estándar, un lector de pantalla normalmente habla el título de la ventana seguido del control con el foco. La propiedad <strong>IsDialog</strong> se puede establecer en <strong>true</strong> para indicar que la aplicación cliente debe tratar el elemento como una ventana de cuadro de diálogo.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>

<tr class="even">
<td style="text-align: left;"><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsEnabled</strong> , que es un valor booleano que indica si el elemento de la interfaz de usuario al que hace referencia el elemento de automatización está habilitado y con el que se puede interactuar.<br/> Cuando el estado habilitado de un control es <strong>false</strong>, se supone que los controles secundarios tampoco están habilitados. Los clientes no deben esperar eventos modificados por propiedad de los elementos secundarios cuando cambia el estado del control primario.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsKeyboardFocusable</strong> , que es un valor booleano que indica si el elemento de automatización puede aceptar el foco de teclado.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsOffscreen</strong> , que es un valor booleano que indica si el elemento de automatización se desplaza totalmente fuera de la vista (por ejemplo, un elemento de un cuadro de lista que está fuera de la ventanilla del objeto contenedor) o se contrae fuera de la vista (por ejemplo, un elemento en una vista de árbol o un menú, o en una ventana minimizada). Si el elemento tiene un punto seleccionable que puede hacer que reciba el foco, se considera que el elemento está en pantalla mientras que una parte del elemento está fuera de la pantalla.<br/> El valor de la propiedad no se ve afectado por otras ventanas, o por si el elemento está visible en un monitor específico.<br/> Si la propiedad <strong>IsOffscreen</strong> es <strong>true</strong>, el elemento de la interfaz de usuario se desplaza fuera de la pantalla o se contrae. El elemento se oculta temporalmente, pero permanece en la percepción del usuario final y continúa estando incluido en el modelo de interfaz de usuario. El objeto se puede devolver a la vista desplazándose, haciendo clic en un menú desplegable, etc.<br/> Los objetos que el usuario final no percibe en absoluto, o que se &quot; ocultan mediante programación &quot; (por ejemplo, un cuadro de diálogo que se ha descartado, pero que el objeto subyacente todavía está almacenado en la memoria caché de la aplicación) no deben estar en el árbol de elementos de automatización en el primer lugar (en lugar de establecer el estado de <strong>IsOffscreen</strong> en <strong>true</strong>).<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsPassword</strong> , que es un valor booleano que indica si el elemento de automatización contiene contenido protegido o una contraseña.<br/> Cuando la propiedad <strong>IsPassword</strong> es <strong>true</strong> y el elemento tiene el foco de teclado, una aplicación cliente debe deshabilitar el eco de teclado o los comentarios de entrada de teclado que pueden exponer la información protegida del usuario. Si se intenta tener acceso a la propiedad <strong>Value</strong> del elemento Protected (control de edición), es posible que se produzca un error.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsPeripheral</strong> , que es un valor booleano que indica si el elemento de automatización representa la interfaz de usuario de periféricos. La interfaz de usuario de periféricos aparece y admite la interacción con el usuario, pero no toma el foco de teclado cuando aparece. Entre los ejemplos de interfaz de usuario de periféricos se incluyen ventanas emergentes, controles flotantes, menús contextuales o notificaciones flotantes. Se admite a partir de Windows 8.1.<br/> Cuando la propiedad <strong>IsPeripheral</strong> es <strong>true</strong>, una aplicación cliente no puede suponer que el foco lo tomó el elemento aunque esté actualmente interactivo mediante el teclado.<br/> Esta propiedad es relevante para estos tipos de control:<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>IsRequiredForForm</strong> , que es un valor booleano que indica si se requiere que el elemento de automatización se rellene en un formulario.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>ItemStatus</strong> , que es una cadena de texto que describe el estado de un elemento del elemento Automation.<br/> <strong>ItemStatus</strong> permite a un cliente averiguar si un elemento está transmitiendo el estado sobre un elemento, así como cuál es el estado. Por ejemplo, un elemento asociado a un contacto en una aplicación de mensajería podría estar &quot; ocupado &quot; o &quot; conectado &quot; .<br/> Cuando se admite <strong>ItemStatus</strong> , la cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con el idioma predeterminado de la interfaz de usuario del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>itemType</strong> , que es una cadena de texto que describe el tipo del elemento de automatización.<br/> <strong>ItemType</strong> se usa para obtener información sobre los elementos de una lista, una vista de árbol o una cuadrícula de datos. Por ejemplo, un elemento de una vista de directorio de archivos puede ser un &quot; archivo de documento &quot; o una &quot; carpeta &quot; .<br/> Cuando se admite <strong>itemType</strong> , la cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con el idioma predeterminado de la interfaz de usuario del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>LabeledBy</strong> , que es un elemento de automatización que contiene la etiqueta de texto para este elemento.<br/> Esta propiedad se puede utilizar para recuperar, por ejemplo, la etiqueta de texto estático de un cuadro combinado.<br/> Tipo de variante: <strong>VT_UNKNOWN</strong><br/> Valor predeterminado: <strong>null</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>LandmarkType</strong> , que es un <a href="landmark-type-identifiers.md"><strong>identificador de tipo</strong></a> de punto de referencia asociado a un elemento.<br/> La propiedad <strong>LandmarkType</strong> describe un elemento que representa un grupo de elementos. Por ejemplo, un punto de referencia de búsqueda podría representar un conjunto de controles relacionados para realizar búsquedas.<br/> Si se utiliza <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> , se requiere <strong>UIA_LocalizedLandmarkTypePropertyId</strong> para describir el punto de referencia personalizado.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad de <strong>nivel</strong> , que es un entero de base 1 asociado a un elemento de automatización.<br/> La propiedad <strong>LEVEL</strong> describe la ubicación de un elemento dentro de estructuras jerárquicas jerárquicas o rotas. Por ejemplo, una lista con viñetas o numerada, los encabezados u otros elementos de datos estructurados pueden tener varias relaciones de elementos primarios y secundarios. <strong>Nivel</strong> describe dónde se encuentra el elemento en la estructura.<br/> Se recomienda usar el patrón de <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">control CustomNavigation</a> en tándem con <strong>LEVEL</strong>.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>LiveSetting</strong> , que es compatible con un elemento de automatización que representa una región activa. La propiedad <strong>LiveSetting</strong> indica el &quot; &quot; nivel de educación que un cliente debe usar para notificar al usuario sobre los cambios en la región activa. Esta propiedad puede ser uno de los valores de la enumeración <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>LiveSetting</strong></a> . Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>LocalizedControlType</strong> , que es una cadena de texto que describe el tipo de control que representa el elemento de automatización. La cadena solo debe contener caracteres en minúsculas:
<ul>
<li>Correcto: &quot; botón&quot;</li>
<li>Incorrecto: &quot; botón&quot;</li>
</ul>
<br/> Cuando el proveedor de elementos no especifica <strong>LocalizedControlType</strong> , el marco de trabajo proporciona la cadena localizada predeterminada, de acuerdo con el tipo de control del elemento (por ejemplo, el &quot; botón &quot; para el tipo de control <a href="uiauto-supportbuttoncontroltype.md">Button</a> ). Un elemento de automatización con el tipo de control <strong>personalizado</strong> debe admitir una cadena de tipo de control localizada que representa el rol del elemento (por ejemplo, &quot; selector &quot; de colores para un control personalizado que permite a los usuarios elegir y especificar colores).<br/> Cuando se proporciona un valor personalizado, la cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con el idioma predeterminado de la interfaz de usuario del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td style="text-align: left;">Identifica <strong>LocalizedLandmarkType</strong>, que es una cadena de texto que describe el tipo de referencia que representa el elemento de automatización.<br/> Se debería usar en conjunto con <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> sin embargo, <strong>LocalizedLandmarkType</strong> siempre debe tener prioridad sobre <strong>LandmarkType</strong> y usarse para describir el punto de referencia antes de <strong>LandmarkType</strong>.<br/> La cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con la interfaz de usuario predeterminada del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>Name</strong> , que es una cadena que contiene el nombre del elemento Automation.<br/> La propiedad <strong>Name</strong> debe ser la misma que el texto de la etiqueta de la pantalla. Por ejemplo, <strong>el nombre</strong> debe &quot; Buscar &quot; un elemento de botón con la etiqueta &quot; Browse &quot; . La propiedad <strong>Name</strong> no debe incluir el carácter de tecla de acceso para las teclas de acceso (es decir, &quot; & &quot; ), que está subrayado en la presentación de texto de la interfaz de usuario. Además, la propiedad <strong>Name</strong> no debe ser una versión extendida o modificada de la etiqueta en pantalla porque la incoherencia entre el nombre y la etiqueta puede causar confusión entre las aplicaciones cliente y los usuarios.<br/> Cuando el texto de la etiqueta correspondiente no está visible en la pantalla o cuando se reemplaza por gráficos, se debe elegir texto alternativo. El texto alternativo debe ser conciso, intuitivo y adaptado al idioma de la interfaz de usuario de la aplicación, o al idioma predeterminado de la interfaz de usuario del sistema operativo. El texto alternativo no debe ser una descripción detallada de los detalles visuales, sino una breve descripción de la función o característica de la interfaz de usuario como si estuviera etiquetada por texto simple. Por ejemplo, el botón menú Inicio de Windows se denomina &quot; Inicio &quot; (botón) en lugar del &quot; logotipo de Windows en gráficos de esfera redonda azul &quot; (botón). Para obtener más información, vea <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">crear equivalentes de texto para imágenes</a>.<br/> Cuando una etiqueta de la interfaz de usuario usa gráficos de texto (por ejemplo, con &quot; >> &quot; para un botón que agrega un elemento de izquierda a derecha), la propiedad de <strong>nombre</strong> debe reemplazarse por una alternativa de texto adecuada (por ejemplo, &quot; agregar &quot; ). Sin embargo, no se recomienda usar gráficos de texto como etiqueta de la interfaz de usuario debido a problemas de localización y accesibilidad.<br/> La propiedad <strong>Name</strong> no debe incluir la información de tipo o la función de control, como &quot; Button &quot; o &quot; List; de &quot; lo contrario, entrará en conflicto con el texto de la propiedad <strong>LocalizedControlType</strong> cuando se anexen estas dos propiedades (muchas de las tecnologías de asistencia existentes lo hacen).<br/> No se puede usar la propiedad <strong>Name</strong> como identificador único entre elementos del mismo nivel. Sin embargo, siempre que sea coherente con la presentación de la interfaz de usuario, se puede admitir el mismo valor de <strong>nombre</strong> entre los elementos del mismo nivel. En la automatización de prueba, los clientes deben considerar el uso de la propiedad <strong>AutomationId</strong> o <strong>RuntimeId</strong> .<br/> Los controles de texto no siempre tienen que tener la propiedad <strong>nombre</strong> igual que el texto que se muestra en el control, siempre que el patrón de <strong>texto</strong> también se admita.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>NativeWindowHandle</strong> , que es un entero que representa el identificador (<strong>hWnd</strong>) de la ventana del elemento de automatización, si existe; de lo contrario, esta propiedad es 0.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>OptimizeForVisualContent</strong> , que es un valor booleano que indica si el proveedor expone solo los elementos que están visibles. Un proveedor puede usar esta propiedad para optimizar el rendimiento cuando se trabaja con fragmentos de contenido muy grandes. Por ejemplo, a medida que el usuario se pagina a través de una gran parte del contenido, el proveedor puede destruir elementos de contenido que ya no están visibles. Cuando se destruye un elemento de contenido, el proveedor debe devolver el código de error <strong>UIA_E_ELEMENTNOTAVAILABLE</strong> . Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>Orientation</strong> , que indica la orientación del control representado por el elemento Automation. La propiedad se expresa como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType</strong></a> .<br/> La propiedad <strong>Orientation</strong> es compatible con los controles, como las barras de desplazamiento y los controles deslizantes, que pueden tener una orientación vertical u horizontal. De lo contrario, siempre puede ser <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>, lo que significa que el control no tiene ninguna orientación.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>)<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>OutlineColor</strong> , que especifica el color utilizado para el contorno del elemento de automatización. Este atributo se especifica como <strong>COLORREF</strong>, un valor de 32 bits que se usa para especificar un color RGB o RGBA.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>OutlineThickness</strong> , que especifica el ancho del contorno del elemento de automatización.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>PositionInSet</strong> , que es un entero de base 1 asociado a un elemento de automatización. <strong>PositionInSet</strong> describe la ubicación ordinal del elemento dentro de un conjunto de elementos que se consideran relacionados.<br/> <strong>PositionInSet</strong> funciona en coordinación con la propiedad <strong>SizeOfSet</strong> para describir la ubicación ordinal en el conjunto.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>ProcessId</strong> , que es un entero que representa el identificador de proceso (ID.) del elemento de automatización.<br/> El sistema operativo asigna el identificador de proceso (ID). Puede verse en la columna <strong>PID</strong> de la pestaña <strong>procesos</strong> del administrador de tareas.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>ProviderDescription</strong> , que es una cadena con formato que contiene la información de origen del proveedor de automatización de la interfaz de usuario para el elemento de automatización, incluida la información de proxy.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>Rotation</strong> , que especifica el ángulo de giro en unidades no especificadas.<br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>RuntimeId</strong> , que es una matriz de enteros que representa el identificador de un elemento de automatización.<br/> El identificador es único en el escritorio, pero se garantiza que es único solo dentro de la interfaz de usuario del escritorio en el que se generó. Los identificadores se pueden reutilizar con el tiempo.<br/> El formato de <strong>RuntimeId</strong> puede cambiar. El identificador devuelto se debe tratar como un valor opaco y usarse solo para la comparación; por ejemplo, para determinar si un elemento de automatización está en la memoria caché.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad de <strong>tamaño</strong> , que especifica el ancho y el alto del elemento de automatización.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>SizeOfSet</strong> , que es un entero de base 1 asociado a un elemento de automatización. <strong>SizeOfSet</strong> describe el número de elementos de automatización de un grupo o conjunto que se consideran relacionados.<br/> <strong>SizeOfSet</strong> funciona en coordinación con la propiedad <strong>PositionInSet</strong> para describir el número de elementos del conjunto.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td style="text-align: left;">Identifica la propiedad <strong>VisualEffects</strong> , que es un campo de bits que especifica los efectos en el elemento de automatización, como sombra, reflexión, resplandor, bordes flexibles o bisel.<br/> VisualEffects:<br/>
<ul>
<li>VisualEffects_Shadow: 0x1</li>
<li>VisualEffects_Reflection: 0X2</li>
<li>VisualEffects_Glow: 0x4</li>
<li>VisualEffects_SoftEdges: 0x8</li>
<li>VisualEffects_Bevel: 0x10</li>
</ul>
Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
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

**Vista**
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md)
</dt> </dl>
