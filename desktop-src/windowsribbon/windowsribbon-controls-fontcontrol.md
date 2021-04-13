---
title: Control de fuente
description: Para simplificar la integración y la configuración de la compatibilidad de fuentes en aplicaciones que requieren funciones de procesamiento de texto y de edición de texto, el marco de la cinta de opciones de Windows proporciona un control de fuente especializado que expone una amplia gama de propiedades de fuente como el nombre del tipo de letra, el estilo, el tamaño de los puntos y los efectos.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420972"
---
# <a name="font-control"></a>Control de fuente

Para simplificar la integración y la configuración de la compatibilidad de fuentes en aplicaciones que requieren funciones de procesamiento de texto y de edición de texto, el marco de la cinta de opciones de Windows proporciona un control de fuente especializado que expone una amplia gama de propiedades de fuente como el nombre del tipo de letra, el estilo, el tamaño de los puntos y los efectos.

-   [Introducción](#introduction)
-   [Una experiencia coherente](#a-consistent-experience)
-   [Fácil integración y configuración](#easy-integration-and-configuration)
-   [Alineación con estructuras de texto GDI comunes](#alignment-with-common-gdi-text-structures)
-   [Agregar un FontControl](#add-a-fontcontrol)
    -   [Declarar un FontControl en el marcado](#declaring-a-fontcontrol-in-markup)
    -   [Propiedades de control de fuente](#font-control-properties)
-   [Definición de un controlador de comandos de FontControl](#define-a-fontcontrol-command-handler)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

El control fuente es un control compuesto que consta de botones, botones de alternancia, cuadros de lista desplegables y cuadros combinados, que se utilizan para especificar una propiedad de fuente o una opción de formato determinadas.

En la captura de pantalla siguiente se muestra el control de fuente de la cinta de opciones en WordPad para Windows 7.

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a>Una experiencia coherente

Como control integrado de la cinta de opciones, el control de fuentes mejora la funcionalidad general de administración de fuentes, selección y formato, y proporciona una experiencia de usuario enriquecida y coherente en todas las aplicaciones de la cinta de opciones.

Esta experiencia coherente incluye

-   Formato estandarizado y selección de fuentes entre aplicaciones de la cinta de opciones.
-   Representación de fuentes estandarizada en las aplicaciones de cinta.
-   Automática, en Windows 7, activación de fuentes basada en el valor **Mostrar** u **ocultar** para cada fuente en el panel de control **fuentes** . El control fuente solo muestra las fuentes que se han establecido en **Mostrar**.
    > [!Note]  
    > En Windows Vista, el panel de control **fuentes** no ofrece la funcionalidad **Mostrar** u **ocultar** , por lo que se activan todas las fuentes.

     

-   Administración de fuentes que está disponible directamente desde el control.

    La siguiente captura de pantalla muestra que se puede tener acceso al panel de control **fuentes** directamente desde el control fuente.

    ![captura de pantalla de la lista de familias de fuentes en WordPad para Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   Compatibilidad con la versión preliminar automática.
-   Exposición de fuentes que son más relevantes para un usuario, como
    -   Listas de fuentes localizadas para usuarios internacionales.
    -   Listas de fuentes basadas en el dispositivo de entrada.

    > [!Note]  
    > La compatibilidad con esta funcionalidad no está disponible en ninguna plataforma anterior a Windows 7.

     

## <a name="easy-integration-and-configuration"></a>Fácil integración y configuración

Al proporcionar funcionalidad estándar, reutilizable y de uso sencillo, el control de fuente de la cinta facilita la carga de integrar la compatibilidad de fuentes en una aplicación.

Los detalles de la selección de fuentes y el formato se ajustan en uno de los elementos lógicos independientes que

-   Elimina la administración compleja de interdependencias de control típicas de las implementaciones de control de fuentes.
-   Requiere un solo controlador de comandos para todas las funciones expuestas por los subcontrols de control de fuentes.

Este controlador de comandos único permite al control de fuentes administrar la funcionalidad de varios subcontrols internamente. un subcontrol nunca interactúa directamente con la aplicación, independientemente de su función.

Otras características del control de fuentes incluyen

-   Generación automática con reconocimiento de PPP de una representación de mapa de bits WYSIWYG (lo que se ve es lo que se obtiene) para cada fuente en el menú de la **familia de fuentes** .
-   Integración de [Windows interfaz de dispositivo gráfico (GDI)](../gdi/windows-gdi.md) .
-   Mapas de bits e información sobre herramientas de la familia de fuentes localizada.
-   Enumeración de fuentes, agrupación y metadatos para administrar y presentar fuentes.
    > [!Note]  
    > La compatibilidad con esta funcionalidad no está disponible en ninguna plataforma anterior a Windows 7.

     

-   El color del **texto** y el **texto resaltan** los separadores de colores desplegables que reflejan el comportamiento del [selector de colores](windowsribbon-controls-dropdowncolorpicker.md) desplegable de la cinta de opciones.
-   Compatibilidad con la vista previa automática de todos los subcontrols basados en la galería de controles de fuente: **familia de fuentes**, **tamaño de fuente**, color de **texto** y **color de resaltado de texto**.

## <a name="alignment-with-common-gdi-text-structures"></a>Alineación con estructuras de texto GDI comunes

Los componentes de la pila de texto de [Windows interfaz de dispositivo gráfico (GDI)](../gdi/windows-gdi.md) se usan para exponer la funcionalidad de selección de fuente y de formato a través del control de fuente de la cinta de opciones. Las diversas características de fuente admitidas por la estructura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), la [estructura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)y la [estructura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) se exponen a través de los SubControles que se incluyen en el control de fuente.

Los SubControles que se muestran en el control de fuente dependen de la plantilla *FontType* declarada en el marcado de la cinta. Las plantillas *FontType* (que se describen con más detalle en la sección siguiente) están diseñadas para alinearse con las estructuras de texto comunes de [Windows interfaz de dispositivo gráfico (GDI)](../gdi/windows-gdi.md) .

## <a name="add-a-fontcontrol"></a>Agregar un FontControl

En esta sección se describen los pasos básicos para agregar un control de fuente a una aplicación de la cinta de opciones.

### <a name="declaring-a-fontcontrol-in-markup"></a>Declarar un FontControl en el marcado

Como otros controles de la cinta de opciones, el control de fuente se declara en el marcado con un elemento [**FontControl**](windowsribbon-element-fontcontrol.md) y se asocia a una declaración de comando a través de un identificador de comando. Cuando se compila la aplicación, el identificador de comando se usa para enlazar el comando a un controlador de comandos en la aplicación host.

> [!Note]  
> Si no se declara ningún identificador de comando con el [**FontControl**](windowsribbon-element-fontcontrol.md) en el marcado, el marco de trabajo genera uno.

 

Dado que los SubControles del control de fuente no se exponen directamente, la personalización del control de fuente se limita a tres plantillas de diseño de *FontType* definidas por el marco.

La personalización adicional del control de fuente puede realizarse mediante la combinación de la plantilla de diseño con atributos [**FontControl**](windowsribbon-element-fontcontrol.md) como *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible* y *IsUnderlineButtonVisible*.

> [!Note]  
> La funcionalidad de fuente más allá de la que exponen las plantillas y atributos del control de fuentes estándar requiere una implementación de control de fuentes personalizada que está fuera del ámbito de este artículo.

 

En la tabla siguiente se muestran las plantillas de control de fuentes y el tipo de control Edit con el que se alinea cada plantilla.



| Plantilla      | Es compatible con                                                                 |
|---------------|--------------------------------------------------------------------------|
| FontOnly      | [LOGFONT (estructura)](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| FontWithColor | [Estructura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| RichFont      | [Estructura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

En la tabla siguiente se enumeran los controles que están asociados a cada plantilla y se identifican los controles que son opcionales para una plantilla asociada.



Controles

Plantillas

**RichFont**

**FontWithColor**

**FontOnly**

Valor predeterminado

Opcional

Valor predeterminado

Opcional

Valor predeterminado

Opcionales

Cuadro combinado de **tamaño de fuente**

Sí

No

Sí

No

Sí

No

Cuadro combinado de **familia de fuentes**

Sí

No

Sí

No

Sí

No

Botón **aumentar fuente**

Sí

Sí

Sí

Sí

\-

\-

Botón **reducir fuente**

Sí

Sí

Sí

Sí

\-

\-

Botón **negrita**

Sí

No

Sí

No

Sí

No

Botón **cursiva**

Sí

No

Sí

No

Sí

No

**Subrayado** (botón)

Sí

No

Sí

Sí

Sí

Sí

Botón **tachado**

Sí

No

Sí

Sí

Sí

Sí

Botón **subíndice**

Sí

No

\-

\-

\-

\-

Botón **Superscript**

Sí

No

\-

\-

\-

\-

Botón de **color de resaltado de texto**

Sí

No

Sí

Sí

\-

\-

Botón **color del texto**

Sí

No

Sí

No

\-

\-



 

Cuando se declara el comportamiento de diseño de un control de fuente, el marco de la cinta de opciones proporciona una plantilla de diseño *SizeDefinition* opcional, `OneFontControl` , que define dos configuraciones de subcontrol basadas en el tamaño de la cinta de opciones y el espacio disponible para el control de fuente. Para obtener más información, vea [personalizar una cinta de opciones a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md).

### <a name="adding-a-fontcontrol-to-a-ribbon"></a>Agregar un FontControl a una cinta de opciones

En los siguientes ejemplos de código se muestran los requisitos básicos de marcado para agregar un control de fuente a una cinta de opciones:

En esta sección de código se muestra el marcado de declaración del comando [**FontControl**](windowsribbon-element-fontcontrol.md) , incluidos los comandos de [**pestaña**](windowsribbon-element-tab.md) y de [**Grupo**](windowsribbon-element-group.md) necesarios para mostrar un control en la [**cinta**](windowsribbon-element-ribbon.md)de opciones.


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



En esta sección de código se muestra el marcado necesario para declarar y asociar un [**FontControl**](windowsribbon-element-fontcontrol.md) con un [**comando**](windowsribbon-element-command.md) mediante un identificador de comando. En este ejemplo concreto se incluyen las declaraciones de [**pestaña**](windowsribbon-element-tab.md) y [**Grupo**](windowsribbon-element-group.md) , con las preferencias de escalado.


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a>Agregar un FontControl a un ContextPopup

Agregar un control de fuente a un [elemento emergente de contexto](windowsribbon-controls-contextpopup.md) requiere un procedimiento similar al de agregar un control de fuente a la cinta de opciones. Sin embargo, un control de fuente de un [**MiniToolbar**](windowsribbon-element-minitoolbar.md) está restringido al conjunto de subcontrols predeterminados que son comunes a todas las plantillas de control de fuentes: **familia de fuentes**, **tamaño de fuente**, **negrita** y **cursiva**.

En los siguientes ejemplos de código se muestran los requisitos básicos de marcado para agregar un control de fuente a un [elemento emergente de contexto](windowsribbon-controls-contextpopup.md):

En esta sección de código se muestra el marcado de declaración de comandos [**FontControl**](windowsribbon-element-fontcontrol.md) que se requiere para mostrar un **FontControl** en [**ContextPopup**](windowsribbon-element-contextpopup.md).


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



En esta sección de código se muestra el marcado necesario para declarar y asociar un [**FontControl**](windowsribbon-element-fontcontrol.md) con un comando mediante un identificador de comando.


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a>Keytips

Cada subcontrol del control de fuente de la cinta de opciones es accesible a través de un método abreviado de teclado o KeyTip. Este KeyTip está predefinido y se asigna a cada subcontrol por el marco de trabajo.

Si se asigna un valor de atributo *KeyTip* al elemento [**FontControl**](windowsribbon-element-fontcontrol.md) en el marcado, este valor se agrega como prefijo al KeyTip definido por el marco de trabajo.

> [!Note]  
> La aplicación debe aplicar una regla de un solo carácter para este prefijo.

 

En la tabla siguiente se enumeran las keytips definidas por el marco. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Control secundario</th>
<th>KeyTip</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Familia de fuentes</td>
<td>F</td>
</tr>
<tr class="even">
<td>Estilo de fuente</td>
<td>T</td>
</tr>
<tr class="odd">
<td>Tamaño de fuente</td>
<td>S</td>
</tr>
<tr class="even">
<td>Aumentar fuente</td>
<td>G</td>
</tr>
<tr class="odd">
<td>Reducir fuente</td>
<td>K</td>
</tr>
<tr class="even">
<td>Bold</td>
<td>B</td>
</tr>
<tr class="odd">
<td>Cursiva</td>
<td>I</td>
</tr>
<tr class="even">
<td>Subrayado</td>
<td>U</td>
</tr>
<tr class="odd">
<td>Tachado</td>
<td>X</td>
</tr>
<tr class="even">
<td>Superscript</td>
<td>Y o Z
<blockquote>
[!Note]<br />
Si el atributo <em>KeyTip</em> no se declara en el marcado, el KeyTip predeterminado es Y; de lo contrario, el KeyTip predeterminado es <em>KeyTip</em> + Z.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Subscript</td>
<td>A</td>
</tr>
<tr class="even">
<td>Color de fuente</td>
<td>C</td>
</tr>
<tr class="odd">
<td>Resaltado de fuentes</td>
<td>H</td>
</tr>
</tbody>
</table>



 

El prefijo recomendado para una interfaz de usuario multilingüe (MUI) EN-US es "F", tal y como se muestra en el ejemplo siguiente.


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



En la siguiente captura de pantalla se muestran las keytips del control de fuentes, tal como se definen en el ejemplo anterior.

![captura de pantalla de las keytips de fontcontrol en WordPad para Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a>El archivo de recursos de la cinta de opciones

Cuando se compila el archivo de marcado, se genera un archivo de recursos que contiene todas las referencias de recursos para la aplicación de cinta.

Ejemplo de un archivo de recursos simple:


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a>Propiedades de control de fuente

El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de fuente y sus subcontrols constituyentes.

Normalmente, una propiedad de control de fuente se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de fuente.



| Clave de propiedad                                                                                                                  | Notas                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI \_ PKEY \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | Expone, en Aggregate como un objeto [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) , todas las propiedades de subcontrol de control de fuente.<br/> El marco de trabajo consulta esta propiedad cuando `UI_INVALIDATIONS_VALUE` se pasa como el valor de *Flags* en la llamada a [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).<br/> |
| [UI \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | Expone, en Aggregate como un objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , solo las propiedades de subcontrol de control de fuente que han cambiado.<br/>                                                                                                                                                                                                        |
| [KeyTip de UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                                                                                                                                                                                      |
| [PKEY de IU \_ \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | Admite [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).                                                                                                                                                                  |



 

Además de las propiedades admitidas por el propio control de fuente, el marco de la cinta de opciones también define una [clave de propiedad](windowsribbon-reference-properties.md) para cada subcontrol de control de fuente. El marco de trabajo expone estas claves de propiedad y sus valores a través de una implementación de la interfaz [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) que define los métodos para administrar una colección, también denominada bolsa de propiedades, de pares nombre-valor.

La aplicación traduce las estructuras de fuente a propiedades a las que se puede tener acceso a través de los métodos de la interfaz [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Este modelo resalta la distinción entre el control de fuente y los componentes de la pila de texto de Windows Interfaz de dispositivo gráfico (GDI) ([estructura LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [estructura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)y [estructura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)) que son compatibles con el marco de trabajo.

En la tabla siguiente se enumeran los controles individuales y sus claves de propiedad asociadas.



| Controles                 | Clave de propiedad                                                                                                                                                                                                                                                           | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tamaño de fuente**            | [Tamaño de FontProperties de UI \_ PKEY \_ \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Cuando se resalta una ejecución de texto de tamaño heterogéneo, el marco de la cinta de opciones establece el control de **tamaño de fuente** en Blank y el valor de la [interfaz de usuario \_ PKEY \_ FontProperties \_ size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) en 0. Cuando se hace clic en el botón **aumentar fuente** o **reducir fuente** , se cambia el tamaño de todo el texto resaltado, pero se conserva la diferencia relativa en los tamaños de texto.                                                                                                                                                    |
| **Familia de fuentes**          | [Familia de FontProperties de UI \_ PKEY \_ \_](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | Los nombres de familia de fuentes de GDI varían con la configuración regional del sistema. Por lo tanto, si el valor de la [familia de PKEY de interfaz de usuario \_ \_ FontProperties \_ ](windowsribbon-reference-properties-uipkey-fontproperties-family.md) se conserva en las sesiones de la aplicación, ese valor se debe recuperar en cada nueva sesión.                                                                                                                                                                                                                                                                            |
| **Aumentar fuente**            | [Tamaño de FontProperties de UI \_ PKEY \_ \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Vea **tamaño de fuente**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Reducir fuente**          | [Tamaño de FontProperties de UI \_ PKEY \_ \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Vea **tamaño de fuente**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Negrita**                 | [UI \_ PKEY \_ FontProperties \_ Bold](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Cursiva**               | [UI \_ PKEY \_ FontProperties \_ cursiva](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Raya**            | [Subrayado de UI \_ PKEY \_ FontProperties \_](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Tachado**        | [PKEY de IU \_ \_ FontProperties \_ tachado](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Subíndice**            | [UI \_ PKEY \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Si se establece el botón **subíndice** , no se puede establecer también el **superíndice** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Superscript**          | [UI \_ PKEY \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Si se establece el botón de **superíndice** , no se puede establecer también el **subíndice** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Color de resaltado de texto** | [Interfaz de usuario \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ PKEY \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md) | Proporciona la misma funcionalidad que la `HighlightColors` plantilla del elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .<br/> Es muy recomendable que la aplicación solo establezca un valor de **color de resaltado de texto** inicial. El último valor seleccionado debe conservarse y no establecerse cuando el cursor se cambie de posición dentro de un documento. Esto permite un acceso rápido a la última selección del usuario y no es necesario volver a abrir el selector de colores.<br/> Las muestras de colores no se pueden personalizar.<br/> |
| **Color del texto**           | [Interfaz de usuario \_ PKEY \_ FontProperties \_ foregroundcolor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI \_ PKEY \_ FontProperties \_ ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)           | Proporciona la misma funcionalidad que la `StandardColors` plantilla del elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .<br/> Es muy recomendable que la aplicación solo establezca un valor de **color de texto** inicial. El último valor seleccionado debe conservarse y no establecerse cuando el cursor se cambie de posición dentro de un documento. Esto permite un acceso rápido a la última selección del usuario y no es necesario volver a abrir el selector de colores.<br/> Las muestras de colores no se pueden personalizar.<br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a>Definición de un controlador de comandos de FontControl

En esta sección se describen los pasos necesarios para enlazar un control de fuente a un controlador de comandos.

> [!WARNING]
> Cualquier intento de seleccionar una muestra de color del selector de colores de un control de fuente puede producir una infracción de acceso si no hay ningún controlador de comandos asociado al control.

 

En el ejemplo de código siguiente se muestra cómo enlazar comandos que se declaran en el marcado a un controlador de comandos.


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



En el ejemplo de código siguiente se muestra cómo implementar el método [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para un control de fuente.


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



En el ejemplo de código siguiente se muestra cómo implementar el método [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) para un control de fuente.


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento FontControl**](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Ejemplo de FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

