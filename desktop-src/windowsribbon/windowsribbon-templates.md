---
title: Personalización de una cinta de opciones mediante definiciones de tamaño y directivas de escalado
description: Los controles hospedados en la barra de comandos de la cinta de opciones están sujetos a reglas de diseño que exige el marco de la cinta de opciones de Windows y se basan en una combinación de comportamientos predeterminados y plantillas de diseño (tanto definidas como personalizadas para el marco) como se declaran en el marcado de la cinta de opciones. Estas reglas definen los comportamientos de diseño adaptable del marco de la cinta de opciones que influyen en cómo se adaptan los controles de la barra de comandos a varios tamaños de cinta en tiempo de ejecución.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows Cinta de opciones, personalización
- Cinta de opciones, personalización
- Windows Ribbon,SizeDefinition templates
- Ribbon,SizeDefinition templates
- Windows Cinta de opciones, plantillas personalizadas
- Cinta de opciones, plantillas personalizadas
- personalizar Windows cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eff1a9d1b2582d5386ce6ea0e02e20cfb5a806e1aaa4a98529474a756b5a8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933800"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>Personalización de una cinta de opciones mediante definiciones de tamaño y directivas de escalado

Los controles hospedados en la barra de comandos de la cinta de opciones están sujetos a reglas de diseño que exige el marco de la cinta de opciones de Windows y se basan en una combinación de comportamientos predeterminados y plantillas de diseño (tanto definidas como personalizadas para el marco) como se declaran en el marcado de la cinta de opciones. Estas reglas definen los comportamientos de diseño adaptable del marco de la cinta de opciones que influyen en cómo se adaptan los controles de la barra de comandos a varios tamaños de cinta en tiempo de ejecución.

