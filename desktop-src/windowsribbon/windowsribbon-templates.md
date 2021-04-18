---
title: Personalización de una cinta a través de definiciones de tamaño y directivas de escalado
description: Los controles hospedados en la barra de comandos de la cinta de opciones están sujetos a las reglas de diseño que aplica el marco de la cinta de opciones de Windows y se basan en una combinación de comportamientos y plantillas de diseño predeterminados (definidas por el marco y personalizadas) como se declara en el marcado de la cinta. Estas reglas definen los comportamientos de diseño adaptable del marco de cinta que influyen en cómo se adaptan los controles de la barra de comandos a varios tamaños de cinta en tiempo de ejecución.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Cinta de Windows, personalizar
- Cinta, personalizar
- Cinta de Windows, plantillas de SizeDefinition
- Cinta de opciones, plantillas de SizeDefinition
- Cinta de opciones de Windows, plantillas personalizadas
- Cinta de opciones, plantillas personalizadas
- Personalización de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b12618f88576cddeff119534215e501216193c3
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/30/2020
ms.locfileid: "104560258"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>Personalización de una cinta a través de definiciones de tamaño y directivas de escalado

Los controles hospedados en la barra de comandos de la cinta de opciones están sujetos a las reglas de diseño que aplica el marco de la cinta de opciones de Windows y se basan en una combinación de comportamientos y plantillas de diseño predeterminados (definidas por el marco y personalizadas) como se declara en el marcado de la cinta. Estas reglas definen los comportamientos de diseño adaptable del marco de cinta que influyen en cómo se adaptan los controles de la barra de comandos a varios tamaños de cinta en tiempo de ejecución.

