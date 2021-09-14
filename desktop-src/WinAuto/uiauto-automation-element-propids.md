---
title: Identificadores de propiedad de elementos de Automation (UIAutomationClient.h)
description: En este tema se describen las constantes con nombre que identifican las propiedades de microsoft Automatización de la interfaz de usuario elementos.
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
ms.openlocfilehash: b373091ec34e71afbac32fca962ec380513acfcd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070574"
---
# <a name="automation-element-property-identifiers"></a>Identificadores de propiedad de elementos de Automation

En este tema se describen las constantes con nombre que identifican las propiedades de microsoft Automatización de la interfaz de usuario elementos.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Constante o valor</th>
<th >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td >Identifica la propiedad <strong>AcceleratorKey,</strong> que es una cadena que contiene las combinaciones de teclas de aceleración (también denominadas teclas de método abreviado) para el elemento de automatización. <br/> Las combinaciones de teclas de método abreviado invocan una acción. Por ejemplo, CTRL+O se usa a menudo para invocar el cuadro de diálogo Abrir archivo común. Un elemento de automatización que tiene la <strong>propiedad AcceleratorKey</strong> puede implementar el patrón de control <a href="uiauto-implementinginvoke.md">Invoke</a> para la acción equivalente al comando de acceso directo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td >Identifica la propiedad <strong>AccessKey,</strong> que es una cadena que contiene el carácter de clave de acceso para el elemento de automatización.<br/> Una clave de acceso (a veces denominada mnemotécnica) es un carácter en el texto de un menú, elemento de menú o etiqueta de un control como un botón, que activa la función de menú asociada. Por ejemplo, para abrir el menú Archivo, para el que la tecla de acceso suele ser F, el usuario presionaría ALT+F.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td >Identifica la propiedad <strong>AnnotationObjects,</strong> que es una lista de objetos de anotación de un documento, como comentario, encabezado, pie de página, entre otros.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td >Identifica la <strong>propiedad AnnotationTypes,</strong> que es una lista de los tipos de anotaciones de un documento, como comentario, encabezado, pie de página, entre otros.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td >Identifica la <strong>propiedad AriaProperties,</strong> que es una cadena con formato que contiene la información de la propiedad Aplicación de Internet enriquecida accesible (ARIA) para el elemento de automatización. Para obtener más información sobre cómo asignar estados y propiedades de ARIA a Automatización de la interfaz de usuario propiedades y funciones, vea Automatización de la interfaz de usuario <a href="uiauto-ariaspecification.md">para W3C Accessible Rich Internet Applications Specification</a>.<br/> <strong>AriaProperties</strong> es una colección de pares nombre-valor con delimitadores de <strong>=</strong> (equals) y <strong>;</strong> (punto y coma), por ejemplo, &quot; checked=true;disabled=false. &quot; La (barra diagonal inversa) se usa como carácter de escape cuando estos caracteres delimitadores <strong>\</strong> o aparecen en los <strong>\</strong> valores. Por motivos de seguridad y otros motivos, la implementación del proveedor de esta propiedad puede tomar medidas para validar las propiedades originales de ARIA. sin embargo, no es necesario.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td >Identifica la <strong>propiedad AriaRole,</strong> que es una cadena que contiene la información del rol Aplicación de Internet enriqueciendo accesible (ARIA) para el elemento de automatización. Para obtener más información sobre cómo asignar roles de ARIA Automatización de la interfaz de usuario tipos de control, vea Automatización de la interfaz de usuario para la especificación de aplicaciones de Internet enriquecidas accesibles para <a href="uiauto-ariaspecification.md">W3C.</a><br/>
<blockquote>
[!Note]<br />
Como opción, el agente de usuario también puede ofrecer una descripción localizada del rol ARIA de W3C en la <strong>propiedad LocalizedControlType.</strong> Cuando no se especifica la cadena localizada, el sistema proporcionará la cadena <strong>LocalizedControlType</strong> predeterminada para el elemento.
</blockquote>
<br/> <br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td >Identifica la <strong>propiedad AutomationId,</strong> que es una cadena que contiene el identificador Automatización de la interfaz de usuario identificador (ID) del elemento de automatización.<br/> Cuando está disponible, el <strong>AutomationId</strong> de un elemento debe ser el mismo en cualquier instancia de la aplicación, independientemente del idioma local. El valor debe ser único entre los elementos del mismo nivel, pero no necesariamente único en todo el escritorio. Por ejemplo, varias instancias de una aplicación o varias vistas de carpeta en Microsoft Windows Explorer pueden contener elementos con la misma <strong>propiedad AutomationId,</strong> como &quot; SystemMenuBar &quot; .<br/> Aunque siempre se recomienda la <strong>compatibilidad con AutomationId</strong> para una mejor compatibilidad con pruebas automatizadas, esta propiedad no es obligatoria. Donde se admite, <strong>AutomationId</strong> es útil para crear un script de automatización de pruebas que se ejecuta independientemente del lenguaje de interfaz de usuario. Los clientes no deben realizar suposiciones con respecto a los <strong>valores automationId</strong> expuestos por otras aplicaciones. <strong>No se garantiza</strong> que AutomationId sea estable en diferentes versiones o compilaciones de una aplicación.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td >Identifica la <strong>propiedad BoundingRectangle,</strong> que especifica las coordenadas del rectángulo que incluye completamente el elemento de automatización. El rectángulo se expresa en coordenadas de pantalla física. Puede contener puntos en los que no se puede hacer clic si la forma o la región en la que se puede hacer clic del elemento de la interfaz de usuario es irregular, o si el elemento está oculto por otros elementos de la interfaz de usuario.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: [0,0,0,0]<br/>
<blockquote>
[!Note]<br />
Esta propiedad es <strong>NULL si</strong> el elemento no muestra actualmente una interfaz de usuario.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td >Identifica la propiedad <strong>CenterPoint,</strong> que especifica las coordenadas de punto X e Y centrales del elemento de automatización. El espacio de coordenadas es lo que el proveedor considera lógicamente una página.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td >Identifica la propiedad <strong>ClassName,</strong> que es una cadena que contiene el nombre de clase del elemento de automatización asignado por el desarrollador del control.<br/> El nombre de clase depende de la implementación del Automatización de la interfaz de usuario y, por tanto, no siempre está en un formato estándar. Sin embargo, si se conoce el nombre de clase, se puede usar para comprobar que una aplicación está trabajando con el elemento de automatización esperado.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td >Identifica la propiedad <strong>ClickablePoint,</strong> que es un punto del elemento de automatización en el que se puede hacer clic. No se puede hacer clic en un elemento si otra ventana lo oculta completamente o parcialmente.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td >Identifica la <strong>propiedad ControllerFor,</strong> que es una matriz de elementos de automatización manipulados por el elemento de automatización que admite esta propiedad.<br/> <strong>ControllerFor</strong> se usa cuando un elemento de automatización afecta a uno o varios segmentos de la interfaz de usuario de la aplicación o del escritorio; De lo contrario, es difícil asociar el impacto de la operación de control a los elementos de la interfaz de usuario.<br/> Este identificador se usa normalmente para la <a href="/windows/uwp/design/accessibility/accessible-text-requirements">accesibilidad de sugerencia automática.</a><br/> Tipo de variante para proveedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo variante para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a> )<br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td >Identifica la <strong>propiedad ControlType,</strong> que es una clase que identifica el tipo del elemento de automatización. <strong>ControlType define</strong> las características de los elementos de la interfaz de usuario mediante primitivas de control de interfaz de usuario conocidas, como botones o casillas. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
Use el valor predeterminado solo si el elemento de automatización representa un tipo de control completamente nuevo.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td >Identifica la propiedad <strong>Culture,</strong> que contiene un identificador de configuración regional para el elemento de automatización (por ejemplo, <code>0x0409</code> para en-US o inglés &quot; &quot; (Estados Unidos)).<br/> Cada configuración regional tiene un identificador único, un valor de 32 bits que consta de un identificador de idioma y un identificador de criterio de ordenación. El identificador de configuración regional es una abreviatura numérica internacional estándar y tiene los componentes necesarios para identificar de forma única una de las configuraciones regionales definidas por el sistema operativo instalado. Para obtener más información, vea <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Language Identifier Constants and Strings</a>.<br/> Esta propiedad puede existir por control, pero normalmente solo está disponible en el nivel de aplicación.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td >Identifica la <strong>propiedad DescribedBy,</strong> que es una matriz de elementos que proporcionan más información sobre el elemento de automatización.<br/> <strong>DescribedBy</strong> se usa cuando otro segmento de la interfaz de usuario de la aplicación explica un elemento de automatización. Por ejemplo, la propiedad puede apuntar a un elemento de texto de &quot; 2529 elementos en 85 grupos, 10 elementos seleccionados de un objeto de &quot; lista personalizado complejo. En lugar de usar el modelo de objetos para que los clientes describan información similar, la propiedad <strong>DescribedBy</strong> puede ofrecer acceso rápido al elemento de interfaz de usuario que ya puede ofrecer información útil para el usuario final que describe el elemento de la interfaz de usuario.<br/> Tipo de variante para proveedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo variante para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td >Identifica la <strong>propiedad FillColor,</strong> que especifica el color utilizado para rellenar el elemento de automatización. Este atributo se especifica como COLORREF, un valor de 32 bits que se usa para especificar un color RGB o RGBA.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td >Identifica la <strong>propiedad FillType,</strong> que especifica el patrón utilizado para rellenar el elemento de automatización, como ninguno, color, degradado, imagen, patrón, y así sucesivamente.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td >Identifica la propiedad <strong>FlowsFrom,</strong> que es una matriz de elementos de automatización que sugiere el orden de lectura antes del elemento de automatización actual. Se admite a partir de Windows 8.<br/> La <strong>propiedad FlowsFrom</strong> especifica el orden de lectura cuando los elementos de automatización no se exponen ni estructuran en el mismo orden de lectura que el usuario percibe. Aunque la <strong>propiedad FlowsFrom</strong> puede especificar varios elementos anteriores, normalmente solo contiene el elemento anterior en el orden de lectura.<br/> Tipo de variante para proveedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo variante para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td >Identifica la propiedad <strong>FlowsTo,</strong> que es una matriz de elementos de automatización que sugiere el orden de lectura después del elemento de automatización actual.<br/> La <strong>propiedad FlowsTo</strong> especifica el orden de lectura cuando los elementos de automatización no se exponen ni estructuran en el mismo orden de lectura que el usuario percibe. Aunque la <strong>propiedad FlowsTo</strong> puede especificar varios elementos siguientes, normalmente solo contiene el siguiente elemento en el orden de lectura.<br/> Tipo de variante para proveedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo variante para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valor predeterminado: matriz vacía<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td >Identifica la propiedad <strong>FrameworkId,</strong> que es una cadena que contiene el nombre del marco de interfaz de usuario subyacente al que pertenece el elemento de automatización.<br/> <strong>FrameworkId permite que</strong> las aplicaciones cliente procese los elementos de automatización de forma diferente en función del marco de trabajo de interfaz de usuario determinado. Algunos ejemplos de valores de propiedad &quot; son Win32, &quot; &quot; WinForm &quot; y &quot; &quot; DirectUI.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td >La <strong>propiedad FullDescription</strong> expone una cadena localizada que puede contener texto de descripción extendido para un elemento. <strong>FullDescription</strong> puede contener una descripción más completa de un elemento que puede ser adecuada para el elemento <strong>Name</strong>.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td >Identifica la <strong>propiedad HasKeyboardFocus,</strong> que es un valor booleano que indica si el elemento de automatización tiene el foco del teclado.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td >Identifica la <strong>propiedad HeadingLevel,</strong> que indica el nivel de encabezado de un elemento Automatización de la interfaz de usuario encabezado.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td >Identifica la propiedad <strong>HelpText,</strong> que es una cadena de texto de ayuda asociada al elemento de automatización.<br/> La <strong>propiedad HelpText</strong> puede ser compatible con el texto de marcador de posición que aparece en los controles de edición o lista. Por ejemplo, Escriba texto aquí para la búsqueda es un buen candidato a la propiedad HelpText para un control de edición que coloca el texto antes de la entrada &quot; &quot; real del usuario. <strong></strong> Sin embargo, no es adecuado para la propiedad name del control de edición.<br/> Cuando <strong>se admite HelpText,</strong> la cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con el idioma predeterminado de la interfaz de usuario del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td >Identifica la <strong>propiedad IsContentElement,</strong> que es un valor booleano que especifica si el elemento aparece en la vista de contenido del árbol de elementos de automatización. Para obtener más información, <a href="uiauto-treeoverview.md">vea información general Automatización de la interfaz de usuario árbol de archivos</a>.<br/>
<blockquote>
[!Note]<br />
Para que un elemento aparezca en la vista de contenido, tanto la propiedad <strong>IsContentElement</strong> como la <strong>propiedad IsControlElement</strong> deben ser <strong>TRUE.</strong>
</blockquote>
<br/> <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>TRUE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td >Identifica la <strong>propiedad IsControlElement,</strong> que es un valor booleano que especifica si el elemento aparece en la vista de control del árbol de elementos de automatización. Para obtener más información, <a href="uiauto-treeoverview.md">vea información general Automatización de la interfaz de usuario árbol de archivos</a>.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>TRUE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td >Identifica la <strong>propiedad IsDataValidForForm,</strong> que es un valor booleano que indica si el valor especificado o seleccionado es válido para la regla de formulario asociada al elemento de automatización. Por ejemplo, si el usuario escribió &quot; 425-555-5555 para un campo de código postal que requiere 5 o 9 dígitos, la propiedad &quot; <strong>IsDataValidForForm</strong> se puede establecer en <strong>FALSE</strong> para indicar que los datos no son válidos.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>

