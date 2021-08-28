---
title: Control de fuentes
description: Para simplificar la integración y configuración de la compatibilidad con fuentes en aplicaciones que requieren capacidades de procesamiento de texto y edición de texto, el marco de la cinta de opciones de Windows proporciona un control de fuentes especializado que expone una amplia gama de propiedades de fuente, como el nombre del tipo de letra, el estilo, el tamaño de punto y los efectos.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 106163c03c506e438ffcffa261ebd7e3a2115e2a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470731"
---
# <a name="font-control"></a>Control de fuentes

Para simplificar la integración y configuración de la compatibilidad con fuentes en aplicaciones que requieren capacidades de procesamiento de texto y edición de texto, el marco de la cinta de opciones de Windows proporciona un control de fuentes especializado que expone una amplia gama de propiedades de fuente, como el nombre del tipo de letra, el estilo, el tamaño de punto y los efectos.

-   [Introducción](#introduction)
-   [Una experiencia coherente](#a-consistent-experience)
-   [Integración y configuración sencillas](#easy-integration-and-configuration)
-   [Alineación con estructuras de texto GDI comunes](#alignment-with-common-gdi-text-structures)
-   [Agregar un FontControl](#add-a-fontcontrol)
    -   [Declarar un fontcontrol en el marcado](#declaring-a-fontcontrol-in-markup)
    -   [Propiedades del control de fuentes](#font-control-properties)
-   [Definir un controlador de comandos FontControl](#define-a-fontcontrol-command-handler)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

El control de fuente es un control compuesto que consta de botones, botones de alternancia, cuadros de lista desplegables y cuadros combinados, que se usan para especificar una propiedad de fuente determinada o una opción de formato.

En la siguiente captura de pantalla se muestra el control de fuente de la cinta de opciones en WordPad para Windows 7.

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a>Una experiencia coherente

Como control de cinta de opciones integrado, el control de fuentes mejora la administración general de fuentes, la selección y la funcionalidad de formato, y proporciona una experiencia de usuario completa y coherente en todas las aplicaciones de la cinta de opciones.

Esta experiencia coherente incluye

-   Formato estandarizado y selección de fuentes en las aplicaciones de la cinta de opciones.
-   Representación de fuentes estandarizada entre aplicaciones de cinta de opciones.
-   Automática, en Windows 7, activación de fuentes  que  se basa en el valor Mostrar u ocultar de cada fuente en el panel **de** control Fuentes. El Control de fuentes solo muestra las fuentes que están establecidas en **Mostrar**.
    > [!Note]  
    > En Windows Vista, **el** panel de control  Fuentes  no ofrece la funcionalidad Mostrar u Ocultar, por lo que se activan todas las fuentes.

     

-   Administración de fuentes que está disponible directamente desde el control .

    En la siguiente captura de pantalla se muestra **que** se puede acceder al panel de control Fuentes directamente desde el Control de fuentes.

    ![captura de pantalla de la lista de familia de fuentes en el bloc de palabras para Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   Compatibilidad con la versión preliminar automática.
-   Exposición de fuentes que son más relevantes para un usuario, como
    -   Listas de fuentes localizadas para usuarios internacionales.
    -   Listas de fuentes basadas en el dispositivo de entrada.

    > [!Note]  
    > La compatibilidad con esta funcionalidad no está disponible en ninguna plataforma anterior a Windows 7.

     

## <a name="easy-integration-and-configuration"></a>Integración y configuración sencillas

Al proporcionar funcionalidad estándar, reutilizable y fácilmente consumida, el control de fuentes de la cinta de opciones facilita la carga de integrar la compatibilidad con fuentes en una aplicación.

Los detalles de la selección y el formato de fuentes se encapsulan en un elemento lógico independiente que

-   Elimina la administración compleja de interdependencias de control típicas de las implementaciones de control de fuentes.
-   Requiere un único controlador command para todas las funciones expuestas por los subcontroles de fuente.

Este único controlador de comandos permite que el control de fuentes administre internamente la funcionalidad de varios subcontroles. un subcontrol nunca interactúa directamente con la aplicación, independientemente de su función.

Otras características del control de fuentes son:

-   Generación automática y compatible con PPP de una representación de mapa de bits DE WYSIWYG (lo que se ve es lo que se obtiene) para cada fuente en el **menú Familia de** fuentes.
-   [Windows Interfaz de dispositivo gráfico (GDI).](../gdi/windows-gdi.md)
-   Mapas de bits e información sobre herramientas de la familia de fuentes localizadas.
-   Enumeración de fuentes, agrupación y metadatos para administrar y presentar fuentes.
    > [!Note]  
    > La compatibilidad con esta funcionalidad no está disponible en ninguna plataforma anterior a Windows 7 .

     

-   Los **selectores de color** desplegable Text color (Color de texto) y Text highlight color **(Color** de texto) que reflejan la lista desplegable [de cintas Selector de colores](windowsribbon-controls-dropdowncolorpicker.md) comportamiento.
-   Compatibilidad con la vista previa automática de todos los subcontroles basados en la galería de control de **fuentes:** familia de **fuentes,** tamaño de fuente, **color** de texto y **color de resaltado de texto**.

## <a name="alignment-with-common-gdi-text-structures"></a>Alineación con estructuras de texto GDI comunes

Windows Interfaz de dispositivo gráfico componentes de pila de [texto (GDI)](../gdi/windows-gdi.md) se usan para exponer la selección de fuentes y la funcionalidad de formato mediante el control de fuentes de la cinta de opciones. Las distintas características de fuente admitidas por la estructura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta)y [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a) se exponen a través de los subcontroles que se incluyen en el control de fuentes.

Los subcontroles que se muestran en el Control de fuentes dependen de la *plantilla FontType* declarada en el marcado de la cinta de opciones. Las *plantillas FontType* (que se detalló con más detalle en la sección siguiente) están diseñadas para alinearse con las estructuras de [texto comunes Windows Interfaz de dispositivo gráfico (GDI).](../gdi/windows-gdi.md)

## <a name="add-a-fontcontrol"></a>Agregar un FontControl

En esta sección se describen los pasos básicos para agregar un control de fuentes a una aplicación de cinta de opciones.

### <a name="declaring-a-fontcontrol-in-markup"></a>Declarar un fontcontrol en el marcado

Al igual que otros controles ribbon, el control Font se declara en marcado con un [**elemento FontControl**](windowsribbon-element-fontcontrol.md) y se asocia a una declaración Command a través de un identificador de comando. Cuando se compila la aplicación, el identificador de comando se usa para enlazar el comando a un controlador command en la aplicación host.

> [!Note]  
> Si no se declara ningún identificador de comando con [**FontControl**](windowsribbon-element-fontcontrol.md) en el marcado, el marco genera uno.

 

Dado que los subcontrolos del control de fuentes no se exponen directamente, la personalización del control de fuentes se limita a tres plantillas de diseño *FontType* definidas por el marco.

Se puede realizar una mayor personalización del control de fuentes combinando la plantilla de diseño con atributos [**FontControl**](windowsribbon-element-fontcontrol.md) como *IsHighlightButtonVisible,* *IsStrikethroughButtonVisible* e *IsUnderlineButtonVisible.*

> [!Note]  
> La funcionalidad de fuente más allá de la expuesta por las plantillas y atributos estándar de Control de fuentes requiere una implementación de control de fuentes personalizada que está fuera del ámbito de este artículo.

 

En la tabla siguiente se enumeran las plantillas de control de fuentes y el tipo de control de edición con el que se alinea cada plantilla.



| Plantilla      | Es compatible con                                                                 |
|---------------|--------------------------------------------------------------------------|
| FontOnly      | [LOGFONT (estructura)](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| FontWithColor | [CHOOSEFONT (estructura)](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| RichFont      | [CHARFORMAT2 (estructura)](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

En la tabla siguiente se enumeran los controles asociados a cada plantilla e identifica los controles que son opcionales para una plantilla asociada.



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

**Cuadro combinado tamaño de** fuente

Sí

No

Sí

No

Sí

No

**Cuadro combinado de familia** de fuentes

Sí

No

Sí

No

Sí

No

**Botón Aumentar fuente**

Sí

Sí

Sí

Sí

\-

\-

**Botón Reducir fuente**

Sí

Sí

Sí

Sí

\-

\-

**Botón Negrita**

Sí

No

Sí

No

Sí

No

**Botón Cursiva**

Sí

No

Sí

No

Sí

No

**Botón Subrayado**

Sí

No

Sí

Sí

Sí

Sí

**Botón tachado**

Sí

No

Sí

Sí

Sí

Sí

**Botón De subíndice**

Sí

No

\-

\-

\-

\-

**Botón De superíndice**

Sí

No

\-

\-

\-

\-

**Botón de color de resaltado de** texto

Sí

No

Sí

Sí

\-

\-

**Botón color de** texto

Sí

No

Sí

No

\-

\-



 

Cuando se declara el comportamiento de diseño de un control de fuente, el marco de la cinta de opciones proporciona una plantilla de diseño *SizeDefinition* opcional, , que define dos configuraciones de subcontrol basadas en el tamaño de la cinta de opciones y el espacio disponible para el `OneFontControl` control de fuentes. Para obtener más información, vea [Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado.](windowsribbon-templates.md)

### <a name="adding-a-fontcontrol-to-a-ribbon"></a>Agregar un FontControl a una cinta de opciones

En los ejemplos de código siguientes se muestran los requisitos de marcado básicos para agregar un control de fuente a una cinta de opciones:

En esta sección de código se muestra el marcado de declaración del comando [**FontControl,**](windowsribbon-element-fontcontrol.md) incluidos los comandos [**tab**](windowsribbon-element-tab.md) y [**group**](windowsribbon-element-group.md) necesarios para mostrar un control en la cinta de [**opciones**](windowsribbon-element-ribbon.md).


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



En esta sección de código se muestra el marcado necesario para declarar y asociar [**un FontControl**](windowsribbon-element-fontcontrol.md) a [**un comando**](windowsribbon-element-command.md) a través de un identificador de comando. En este ejemplo concreto se incluyen las [**declaraciones Tab**](windowsribbon-element-tab.md) [**y Group,**](windowsribbon-element-group.md) con preferencias de escalado.


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



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a>Agregar un FontControl a contextPopup

Agregar un control de fuente a un [elemento emergente de](windowsribbon-controls-contextpopup.md) contexto requiere un procedimiento similar al de agregar un control de fuente a la cinta de opciones. Sin embargo, un control de fuente en [**una barra miniherramienta**](windowsribbon-element-minitoolbar.md) está restringido al conjunto de subcontroles predeterminados que son comunes a todas las plantillas de control de **fuentes:** familia de **fuentes,** tamaño de **fuente,** negrita y **cursiva.**

En los ejemplos de código siguientes se muestran los requisitos de marcado básicos para agregar un control de fuente a un [elemento emergente de contexto](windowsribbon-controls-contextpopup.md):

En esta sección de código se muestra el marcado de declaración del comando [**FontControl**](windowsribbon-element-fontcontrol.md) necesario para mostrar **un FontControl** en [**ContextPopup.**](windowsribbon-element-contextpopup.md)


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



En esta sección de código se muestra el marcado necesario para declarar y asociar [**un FontControl**](windowsribbon-element-fontcontrol.md) a un comando a través de un identificador de comando.


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

Cada subcontrol del control de fuentes de la cinta de opciones es accesible a través de un método abreviado de teclado o la información sobre teclas. Esta información sobre claves está predefinida y asignada a cada subcontrol mediante el marco.

Si se asigna un valor de atributo *Keytip* al elemento [**FontControl**](windowsribbon-element-fontcontrol.md) en el marcado, este valor se agrega como prefijo a la información sobre claves definida por el marco.

> [!Note]  
> La aplicación debe aplicar una regla de un solo carácter para este prefijo.

 

En la tabla siguiente se enumeran las sugerencias clave definidas por el marco. 


| Subcontrol | Keytip | 
|-------------|--------|
| Familia de fuentes | F | 
| Estilo de fuente | T | 
| Tamaño de fuente | S | 
| Fuente de crecimiento | G | 
| Reducir fuente | K | 
| Negrita | B | 
| Cursiva | I | 
| Subrayado | U | 
| Tachado | X | 
| Superscript | Y o Z<blockquote>[!Note]<br />Si el <em>atributo Keytip</em> no se declara en el marcado, la información sobre claves predeterminada es Y; De lo contrario, la información sobre claves predeterminada es <em>Keytip</em> + Z.</blockquote><br /> | 
| Subscript | A | 
| Color de fuente | C | 
| Resaltado de fuente | H | 




 

El prefijo recomendado para una cinta Interfaz de usuario multilingüe (MUI) EN-US es "F", como se muestra en el ejemplo siguiente.


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



En la captura de pantalla siguiente se muestran las sugerencias clave de control de fuentes tal y como se definen en el ejemplo anterior.

![captura de pantalla de la información clave de fontcontrol en el bloc de palabras para Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a>El archivo de recursos de la cinta de opciones

Cuando se compila el archivo de marcado, se genera un archivo de recursos que contiene todas las referencias de recursos para la aplicación de cinta de opciones.

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



### <a name="font-control-properties"></a>Propiedades del control de fuentes

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de fuentes y sus subcontroles constituyentes.

Normalmente, una propiedad Control de fuentes se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El evento de invalidación se controla y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación ha consultado un valor de propiedad actualizado, hasta que el marco requiere la propiedad . Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control de fuentes.



| Clave de propiedad                                                                                                                  | Notas                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FontProperties de PKEY de la \_ interfaz de \_ usuario](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | Expone, de forma agregada como un [objeto IPropertyStore,](/windows/win32/api/propsys/nn-propsys-ipropertystore) todas las propiedades de subcontrol de control de fuentes.<br/> El marco consulta esta propiedad cuando se pasa como el valor de flags en la llamada `UI_INVALIDATIONS_VALUE` a [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand). <br/> |
| [UI \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | Expone, en agregado como un [**objeto IUISimplePropertySet,**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) solo las propiedades de subcontrol de control de fuentes que han cambiado.<br/>                                                                                                                                                                                                        |
| [Información sobre \_ claves PKEY \_ de la interfaz de usuario](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | Solo se puede actualizar a través de la invalidación.                                                                                                                                                                                                                                                                                                                                                      |
| [Ui \_ PKEY \_ habilitado](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | Admite [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).                                                                                                                                                                  |



 

Además de las propiedades admitidas por el propio control de fuentes, el marco de la cinta de opciones también define una clave de propiedad [para](windowsribbon-reference-properties.md) cada subcontrol de fuente. El marco expone estas claves de propiedad y sus valores a través de una implementación de interfaz [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) que define los métodos para administrar una colección, también denominada bolsa de propiedades, de pares de nombre y valor.

La aplicación convierte las estructuras de fuente en propiedades a las que se puede acceder a través de los [métodos de interfaz IPropertyStore.](/windows/win32/api/propsys/nn-propsys-ipropertystore) Este modelo resalta la distinción entre el control de fuentes y los componentes de pila de texto Windows Interfaz de dispositivo gráfico (GDI) (estructura[LOGFONT,](/windows/win32/api/wingdi/ns-wingdi-logfonta) [estructura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)y [estructura CHARFORMAT2)](/windows/win32/api/richedit/ns-richedit-charformat2a)que admite el marco.

En la tabla siguiente se enumeran los controles individuales y sus claves de propiedad asociadas.



| Controles                 | Clave de propiedad                                                                                                                                                                                                                                                           | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tamaño de fuente**            | [Tamaño \_ de fuente PKEY de la interfaz de \_ \_ usuarioPropiedades](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Cuando se resalta una ejecución de texto de tamaño heterogéneo, el marco de la cinta de opciones establece el **control** Tamaño de fuente en blanco y el valor de Ui [ \_ PKEY \_ FontProperties \_ Size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) en 0. Cuando se **hace clic en** el botón **Aumentar** fuente o Reducir fuente, se cambia el tamaño de todo el texto resaltado, pero se conserva la diferencia relativa en los tamaños de texto.                                                                                                                                                    |
| **Familia de fuentes**          | [Familia \_ FontProperties de PKEY de interfaz \_ de \_ usuario](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | Los nombres de familia de fuentes GDI varían con la configuración regional del sistema. Por lo tanto, si el valor de la familia [ \_ \_ FontProperties \_ ](windowsribbon-reference-properties-uipkey-fontproperties-family.md) de PKEY de la interfaz de usuario se conserva en las sesiones de la aplicación, ese valor se debe recuperar en cada nueva sesión.                                                                                                                                                                                                                                                                            |
| **Fuente de crecimiento**            | [Tamaño \_ de fuente PKEY de la interfaz de \_ \_ usuarioPropiedades](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Vea **Tamaño de fuente**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Reducir fuente**          | [Tamaño \_ de fuente PKEY de la interfaz de \_ \_ usuarioPropiedades](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Vea **Tamaño de fuente**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Negrita**                 | [UI \_ PKEY \_ FontProperties \_ Bold](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Cursiva**               | [UI \_ PKEY \_ FontProperties \_ Italic](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Subrayado**            | [Subrayado \_ fontproperties PKEY de la interfaz \_ de \_ usuario](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Tachado**        | [\_Tachado de \_ FontProperties de PKEY de la \_ interfaz de usuario](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Subíndice**            | [UI \_ PKEY \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Si se establece el botón **Subíndice,** no se puede establecer también el **superíndice.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Superscript**          | [UI \_ PKEY \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Si se establece el botón **Superscript,** no se puede establecer también el **subíndice.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Color de resaltado de texto** | [Interfaz de usuario \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ PKEY \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md) | Proporciona la misma funcionalidad que la `HighlightColors` plantilla del [**elemento DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)<br/> Se recomienda encarecidamente que solo la aplicación establezca un valor de **color** de resaltado de texto inicial. El último valor seleccionado debe conservarse y no establecerse cuando el cursor se cambia de posición dentro de un documento. Esto permite un acceso rápido a la última selección del usuario y no es necesario volver a abrir el selector de colores.<br/> Las muestras de color no se pueden personalizar.<br/> |
| **Color del texto**           | [Interfaz de usuario \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI \_ PKEY \_ FontProperties \_ ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)           | Proporciona la misma funcionalidad que la `StandardColors` plantilla del [**elemento DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)<br/> Se recomienda encarecidamente que solo la aplicación establezca un valor de **color** text inicial. El último valor seleccionado debe conservarse y no establecerse cuando el cursor se cambia de posición dentro de un documento. Esto permite un acceso rápido a la última selección del usuario y no es necesario volver a abrir el selector de colores.<br/> Las muestras de color no se pueden personalizar.<br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a>Definir un controlador de comandos FontControl

En esta sección se describen los pasos necesarios para enlazar un control de fuente a un controlador de comandos.

> [!WARNING]
> Cualquier intento de seleccionar una muestra de color del selector de colores de un control de fuente puede producir una infracción de acceso si no hay ningún controlador command asociado al control.

 

En el ejemplo de código siguiente se muestra cómo enlazar comandos declarados en marcado a un controlador Command.


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



En el ejemplo de código siguiente se muestra cómo implementar el [**método IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para un control font.


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



En el ejemplo de código siguiente se muestra cómo implementar el [**método IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) para un control font.


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

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento FontControl**](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Ejemplo de FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