-   [Introducción](#introduction)
    -   [Plantillas SizeDefinition de la cinta](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [Plantillas personalizadas](#custom-templates)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

El diseño adaptable, tal como se define en el marco de la cinta de opciones, es la capacidad de todos los controles de la interfaz de usuario de la cinta de ajustar dinámicamente la organización, el tamaño, el formato y la escala relativa en función de los cambios en el tamaño de la cinta de opciones en tiempo de ejecución.

El marco de trabajo expone la funcionalidad de diseño adaptable a través de un conjunto de elementos de marcado que están dedicados a especificar y personalizar distintos comportamientos de diseño. Una colección de plantillas, denominada [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), se define en el marco de trabajo, cada una de las cuales admite varios escenarios de control y diseño. Sin embargo, el marco también admite plantillas personalizadas si las plantillas predefinidas no proporcionan la experiencia de interfaz de usuario ni los diseños necesarios para una aplicación.

Para mostrar los controles en un diseño preferido en un tamaño de cinta determinado, las plantillas predefinidas y las plantillas personalizadas funcionan junto con el elemento [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) . Este elemento contiene un manifiesto de las preferencias de tamaño que el marco de trabajo usa como guía al representar la cinta de opciones.

> [!Note]  
> El marco de cinta proporciona comportamientos de diseño predeterminados basados en un conjunto de heurísticas integradas para la organización y presentación de controles en tiempo de ejecución sin necesidad de las plantillas predefinidas de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) . Sin embargo, esta funcionalidad está pensada solo para la generación de prototipos.

 

### <a name="ribbon-sizedefinition-templates"></a>Plantillas SizeDefinition de la cinta

El marco de cinta de opciones proporciona un conjunto completo de plantillas de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) que especifican el tamaño y el comportamiento de diseño de un [Grupo](windowsribbon-controls-group.md) de controles de la cinta. Estas plantillas cubren los escenarios más comunes para organizar los controles en una aplicación de cinta.

Para aplicar una experiencia de usuario coherente en todas las aplicaciones de la cinta, cada plantilla de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impone restricciones en los controles o en la familia de controles que admite.

Por ejemplo, la familia de controles Button incluye:

-   [Botón](windowsribbon-controls-button.md)
-   [Botón de alternancia](windowsribbon-controls-togglebutton.md)
-   [Botón desplegable](windowsribbon-controls-dropdownbutton.md)
-   [Botón de expansión](windowsribbon-controls-splitbutton.md)
-   [Galería desplegable](windowsribbon-controls-dropdowngallery.md)
-   [Galería de botones de expansión](windowsribbon-controls-splitbuttongallery.md)
-   [Selector de colores desplegables](windowsribbon-controls-dropdowncolorpicker.md)

Mientras que la familia de controles de entrada incluye:

-   [Cuadro combinado](windowsribbon-controls-combobox.md)
-   [Spinner](windowsribbon-controls-spinner.md)

Las [casillas](windowsribbon-controls-checkbox.md) y [en la galería de la cinta de](windowsribbon-controls-inribbongallery.md) opciones no pertenecen a la familia de botones ni a la familia de entrada. Estos dos controles solo se pueden usar cuando se indican explícitamente en una plantilla [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

A continuación se muestra una lista de las plantillas [**SizeDefinition**](windowsribbon-element-sizedefinition.md) con una descripción del diseño y los controles permitidos por cada plantilla.

> [!IMPORTANT]
> Si los controles declarados en el marcado no se asignan exactamente al tipo de control, el orden y la cantidad definidos en la plantilla asociada, el [compilador de marcado](windowsribbon-intentcl.md) registra un [error de validación](windowsribbon-compilationerrors.md) y finaliza la compilación.

 



OneButton

Un control de familia de botones.<br/> Solo se admite el tamaño de grupo grande.<br/>

![imagen de la plantilla de OneButton sizedefinition.](images/overviews/sizedefinition-onebutton.png)

TwoButtons

Dos controles de la familia de botones.<br/> Solo se admiten tamaños de grupo grandes y medianas.<br/>

![imagen de la plantilla twobuttons Large sizedefinition](images/overviews/sizedefinition-twobuttons-large.png)

![imagen de la plantilla sizedefinition twobuttons Medium.](images/overviews/sizedefinition-twobuttons-medium.png)

ThreeButtons

Tres controles de la familia de botones.<br/> Solo se admiten tamaños de grupo grandes y medianas.<br/>

![imagen de la plantilla threebuttons Large sizedefinition](images/overviews/sizedefinition-threebuttons-large.png)

![imagen de la plantilla sizedefinition threebuttons Medium.](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

Tres controles de la familia de botones.<br/> El primer botón se presenta de forma destacada en los tres tamaños.<br/>

![imagen de la plantilla threebuttons-onebigandtwosmall Large sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![imagen de la plantilla threebuttons-onebigandtwosmall Medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![imagen de la plantilla threebuttons-onebigandtwosmall Small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

ThreeButtonsAndOneCheckBox

Tres controles de la familia de botones acompañados por un único control CheckBox.<br/> Solo se admiten tamaños de grupo grandes y medianas.<br/>

![imagen de la plantilla threebuttonsandonecheckbox Large sizedefinition](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![imagen de la plantilla sizedefinition threebuttonsandonecheckbox Medium.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

FourButtons

Cuatro controles de la familia de botones.<br/>

![imagen de la plantilla fourbuttons Large sizedefinition](images/overviews/sizedefinition-fourbuttons-large.png)

![imagen de la plantilla sizedefinition fourbuttons Medium.](images/overviews/sizedefinition-fourbuttons-medium.png)

![imagen de la plantilla fourbuttons Small sizedefinition](images/overviews/sizedefinition-fourbuttons-small.png)

FiveButtons

Cinco controles de la familia de botones.<br/>

![imagen de la plantilla fivebuttons Large sizedefinition](images/overviews/sizedefinition-fivebuttons-large.png)

![imagen de la plantilla sizedefinition fivebuttons Medium.](images/overviews/sizedefinition-fivebuttons-medium.png)

![imagen de la plantilla fivebuttons Small sizedefinition](images/overviews/sizedefinition-fivebuttons-small.png)

FiveOrSixButtons

Cinco controles de la familia de botones y un sexto botón opcional.<br/>

![imagen de la plantilla fiveorsixbuttons Large sizedefinition](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![imagen de la plantilla sizedefinition fiveorsixbuttons Medium.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![imagen de la plantilla fiveorsixbuttons Small sizedefinition](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

SixButtons

Seis controles de la familia de botones.<br/>

![imagen de la plantilla sixbuttons Large sizedefinition](images/overviews/sizedefinition-sixbuttons-large.png)

![imagen de la plantilla sizedefinition sixbuttons Medium.](images/overviews/sizedefinition-sixbuttons-medium.png)

![imagen de la plantilla sixbuttons Small sizedefinition](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

Seis controles de la familia de botones (presentación alternativa).<br/>

![imagen de la plantilla sixbuttons-twocolumns Large sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons: twocolumns Medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![imagen de la plantilla sixbuttons-twocolumns Small sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

SevenButtons

Siete controles de la familia de botones.<br/>

![imagen de la plantilla sevenbuttons Large sizedefinition](images/overviews/sizedefinition-sevenbuttons-large.png)

![imagen de la plantilla de sevenbuttons mediumsizedefinition.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![imagen de la plantilla sevenbuttons Small sizedefinition](images/overviews/sizedefinition-sevenbuttons-small.png)

EightButtons

Ocho controles de la familia de botones.<br/>

![imagen de la plantilla eightbuttons-lastthreesmall Large sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![imagen de la plantilla eightbuttons-lastthreesmall Medium sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![imagen de la plantilla eightbuttons-lastthreesmall Small sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

Ocho controles de la familia de botones (presentación alternativa).<br/>

> [!Note]  
> Todos los elementos de control declarados con esta plantilla deben estar contenidos en dos elementos [**ControlGroup**](windowsribbon-element-controlgroup.md) : uno para los primeros cinco elementos y otro para los tres últimos elementos.

<br/> En el ejemplo siguiente se muestra el marcado necesario para esta plantilla.<br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![imagen de la plantilla eightbuttons Large sizedefinition](images/overviews/sizedefinition-eightbuttons-large.png)

![imagen de la plantilla sizedefinition eightbuttons Medium.](images/overviews/sizedefinition-eightbuttons-medium.png)

![imagen de la plantilla eightbuttons Small sizedefinition](images/overviews/sizedefinition-eightbuttons-small.png)

NineButtons

Nueve controles de la familia de botones.

![imagen de la plantilla ninebuttons Large sizedefinition](images/overviews/sizedefinition-ninebuttons-large.png)

![imagen de la plantilla sizedefinition ninebuttons Medium.](images/overviews/sizedefinition-ninebuttons-medium.png)

![imagen de la plantilla ninebuttons Small sizedefinition](images/overviews/sizedefinition-ninebuttons-small.png)

TenButtons

Diez controles de la familia de botones.

![imagen de la plantilla tenbuttons Large sizedefinition](images/overviews/sizedefinition-tenbuttons-large.png)

![imagen de la plantilla sizedefinition tenbuttons Medium.](images/overviews/sizedefinition-tenbuttons-medium.png)

![imagen de la plantilla tenbuttons Small sizedefinition](images/overviews/sizedefinition-tenbuttons-small.png)

ElevenButtons

Once controles de la familia de botones.

![imagen de la plantilla elevenbuttons Large sizedefinition](images/overviews/sizedefinition-elevenbuttons-large.png)

![imagen de la plantilla sizedefinition elevenbuttons Medium.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![imagen de la plantilla elevenbuttons Small sizedefinition](images/overviews/sizedefinition-elevenbuttons-small.png)

OneFontControl

Un [**FontControl**](windowsribbon-element-fontcontrol.md).

Solo se admiten tamaños de grupo grandes y medianas.

> [!IMPORTANT]
> El marco de trabajo no admite la inclusión de [**FontControl**](windowsribbon-element-fontcontrol.md) dentro de una definición de plantilla personalizada.

 

![imagen de la plantilla onefontcontrol Large sizedefinition](images/overviews/sizedefinition-onefontcontrol-large.png)

![imagen de la plantilla sizedefinition onefontcontrol Medium.](images/overviews/sizedefinition-onefontcontrol-medium.png)

OneInRibbonGallery

Un control [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .

Solo se admiten tamaños de grupo grandes y pequeños.

![imagen de la plantilla oneinribbongallery Large sizedefinition](images/overviews/sizedefinition-oneinribbongallery-large.png)

![imagen de la plantilla oneinribbongallery Small sizedefinition](images/overviews/sizedefinition-oneinribbongallery-small.png)

InRibbonGalleryAndBigButton

Un control [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) y un control Family Button.

Solo se admiten tamaños de grupo grandes y pequeños.

![imagen de la plantilla inribbongalleryandbigbutton Large sizedefinition](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![imagen de la plantilla inribbongalleryandbigbutton Small sizedefinition](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

Un control [de la galería de la cinta de](windowsribbon-controls-inribbongallery.md) opciones y dos o tres controles de la familia de botones.

La galería se contrae en la representación emergente en tamaños de grupo de tamaño medio y pequeño.

![imagen de la plantilla inribbongalleryandbuttons-galleryscalesfirst Large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![imagen de la plantilla inribbongalleryandbuttons-galleryscalesfirst Medium sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![imagen de la plantilla inribbongalleryandbuttons-galleryscalesfirst Small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

ButtonGroups

Una organización compleja de controles de familia de botones de 32 (la mayoría de los cuales son opcionales).

> [!Note]  
> Aparte del botón opcional de tamaño completo de la plantilla grande de ButtonGroups, todos los elementos de control que se declaran con esta plantilla deben estar contenidos en elementos [**ControlGroup**](windowsribbon-element-controlgroup.md) .

 

En el ejemplo siguiente se muestra el marcado necesario para mostrar todos los elementos de control de 32 (obligatorio y opcional) con esta plantilla.


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![imagen de la plantilla buttongroups Large sizedefinition](images/overviews/sizedefinition-buttongroups-large.png)

![imagen de la plantilla sizedefinition buttongroups Medium.](images/overviews/sizedefinition-buttongroups-medium.png)

![imagen de la plantilla buttongroups Small sizedefinition](images/overviews/sizedefinition-buttongroups-small.png)

ButtonGroupsAndInputs

Dos controles de la familia de entrada (el segundo es opcional) seguidos de una organización compleja de 29 controles de la familia de botones (la mayoría de los cuales son opcionales).

Solo se admiten tamaños de grupo grandes y medianas.

> [!Note]  
> Todos los elementos de control declarados con esta plantilla deben estar contenidos en elementos [**ControlGroup**](windowsribbon-element-controlgroup.md) .

 

En el ejemplo siguiente se muestra el marcado necesario para mostrar todos los elementos de control (obligatorio y opcional) con esta plantilla.


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![imagen de la plantilla buttongroupsandinputs Large sizedefinition](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![imagen de la plantilla sizedefinition buttongroupsandinputs Medium.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

BigButtonsAndSmallButtonsOrInputs

Dos controles de la familia de botones (ambos opcionales) seguidos de dos o tres controles de botón o familia de entrada.

Solo se admiten tamaños de grupo grandes y medianas.

![imagen de la plantilla bigbuttonsandsmallbuttonsorinputs Large sizedefinition](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![imagen de la plantilla sizedefinition bigbuttonsandsmallbuttonsorinputs Medium.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>Ejemplo de SizeDefinition básico

En el ejemplo de código siguiente se proporciona una demostración básica de cómo declarar una plantilla de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) en el marcado de la cinta.

*OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) se usa para este ejemplo concreto, pero todas las plantillas de Framework se especifican de manera similar.


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a>Ejemplo de SizeDefinition complejo con directivas de escalado

El comportamiento de contracción de las plantillas [**SizeDefinition**](windowsribbon-element-sizedefinition.md) se puede controlar mediante el uso de directivas de escalado en el marcado de la cinta de opciones.

El elemento [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contiene un manifiesto de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) y declaraciones de [**escala**](windowsribbon-element-scale.md) que especifican las preferencias de diseño adaptable para uno o más elementos de [**Grupo**](windowsribbon-element-group.md) cuando se cambia el tamaño de la cinta de opciones.

> [!Note]  
> Se recomienda especificar el nivel de detalle de la Directiva de escalado adecuado de modo que la mayoría de los elementos de [**Grupo**](windowsribbon-element-group.md) , si no todos, estén asociados a un elemento de [**escala**](windowsribbon-element-scale.md) en el que el atributo de *tamaño* sea igual a `Popup` . Esto permite al marco de trabajo representar la cinta de opciones con el menor tamaño posible y admitir la gama más amplia de dispositivos de pantalla, antes de introducir automáticamente un mecanismo de desplazamiento.

 

En el ejemplo de código siguiente se muestra un manifiesto de [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) que especifica una preferencia [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de cuatro grupos de controles en una pestaña **Inicio** . Además, los elementos de [**escala**](windowsribbon-element-scale.md) se especifican para influir en el comportamiento de contracción, en orden de tamaño descendente, de cada grupo.


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a>Plantillas personalizadas

Si los comportamientos de diseño predeterminados y las plantillas predefinidas de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) no ofrecen la flexibilidad o compatibilidad para un escenario de diseño determinado, el marco de la cinta de opciones admite plantillas personalizadas a través del elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .

Las plantillas personalizadas se pueden declarar de dos maneras: un método independiente mediante el elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) para declarar plantillas con nombre reutilizables o un método insertado específico del [**Grupo**](windowsribbon-element-group.md).

### <a name="standalone-template"></a>Plantilla independiente

En el ejemplo de código siguiente se muestra una plantilla personalizada básica reutilizable.


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a>Plantilla alineada

En los siguientes ejemplos de código se muestra una plantilla personalizada básica insertada para un grupo de cuatro botones.

En esta sección de código se muestran las declaraciones de comandos de un grupo de botones. Los recursos de imagen grandes y pequeños también se especifican aquí.


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



En esta sección de código se muestra cómo definir plantillas [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) grandes, medianas y pequeñas para mostrar los cuatro botones en distintos tamaños y diseños. La declaración [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) de la pestaña define la plantilla que se usa para un grupo de controles basándose en el tamaño de la cinta de opciones y el espacio que requiere la pestaña activa.


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



En las siguientes imágenes se muestra cómo se aplican las plantillas del ejemplo anterior a la interfaz de usuario de la cinta para dar cabida a una reducción del tamaño de la cinta.



|        |                                                                                                    |
|--------|----------------------------------------------------------------------------------------------------|
| Grande  | ![imagen de una plantilla personalizada de gran tamaño en línea.](images/overviews/sizedefinition-custom-large.png)   |
| Media | ![imagen de una plantilla personalizada mediana en línea.](images/overviews/sizedefinition-custom-medium.png) |
| Pequeña  | ![imagen de una plantilla personalizada pequeña insertada.](images/overviews/sizedefinition-custom-small.png)   |
| Popup  | ![imagen de una plantilla personalizada emergente en línea.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**SizeDefinition**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**Escala**](windowsribbon-element-scale.md)
</dt> <dt>

[**Group (Grupo)**](windowsribbon-element-group.md)
</dt> </dl>

 

 