-   [Introducción](#introduction)
    -   [Tamaño de la cinta Plantillas de definición](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [Plantillas personalizadas](#custom-templates)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

El diseño adaptable, tal como se define en el marco de la cinta de opciones, es la capacidad de todos los controles dentro de la interfaz de usuario de la cinta de opciones de ajustar dinámicamente su organización, tamaño, formato y escala relativa en función de los cambios en el tamaño de la cinta en tiempo de ejecución.

El marco expone la funcionalidad de diseño adaptable a través de un conjunto de elementos de marcado dedicados a especificar y personalizar varios comportamientos de diseño. El marco define una colección de plantillas, [**denominada SizeDefinitions,**](windowsribbon-element-sizedefinition.md)cada una de las cuales admite varios escenarios de control y diseño. Sin embargo, el marco también admite plantillas personalizadas si las plantillas predefinidas no proporcionan la experiencia de interfaz de usuario o los diseños que requiere una aplicación.

Para mostrar los controles en un diseño preferido con un tamaño de cinta determinado, tanto las plantillas predefinidas como las personalizadas funcionan junto con el [**elemento ScalingPolicy.**](windowsribbon-element-scalingpolicy.md) Este elemento contiene un manifiesto de preferencias de tamaño que el marco usa como guía al representar la cinta de opciones.

> [!Note]  
> El marco de la cinta de opciones proporciona comportamientos de diseño predeterminados basados en un conjunto de heurística integrada para la organización y la presentación de controles en tiempo de ejecución sin necesidad de las plantillas [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefinidas. Sin embargo, esta funcionalidad está pensada solo con fines de creación de prototipos.

 

### <a name="ribbon-sizedefinition-templates"></a>Tamaño de la cinta Plantillas de definición

El marco de la cinta de opciones proporciona un conjunto completo de [**plantillas SizeDefinition**](windowsribbon-element-sizedefinition.md) que especifican el comportamiento de tamaño y diseño para [un grupo de controles](windowsribbon-controls-group.md) de cinta de opciones. Estas plantillas cubren los escenarios más comunes para organizar controles en una aplicación de cinta de opciones.

Para aplicar una experiencia de usuario coherente en las aplicaciones de la cinta de opciones, cada plantilla [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impone restricciones en los controles o en la familia de controles que admite.

Por ejemplo, la familia de botones de controles incluye:

-   [Botón](windowsribbon-controls-button.md)
-   [Botón De alternancia](windowsribbon-controls-togglebutton.md)
-   [Botón desplegable](windowsribbon-controls-dropdownbutton.md)
-   [Botón Dividir](windowsribbon-controls-splitbutton.md)
-   [Galería desplegable](windowsribbon-controls-dropdowngallery.md)
-   [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md)
-   [Lista desplegable Selector de colores](windowsribbon-controls-dropdowncolorpicker.md)

Mientras que la familia de entrada de controles incluye:

-   [Cuadro combinado](windowsribbon-controls-combobox.md)
-   [Spinner](windowsribbon-controls-spinner.md)

[Las casillas](windowsribbon-controls-checkbox.md) [y la Galería de la](windowsribbon-controls-inribbongallery.md) cinta de opciones no pertenecen a la familia de botones ni a la familia de entrada. Estos dos controles solo se pueden usar cuando se indica explícitamente en una [**plantilla SizeDefinition.**](windowsribbon-element-sizedefinition.md)

A continuación se muestra una lista de las [**plantillas SizeDefinition**](windowsribbon-element-sizedefinition.md) con una descripción del diseño y los controles permitidos por cada plantilla.

> [!IMPORTANT]
> Si los controles declarados en el marcado no se asignan exactamente al tipo de control, orden [](windowsribbon-intentcl.md) y cantidad definidos en la plantilla asociada, el compilador de marcado registra un [error](windowsribbon-compilationerrors.md) de validación y finaliza la compilación.

 



Onebutton

Un control de familia de botones.<br/> Solo se admite el tamaño de grupo grande.<br/>

![imagen de la plantilla sizedefinition de un botón.](images/overviews/sizedefinition-onebutton.png)

TwoButtons

Dos controles de familia de botones.<br/> Solo se admiten tamaños de grupo grandes y medianos.<br/>

![imagen de la plantilla sizedefinition de dos botones de gran tamaño.](images/overviews/sizedefinition-twobuttons-large.png)

![imagen de la plantilla twobuttons medium sizedefinition.](images/overviews/sizedefinition-twobuttons-medium.png)

ThreeButtons

Tres controles de familia de botones.<br/> Solo se admiten tamaños de grupo grandes y medianos.<br/>

![imagen de la plantilla sizedefinition de tres botones de gran tamaño.](images/overviews/sizedefinition-threebuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de tres botones.](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

Tres controles de familia de botones.<br/> El primer botón se presenta de forma destacada en los tres tamaños.<br/>

![imagen de la plantilla threebuttons-onebigandtwosmall large sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![imagen de la plantilla threebuttons-onebigandtwosmall medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![imagen de la plantilla threebuttons-onebigandtwosmall small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

ThreeButtonsAndOneCheckBox

Tres controles de familia de botones acompañados de un único control CheckBox.<br/> Solo se admiten tamaños de grupo grandes y medianos.<br/>

![imagen de la plantilla threebuttonsandonecheckbox large sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![imagen de la plantilla threebuttonsandonecheckbox medium sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

FourButtons

Cuatro controles de familia de botones.<br/>

![imagen de la plantilla de definición de tamaño grande de cuatro botones.](images/overviews/sizedefinition-fourbuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de cuatro botones.](images/overviews/sizedefinition-fourbuttons-medium.png)

![imagen de la plantilla sizedefinition de cuatro botones pequeños.](images/overviews/sizedefinition-fourbuttons-small.png)

FiveButtons

Cinco controles de familia de botones.<br/>

![imagen de la plantilla de definición de tamaño grande de cinco botones.](images/overviews/sizedefinition-fivebuttons-large.png)

![imagen de la plantilla fivebuttons medium sizedefinition.](images/overviews/sizedefinition-fivebuttons-medium.png)

![imagen de la plantilla small sizedefinition de cinco botones.](images/overviews/sizedefinition-fivebuttons-small.png)

FiveOrSixButtons

Cinco controles de familia de botones y un sexto botón opcional.<br/>

![imagen de la plantilla fiveorsixbuttons large sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![imagen de la plantilla fiveorsixbuttons medium sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![imagen de la plantilla small sizedefinition de fiveorsixbuttons.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

SixButtons

Seis controles de familia de botones.<br/>

![imagen de la plantilla de definición de tamaño grande de seis botones.](images/overviews/sizedefinition-sixbuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de seis botones.](images/overviews/sizedefinition-sixbuttons-medium.png)

![imagen de la plantilla small sizedefinition de seis botones.](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

Seis controles de familia de botones (presentación alternativa).<br/>

![imagen de la plantilla de definición de tamaño grande sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![plantilla sixbuttons-twocolumns medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![imagen de la plantilla small sizedefinition de sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

SevenButtons

Siete controles de familia de botones.<br/>

![imagen de la plantilla de definición de tamaño grande de siete botones.](images/overviews/sizedefinition-sevenbuttons-large.png)

![imagen de la plantilla mediumsizedefinition de siete botones.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![imagen de la plantilla small sizedefinition de siete botones.](images/overviews/sizedefinition-sevenbuttons-small.png)

EightButtons

Ocho controles de familia de botones.<br/>

![imagen de la plantilla eightbuttons-lastthreesmall large sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![imagen de la plantilla eightbuttons-lastthreesmall medium sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![imagen de la plantilla eightbuttons-lastthreesmall small sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

Ocho controles de familia de botones (presentación alternativa).<br/>

> [!Note]  
> Todos los elementos de control declarados con esta plantilla deben estar contenidos en dos [**elementos ControlGroup:**](windowsribbon-element-controlgroup.md) uno para los cinco primeros elementos y otro para los tres últimos elementos.

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



![imagen de la plantilla sizedefinition de ocho botones de gran tamaño.](images/overviews/sizedefinition-eightbuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de ocho botones.](images/overviews/sizedefinition-eightbuttons-medium.png)

![imagen de la plantilla small sizedefinition de ocho botones.](images/overviews/sizedefinition-eightbuttons-small.png)

NineButtons

Nueve controles de familia de botones.

![imagen de la plantilla de definición de tamaño grande de ninebuttons.](images/overviews/sizedefinition-ninebuttons-large.png)

![imagen de la plantilla ninebuttons medium sizedefinition.](images/overviews/sizedefinition-ninebuttons-medium.png)

![imagen de la plantilla small sizedefinition de ninebuttons.](images/overviews/sizedefinition-ninebuttons-small.png)

TenButtons

Diez controles de familia de botones.

![imagen de la plantilla de definición de tamaño grande de los botones de diez botones.](images/overviews/sizedefinition-tenbuttons-large.png)

![imagen de la plantilla tenbuttons medium sizedefinition.](images/overviews/sizedefinition-tenbuttons-medium.png)

![imagen de la plantilla small sizedefinition de tenbuttons.](images/overviews/sizedefinition-tenbuttons-small.png)

OnceButtons

Once controles de familia de botones.

![imagen de la plantilla de definición de tamaño grande de once botones.](images/overviews/sizedefinition-elevenbuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de once botones.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![imagen de la plantilla small sizedefinition de once botones.](images/overviews/sizedefinition-elevenbuttons-small.png)

OneFontControl

Un [**FontControl**](windowsribbon-element-fontcontrol.md).

Solo se admiten tamaños de grupo grandes y medianos.

> [!IMPORTANT]
> El marco de trabajo no admite la inclusión de [**un FontControl**](windowsribbon-element-fontcontrol.md) dentro de una definición de plantilla personalizada.

 

![imagen de una plantilla de definición de tamaño grande de onefontcontrol.](images/overviews/sizedefinition-onefontcontrol-large.png)

![imagen de una plantilla de definición de tamaño medio de onefontcontrol.](images/overviews/sizedefinition-onefontcontrol-medium.png)

OneInRibbonGallery

Un [**control InRibbonGallery.**](windowsribbon-element-inribbongallery.md)

Solo se admiten los tamaños de grupo grande y pequeño.

![imagen de una plantilla de definición de tamaño grande de oneinribbongallery.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![imagen de una plantilla de definición de tamaño pequeño de oneinribbongallery.](images/overviews/sizedefinition-oneinribbongallery-small.png)

InRibbonGalleryAndBigButton

Un [**control InRibbonGallery**](windowsribbon-element-inribbongallery.md) y un control de familia de botones.

Solo se admiten los tamaños de grupo grande y pequeño.

![imagen de la plantilla inribbongalleryandbigbutton large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![imagen de la plantilla inribbongalleryandbigbutton small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

Un [control de la Galería en la cinta de](windowsribbon-controls-inribbongallery.md) opciones y dos o tres controles de familia de botones.

La galería se contrae en la representación Popup en tamaños de grupo Mediano y Pequeño.

![imagen de inribbongalleryandbuttons-galleryscalesfirst large sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![imagen de inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![imagen de inribbongalleryandbuttons-galleryscalesfirst small sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

ButtonGroups

Una disposición compleja de 32 controles de familia de botones (la mayoría de los cuales son opcionales).

> [!Note]  
> Además del botón de tamaño completo opcional de la plantilla ButtonGroups grande, todos los elementos de control declarados con esta plantilla deben estar incluidos en [**los elementos ControlGroup.**](windowsribbon-element-controlgroup.md)

 

En el ejemplo siguiente se muestra el marcado necesario para mostrar los 32 elementos de control (obligatorios y opcionales) con esta plantilla.


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



![imagen de la plantilla sizedefinition de grupos de botones de gran tamaño.](images/overviews/sizedefinition-buttongroups-large.png)

![imagen de la plantilla de definición de tamaño medio de los grupos de botones.](images/overviews/sizedefinition-buttongroups-medium.png)

![imagen de la plantilla small sizedefinition de grupos de botones.](images/overviews/sizedefinition-buttongroups-small.png)

ButtonGroupsAndInputs

Dos controles de familia de entrada (el segundo es opcional) seguidos de una compleja disposición de 29 controles de familia de botones (la mayoría de los cuales son opcionales).

Solo se admiten tamaños de grupo grandes y medianos.

> [!Note]  
> Todos los elementos de control declarados con esta plantilla deben estar incluidos en [**los elementos ControlGroup.**](windowsribbon-element-controlgroup.md)

 

En el ejemplo siguiente se muestra el marcado necesario para mostrar todos los elementos de control (obligatorios y opcionales) con esta plantilla.


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



![imagen de la plantilla buttongroupsandinputs large sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![imagen de la plantilla buttongroupsandinputs medium sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

BigButtonsAndSmallButtonsOrInputs

Dos controles de familia de botones (ambos opcionales) seguidos de dos o tres controles de botón o familia de entrada.

Solo se admiten tamaños de grupo grandes y medianos.

![imagen de la plantilla bigbuttonsandsmallbuttonsorinputs large sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![imagen de la plantilla bigbuttonsandsmallbuttonsorinputs medium sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>Ejemplo de SizeDefinition básico

En el ejemplo de código siguiente se proporciona una demostración básica de cómo declarar una [**plantilla SizeDefinition**](windowsribbon-element-sizedefinition.md) en el marcado de la cinta de opciones.

*OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) se usa para este ejemplo en particular, pero todas las plantillas de marco se especifican de forma similar.


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

El comportamiento de con contraer las plantillas [**SizeDefinition**](windowsribbon-element-sizedefinition.md) se puede controlar mediante el uso de directivas de escalado en el marcado de la cinta de opciones.

El [**elemento ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contiene un manifiesto de declaraciones [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) y [**Scale**](windowsribbon-element-scale.md) que especifican preferencias de diseño adaptable para uno o varios elementos [**Group**](windowsribbon-element-group.md) cuando se cambia el tamaño de la cinta.

> [!Note]  
> Se recomienda encarecidamente que se especifiquen los detalles adecuados de la directiva de escalado de forma que la mayoría de los elementos [**Group,**](windowsribbon-element-group.md) si no todos, estén asociados a un elemento [**Scale**](windowsribbon-element-scale.md) donde el atributo *Size* sea igual a `Popup` . Esto permite que el marco represente la cinta de opciones con el menor tamaño posible y admita la gama más amplia de dispositivos de visualización, antes de introducir automáticamente un mecanismo de desplazamiento.

 

En el ejemplo de código siguiente se muestra un [**manifiesto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) que especifica una preferencia [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de los cuatro grupos de controles de una **pestaña** Inicio. Además, los [**elementos Scale**](windowsribbon-element-scale.md) se especifican para influir en el comportamiento de conserción, en orden descendente de tamaño, de cada grupo.


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

Si los comportamientos de diseño predeterminados y las plantillas [**de SizeDefinition**](windowsribbon-element-sizedefinition.md) predefinidas no ofrecen la flexibilidad o compatibilidad con un escenario de diseño determinado, el marco de la cinta de opciones admite las plantillas personalizadas a través del elemento [**Ribbon.SizeDefinitions.**](windowsribbon-element-ribbon-sizedefinitions.md)

Las plantillas personalizadas se pueden declarar de dos maneras: un método independiente mediante el elemento [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) para declarar plantillas reutilizables con nombre o un método en línea específico de [**Group.**](windowsribbon-element-group.md)

### <a name="standalone-template"></a>Plantilla independiente

En el ejemplo de código siguiente se muestra una plantilla personalizada básica y reutilizable.


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



### <a name="inline-template"></a>Plantilla inserta

En los ejemplos de código siguientes se muestra una plantilla personalizada en línea básica para un grupo de cuatro botones.

En esta sección de código se muestran las declaraciones command de un grupo de botones. Aquí también se especifican recursos de imagen grandes y pequeños.


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



En esta sección de código se muestra cómo definir plantillas [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) grandes, medianas y pequeñas para mostrar los cuatro botones en distintos tamaños y diseños. La [**declaración ScalingPolicy**](windowsribbon-element-scalingpolicy.md) de la pestaña define qué plantilla se usa para un grupo de controles en función del tamaño y el espacio de la cinta de opciones requeridos por la pestaña activa.


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



En las imágenes siguientes se muestra cómo se aplican las plantillas del ejemplo anterior a la interfaz de usuario de la cinta de opciones para dar cabida a una disminución del tamaño de la cinta.



|  Tipo  |      Imagen                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| grande  | ![imagen de una plantilla personalizada grande insertda.](images/overviews/sizedefinition-custom-large.png)   |
| Media | ![imagen de una plantilla personalizada mediana insertda.](images/overviews/sizedefinition-custom-medium.png) |
| Pequeña  | ![imagen de una plantilla personalizada pequeña insertda.](images/overviews/sizedefinition-custom-small.png)   |
| Popup  | ![imagen de una plantilla personalizada emergente insertda.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**SizeDefinition**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**Escala**](windowsribbon-element-scale.md)
</dt> <dt>

[**Group (Grupo)**](windowsribbon-element-group.md)
</dt> </dl>

 

 