<tr class="odd">
<td ><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td >Identifica la <strong>propiedad IsDialog,</strong> que es un valor booleano que indica si el elemento de automatización es una ventana de diálogo. Por ejemplo, la tecnología de asistencia, como los lectores de pantalla, suele decir el título del diálogo, el control centrado en el diálogo y, a continuación, el contenido del diálogo hasta el control centrado ( ¿Desea guardar los cambios antes de cerrar &quot; &quot; ). Para las ventanas estándar, un lector de pantalla suele hablar el título de la ventana seguido del control enfocado. La <strong>propiedad IsDialog</strong> se puede establecer en <strong>TRUE para</strong> indicar que la aplicación cliente debe tratar el elemento como una ventana de diálogo.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>

<tr class="even">
<td ><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td >Identifica la <strong>propiedad IsEnabled,</strong> que es un valor booleano que indica si el elemento de interfaz de usuario al que hace referencia el elemento de automatización está habilitado y se puede interactuar con él.<br/> Cuando el estado habilitado de un control <strong>es FALSE,</strong>se supone que los controles secundarios tampoco están habilitados. Los clientes no deben esperar eventos modificados por propiedades de los elementos secundarios cuando cambia el estado del control primario.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td >Identifica la <strong>propiedad IsKeyboardFocusable,</strong> que es un valor booleano que indica si el elemento de automatización puede aceptar el foco del teclado.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td >Identifica la propiedad <strong>IsOffscreen,</strong> que es un valor booleano que indica si el elemento de automatización se desplaza completamente fuera de la vista (por ejemplo, un elemento de un cuadro de lista que está fuera de la ventanilla del objeto contenedor) o se contrae fuera de la vista (por ejemplo, un elemento de una vista de árbol o un menú, o en una ventana minimizada). Si el elemento tiene un punto en el que se puede hacer clic que puede hacer que reciba el foco, se considera que el elemento está en pantalla mientras una parte del elemento está fuera de la pantalla.<br/> El valor de la propiedad no se ve afectado por la oclusión por otras ventanas o por si el elemento está visible en un monitor específico.<br/> Si la <strong>propiedad IsOffscreen</strong> es <strong>TRUE,</strong>el elemento de interfaz de usuario se desplaza fuera de la pantalla o se contrae. El elemento está oculto temporalmente, pero permanece en la percepción del usuario final y continúa incluyéndolo en el modelo de interfaz de usuario. El objeto se puede volver a ver si se desplaza, hace clic en una lista desplegable, y así sucesivamente.<br/> Los objetos que el usuario final no percibe en absoluto o que están ocultos mediante programación (por ejemplo, un cuadro de diálogo que se ha descartado, pero la aplicación todavía almacena en caché el objeto subyacente) no deben estar en el árbol de elementos de automatización en primer lugar (en lugar de establecer el estado de &quot; &quot; <strong>IsOffscreen</strong> en <strong>TRUE).</strong><br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td >Identifica la <strong>propiedad IsPassword,</strong> que es un valor booleano que indica si el elemento de automatización contiene contenido protegido o una contraseña.<br/> Cuando la <strong>propiedad IsPassword</strong> es <strong>TRUE</strong> y el elemento tiene el foco de teclado, una aplicación cliente debe deshabilitar el eco del teclado o los comentarios de entrada de teclado que puedan exponer la información protegida del usuario. Si intenta obtener acceso a <strong>la propiedad Value</strong> del elemento protegido (control de edición), puede producirse un error.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td >Identifica la <strong>propiedad IsPeripheral,</strong> que es un valor booleano que indica si el elemento de automatización representa la interfaz de usuario periférico. La interfaz de usuario periférico aparece y admite la interacción del usuario, pero no se centra en el teclado cuando aparece. Entre los ejemplos de interfaz de usuario periférico se incluyen elementos emergentes, controles flotantes, menús contextuales o notificaciones flotantes. Se admite a partir de Windows 8.1.<br/> Cuando la <strong>propiedad IsPeripheral</strong> es <strong>TRUE,</strong>una aplicación cliente no puede suponer que el elemento ha tomado el foco incluso si actualmente es interactivo con el teclado.<br/> Esta propiedad es relevante para estos tipos de control:<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td >Identifica la <strong>propiedad IsRequiredForForm,</strong> que es un valor booleano que indica si es necesario rellenar el elemento de automatización en un formulario.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td >Identifica la <strong>propiedad ItemStatus,</strong> que es una cadena de texto que describe el estado de un elemento del elemento de automatización.<br/> <strong>ItemStatus</strong> permite a un cliente determinar si un elemento transmite el estado de un elemento, así como cuál es el estado. Por ejemplo, un elemento asociado a un contacto en una aplicación de mensajería podría ser &quot; Ocupado &quot; o &quot; &quot; Conectado.<br/> Cuando <strong>se admite ItemStatus,</strong> la cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con el idioma predeterminado de la interfaz de usuario del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td >Identifica la <strong>propiedad ItemType,</strong> que es una cadena de texto que describe el tipo del elemento de automatización.<br/> <strong>ItemType</strong> se usa para obtener información sobre los elementos de una lista, vista de árbol o cuadrícula de datos. Por ejemplo, un elemento de una vista de directorio de archivos podría ser un archivo &quot; de documento o una carpeta &quot; &quot; &quot; .<br/> Cuando <strong>se admite ItemType,</strong> la cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con el idioma predeterminado de la interfaz de usuario del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td >Identifica la <strong>propiedad LabeledBy,</strong> que es un elemento de automatización que contiene la etiqueta de texto para este elemento.<br/> Esta propiedad se puede usar para recuperar, por ejemplo, la etiqueta de texto estático para un cuadro combinado.<br/> Tipo de variante: <strong>VT_UNKNOWN</strong><br/> Valor predeterminado: <strong>NULL</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td >Identifica la propiedad <strong>LandmarkType,</strong> que es un <a href="landmark-type-identifiers.md"><strong>identificador de tipo de punto de referencia</strong></a> asociado a un elemento.<br/> La <strong>propiedad LandmarkType</strong> describe un elemento que representa un grupo de elementos. Por ejemplo, un punto de referencia de búsqueda podría representar un conjunto de controles relacionados para la búsqueda.<br/> Si <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> se usa , <strong>UIA_LocalizedLandmarkTypePropertyId</strong> para describir el punto de referencia personalizado.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td >Identifica la <strong>propiedad Level,</strong> que es un entero basado en 1 asociado a un elemento de automatización.<br/> La <strong>propiedad Level</strong> describe la ubicación de un elemento dentro de estructuras jerárquicas jerárquicas o rotas. Por ejemplo, una lista con viñetas o numeradas, encabezados u otros elementos de datos estructurados puede tener varias relaciones de elementos primarios y secundarios. <strong>Level</strong> describe dónde se encuentra el elemento en la estructura .<br/> Se recomienda usar el patrón <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">de control CustomNavigation</a> junto con <strong>el nivel</strong>.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td >Identifica la <strong>propiedad LiveSetting,</strong> que es compatible con un elemento de automatización que representa una región en directo. La <strong>propiedad LiveSetting</strong> indica el nivel de integridad que debe usar un cliente para notificar al usuario los cambios &quot; en la región en &quot; directo. Esta propiedad puede ser uno de los valores de la <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>enumeración LiveSetting.</strong></a> Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td >Identifica la propiedad <strong>LocalizedControlType,</strong> que es una cadena de texto que describe el tipo de control que representa el elemento de automatización. La cadena solo debe contener caracteres en minúsculas:
<ul>
<li>Correcto: &quot; botón&quot;</li>
<li>Incorrecto: &quot; Botón&quot;</li>
</ul>
<br/> Cuando el proveedor de elementos no especifica <strong>LocalizedControlType,</strong> el marco proporciona la cadena localizada predeterminada, según el tipo de control del elemento (por ejemplo, el botón para el tipo de &quot; &quot; control <a href="uiauto-supportbuttoncontroltype.md">Button).</a> Un elemento de automatización con el <strong>tipo</strong> de control Personalizado debe admitir una cadena de tipo de control localizado que represente el rol del elemento (por ejemplo, el selector de colores para un control personalizado que permita a los usuarios elegir y especificar &quot; &quot; colores).<br/> Cuando se proporciona un valor personalizado, la cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con el idioma predeterminado de la interfaz de usuario del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td >Identifica <strong>localizedLandmarkType</strong>, que es una cadena de texto que describe el tipo de punto de referencia que representa el elemento de automatización.<br/> Esto debe usarse junto con <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> sin embargo, <strong>LocalizedLandmarkType</strong> siempre debe tener prioridad sobre <strong>LandmarkType</strong> y usarse para describir el punto de referencia antes <strong>de LandmarkType</strong>.<br/> La cadena debe coincidir con el idioma de la interfaz de usuario de la aplicación o con el idioma predeterminado de la interfaz de usuario del sistema operativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td >Identifica la <strong>propiedad Name,</strong> que es una cadena que contiene el nombre del elemento de automatización.<br/> La <strong>propiedad Nombre</strong> debe ser la misma que el texto de la etiqueta en pantalla. Por ejemplo, <strong>Name debe</strong> ser &quot; Browse para un elemento de botón con la etiqueta &quot; Browse &quot; &quot; . La <strong>propiedad Name</strong> no debe incluir el carácter mnemónico para las claves de acceso (es decir, ), que se subraya en la presentación de texto de la interfaz de &quot; & &quot; usuario. Además, la propiedad <strong>Name</strong> no debe ser una versión extendida o modificada de la etiqueta en pantalla porque la incoherencia entre el nombre y la etiqueta puede causar confusión entre las aplicaciones cliente y los usuarios.<br/> Cuando el texto de etiqueta correspondiente no está visible en la pantalla o cuando se reemplaza por gráficos, se debe elegir texto alternativo. El texto alternativo debe ser conciso, intuitivo y traducirse al idioma de la interfaz de usuario de la aplicación o al idioma predeterminado de la interfaz de usuario del sistema operativo. El texto alternativo no debe ser una descripción detallada de los detalles visuales, sino una descripción concisa de la función o característica de la interfaz de usuario como si estuviera etiquetada por texto simple. Por ejemplo, el botón Windows menú Inicio se denomina Inicio (botón) en lugar de Windows logotipo en gráficos de &quot; &quot; &quot; esferas redondeada &quot; azules (botón). Para obtener más información, vea <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">Crear equivalentes de texto para imágenes.</a><br/> Cuando una etiqueta de interfaz de usuario usa gráficos de texto (por ejemplo, mediante para un botón que agrega un elemento de izquierda a derecha), la propiedad Name debe reemplazarse por una alternativa de texto adecuada &quot; >> &quot; (por ejemplo, Agregar <strong></strong> &quot; &quot; ). Sin embargo, no se recomienda usar gráficos de texto como etiqueta de interfaz de usuario debido a problemas de localización y accesibilidad.<br/> La propiedad <strong>Name</strong> no debe incluir el rol de control ni la información de tipo, como botón o lista; de lo contrario, entra en conflicto con el texto de la propiedad &quot; &quot; &quot; &quot; <strong>LocalizedControlType</strong> cuando se anexan estas dos propiedades (muchas tecnologías de asistencia existentes lo hacen).<br/> La <strong>propiedad Name</strong> no se puede usar como identificador único entre los elementos del mismo nivel. Sin embargo, siempre que sea coherente con <strong></strong> la presentación de la interfaz de usuario, se puede admite el mismo valor de nombre entre los elementos del mismo nivel. Para la automatización de pruebas, los clientes deben considerar el uso de <strong>la propiedad AutomationId</strong> <strong>o RuntimeId.</strong><br/> Los controles de texto no siempre tienen que hacer que la propiedad <strong>Name</strong> sea <strong></strong> idéntica al texto que se muestra en el control , siempre y cuando también se admite el patrón Text.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td >Identifica la propiedad <strong>NativeWindowHandle,</strong> que es un entero que representa el identificador<strong>(HWND)</strong>de la ventana de elementos de automatización, si existe; De lo contrario, esta propiedad es 0.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td >Identifica la <strong>propiedad OptimizeForVisualContent,</strong> que es un valor booleano que indica si el proveedor expone solo los elementos visibles. Un proveedor puede usar esta propiedad para optimizar el rendimiento al trabajar con fragmentos de contenido muy grandes. Por ejemplo, a medida que el usuario pagina a través de un gran fragmento de contenido, el proveedor puede destruir elementos de contenido que ya no están visibles. Cuando se destruye un elemento de contenido, el proveedor debe devolver el <strong>UIA_E_ELEMENTNOTAVAILABLE</strong> de error. Se admite a partir de Windows 8.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor predeterminado: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td >Identifica la <strong>propiedad Orientation,</strong> que indica la orientación del control representado por el elemento de automatización. La propiedad se expresa como un valor del tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType.</strong></a><br/> La <strong>propiedad Orientation</strong> es compatible con controles, como barras de desplazamiento y controles deslizantes, que pueden tener una orientación vertical o horizontal. De lo contrario, siempre se <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>puede OrientationType_None</strong></a>, lo que significa que el control no tiene ninguna orientación.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>)<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td >Identifica la <strong>propiedad OutlineColor,</strong> que especifica el color utilizado para el contorno del elemento de automatización. Este atributo se especifica como <strong>COLORREF,</strong>un valor de 32 bits que se usa para especificar un color RGB o RGBA.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td >Identifica la <strong>propiedad OutlineThickness,</strong> que especifica el ancho del contorno del elemento de automatización.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td >Identifica la <strong>propiedad PositionInSet,</strong> que es un entero basado en 1 asociado a un elemento de automatización. <strong>PositionInSet</strong> describe la ubicación ordinal del elemento dentro de un conjunto de elementos que se consideran elementos del mismo nivel.<br/> <strong>PositionInSet</strong> funciona en coordinación con <strong>la propiedad SizeOfSet</strong> para describir la ubicación ordinal del conjunto.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td >Identifica la <strong>propiedad ProcessId,</strong> que es un entero que representa el identificador de proceso (ID) del elemento de automatización.<br/> El sistema operativo asigna el identificador de proceso (ID). Se puede ver en la columna <strong>PID</strong> de la <strong>pestaña Procesos</strong> de Administrador de tareas.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td >Identifica la <strong>propiedad ProviderDescription,</strong> que es una cadena con formato que contiene la información de origen del proveedor de Automatización de la interfaz de usuario para el elemento de automatización, incluida la información de proxy.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor predeterminado: cadena vacía<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td >Identifica la propiedad <strong>Rotation,</strong> que especifica el ángulo de rotación en unidades no especificadas.<br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td >Identifica la propiedad <strong>RuntimeId,</strong> que es una matriz de enteros que representa el identificador de un elemento de automatización.<br/> El identificador es único en el escritorio, pero se garantiza que es único solo dentro de la interfaz de usuario del escritorio en el que se generó. Los identificadores se pueden reutilizar con el tiempo.<br/> El formato de <strong>RuntimeId</strong> puede cambiar. El identificador devuelto debe tratarse como un valor opaco y usarse solo para la comparación; por ejemplo, para determinar si un elemento de automatización está en la memoria caché.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td >Identifica la <strong>propiedad Size,</strong> que especifica el ancho y alto del elemento de automatización.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor predeterminado: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td >Identifica la <strong>propiedad SizeOfSet,</strong> que es un entero basado en 1 asociado a un elemento de automatización. <strong>SizeOfSet</strong> describe el número de elementos de automatización de un grupo o conjunto que se consideran elementos del mismo nivel.<br/> <strong>SizeOfSet</strong> funciona en coordinación con la <strong>propiedad PositionInSet</strong> para describir el recuento de elementos del conjunto.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor predeterminado: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td >Identifica la <strong>propiedad VisualEffects,</strong> que es un campo de bits que especifica los efectos en el elemento de automatización, como sombra, reflexión, efecto de iluminado, bordes flexibles o bisel.<br/> VisualEffects:<br/>
<ul>
<li>VisualEffects_Shadow: 0x1</li>
<li>VisualEffects_Reflection: 0x2</li>
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
| Cliente mínimo compatible<br/> | Windows Aplicaciones \[ de escritorio XP para aplicaciones para \| UWP\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2003 \[ \| aplicaciones para UWP\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>UIAutomationClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Recuperar propiedades de Automatización de la interfaz de usuario elementos](uiauto-propertiesforclients.md)
</dt> </dl>
