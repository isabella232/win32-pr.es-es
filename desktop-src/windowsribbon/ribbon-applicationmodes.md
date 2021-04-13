---
title: Volver a configurar la cinta de opciones con modos de aplicación
description: El marco de la cinta de opciones de Windows admite la reconfiguración dinámica y la exposición de elementos básicos de la interfaz de usuario de la cinta de opciones en tiempo de ejecución, en función del estado de la aplicación (también conocido como contexto).
ms.assetid: 8e9d85c5-33e4-4212-b9e4-2fc3b492c273
keywords:
- Cinta de Windows, volver a configurar con modos de aplicación
- Cinta de opciones, reconfigurar con modos de aplicación
- volver a configurar la cinta de opciones de Windows con modos de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d206c238e6fe7463562077daaa52a5522a79d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420731"
---
# <a name="reconfiguring-the-ribbon-with-application-modes"></a>Volver a configurar la cinta de opciones con modos de aplicación

El marco de la cinta de opciones de Windows admite la reconfiguración dinámica y la exposición de elementos básicos de la interfaz de usuario de la cinta de opciones en tiempo de ejecución, en función del estado de la aplicación (también conocido como contexto). Declarado y asociado con elementos específicos en el marcado, los distintos Estados admitidos por una aplicación se conocen como modos de aplicación.

-   [Introducción](#introduction)
-   [Interfaz de usuario contextual](#contextual-user-interface)
    -   [Un escenario de modo de aplicación simple](#a-simple-application-mode-scenario)
-   [Implementar modos de aplicación](#implementing-application-modes)
    -   [Identificar los modos](#identify-the-modes)
    -   [Asignación de controles a los modos de aplicación](#assign-controls-to-application-modes)
    -   [Cambiar los modos en tiempo de ejecución](#switch-modes-at-runtime)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Los modos de aplicación constan de grupos lógicos de controles que exponen alguna funcionalidad básica de la aplicación en la interfaz de usuario de la cinta. La aplicación habilita o deshabilita dinámicamente estos modos a través de una llamada al método de marco [**IUIFramework:: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes), que activa o desactiva la visibilidad de uno o más modos de aplicación.

## <a name="contextual-user-interface"></a>Interfaz de usuario contextual

El marco de la cinta de opciones proporciona una experiencia de usuario enriquecida al incorporar controles dinámicos que responden sin problemas a la interacción del usuario y al contexto de la aplicación. Esta interfaz de usuario contextual enriquecida se entrega a través de una combinación de los siguientes mecanismos:

-   Galerías: controles basados en colección que admiten la manipulación dinámica de sus colecciones de elementos.
-   Pestañas contextuales: pestañas de la cinta de opciones que tienen su visibilidad determinada por un cambio en el contexto del área de trabajo, como la selección de una imagen de un documento.
-   Modos de aplicación: funcionalidad básica de la aplicación que depende del contexto de la aplicación.

En algunos aspectos, los modos de aplicación parecen funcionalmente similares a las pestañas contextuales. Sin embargo, la distinción fundamental radica en la intención y el ámbito de cada uno.

Los controles contextuales se activan en respuesta a un cambio de contexto dentro de una aplicación. Por ejemplo, en Microsoft Paint para Windows 7, se muestra una pestaña contextual que contiene grupos de comandos relacionados con el texto cuando un usuario inserta un área de texto en el área de trabajo. Esta pestaña contextual no contiene comandos básicos para la aplicación y solo se expone en la interfaz de usuario porque el contexto *dentro* de la aplicación ha cambiado. La funcionalidad básica de la aplicación (los comandos de edición de imágenes) sigue siendo relevante y está disponible para el usuario, incluso con la pestaña contextual visible.

Los modos de aplicación se diferencian de los controles contextuales en que reconfiguran la funcionalidad en respuesta a los cambios en el contexto en el que funciona la aplicación. Los modos de aplicación se encuentran en un nivel más alto de abstracción; proporcionan una manera de volver a configurar la funcionalidad básica de una aplicación en lugar de exponer temporalmente la funcionalidad que no es un componente básico de la interfaz de usuario. Por ejemplo, en Microsoft Paint para Windows 7, se produce un cambio en el modo de aplicación cuando se invoca el comando de **vista previa de impresión** . Cuando Microsoft Paint cambia a la **vista previa de impresión**, el contexto en el que funciona la aplicación cambia de edición a vista previa. Como resultado, la funcionalidad básica de la aplicación cambia hasta que se cancela la **vista previa de impresión** y la aplicación vuelve a entrar en el contexto de edición.

### <a name="a-simple-application-mode-scenario"></a>Un escenario de modo de aplicación simple

En el escenario siguiente se muestra cómo se usan los modos de aplicación, en una aplicación denominada RibbonApp, para exponer aspectos discretos de la funcionalidad básica.

Dos modos de aplicación se definen en RibbonApp:

-   El modo **simple** expone comandos básicos a través de la interfaz de usuario de la cinta de opciones. Estos comandos aparecen en todo momento, independientemente del modo de aplicación que esté activo.
-   El modo **avanzado** expone comandos complejos destinados a usuarios expertos de la aplicación. Estos comandos avanzados aparecen en la interfaz de usuario de la cinta de opciones, además de los comandos sencillos.

De forma predeterminada, RibbonApp se establece en abierto en modo **simple** y los comandos que requieren los usuarios inexpertos se muestran en el **menú aplicación** y en la pestaña **Inicio** . Las capturas de pantalla siguientes muestran el menú de la **aplicación** RibbonApp y la pestaña **Inicio** en el modo **simple** , resaltando los controles modales.

![captura de pantalla que muestra una pestaña para el modo de aplicación simple.](images/overviews/appmode-hometab.png)![captura de pantalla que muestra el menú de la aplicación para el modo de aplicación simple.](images/overviews/appmode-simpleappmenu.png)

Aunque estos comandos pueden ser suficientes para usuarios inexpertos, el RibbonApp también admite usuarios expertos a través de un modo **avanzado** que, cuando se activa haciendo clic en el botón **cambiar a modo avanzado** en el **menú aplicación**, muestra la funcionalidad básica adicional.

Este escenario se implementa fácilmente mediante el enlace de varios elementos en el marcado a modos de aplicación discretos que se pueden activar y desactivar según sea necesario. Las capturas de pantalla siguientes muestran el menú de la **aplicación** RibbonApp y la pestaña **Inicio** en modo **avanzado** , resaltando los controles modales.

![captura de pantalla que muestra una pestaña para el modo de aplicación avanzada.](images/overviews/appmode-advancedtab.png)![captura de pantalla que muestra el menú de la aplicación para el modo de aplicación avanzada.](images/overviews/appmode-advancedappmenu.png)

## <a name="implementing-application-modes"></a>Implementar modos de aplicación

En esta sección se describen los tres pasos que suelen ser necesarios para la implementación de los modos de aplicación del marco de cinta. RibbonApp se utiliza para proporcionar un ejemplo de cada paso.

### <a name="identify-the-modes"></a>Identificar los modos

Cada modo de una aplicación debe representar un conjunto lógico de funcionalidad que depende del contexto en el que una aplicación puede operar. Por ejemplo, si una aplicación muestra controles que solo son relevantes cuando se detecta una conexión de red, esos controles funcionan en un contexto de red que podría justificar la creación de un modo de **red** .

RibbonApp tiene dos contextos que pueden estar activos en un momento dado: **simples** y **avanzados**. Por lo tanto, RibbonApp requiere dos modos: **simple** y **avanzado**.

### <a name="assign-controls-to-application-modes"></a>Asignación de controles a los modos de aplicación

Una vez identificados los modos de aplicación, asigne cada control de la cinta de opciones a un modo declarando un atributo *ApplicationModes* en el marcado para los elementos de control que admiten los modos de aplicación.

La vista de cinta permite especificar los modos en los siguientes elementos de control:

-   Elementos de [**ficha**](windowsribbon-element-tab.md) principales.
-   Elementos de [**Grupo**](windowsribbon-element-group.md) que son elementos secundarios de un elemento de [**ficha**](windowsribbon-element-tab.md) principal.
-   Elementos [**Button**](windowsribbon-element-button.md), [**splitButton**](windowsribbon-element-splitbutton.md)y [**DropDownButton**](windowsribbon-element-dropdownbutton.md) asignados a un [**MenuGroup**](windowsribbon-element-menugroup.md) en el [menú](windowsribbon-controls-applicationmenu.md)de la aplicación.
    > [!Note]  
    > Los elementos [**Button**](windowsribbon-element-button.md), [**splitButton**](windowsribbon-element-splitbutton.md)y [**DropDownButton**](windowsribbon-element-dropdownbutton.md) no se pueden asignar a un modo a menos que se hospeden en el menú de la [aplicación](windowsribbon-controls-applicationmenu.md).

     

En el marco de la cinta de opciones, estos elementos de control se conocen como controles modales. Solo aparecen si un modo al que están enlazados está activo en la interfaz de usuario.

Los elementos de control contenidos dentro de un control modal heredan el comportamiento del modo de aplicación. Por ejemplo, si un control modal de [**Grupo**](windowsribbon-element-group.md) se asigna a un modo **avanzado** y el modo **Avanzado** no está activo, el **Grupo** y los controles que contenga, modal o de otro tipo, no estarán visibles en la interfaz de usuario de la cinta de opciones.

Con el uso del atributo *ApplicationModes* , los modos se asignan a los controles modales en una relación 1: N (uno a varios), donde un solo control modal puede asociarse a varios modos.

El marco de la cinta de opciones hace referencia a los modos numéricamente, de 0 a 31, con el modo 0 considerado el modo predeterminado que se activa automáticamente cuando se inicia una aplicación de la cinta de opciones. Cualquier control modal que no especifique un atributo *ApplicationModes* se considera un miembro del modo predeterminado.

En RibbonApp, **simple** es el modo predeterminado, con la funcionalidad de modo **avanzado** que solo se muestra cuando lo inicia el usuario.

En el ejemplo siguiente se muestra el marcado necesario para RibbonApp.


```C++
<Application.Views>
  <Ribbon>

    <!--Application Menu-->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName='cmdAppMenu'>                    
        <MenuGroup>
          <Button CommandName='cmdSave'/>                        
          <Button CommandName='cmdExportMetadata' ApplicationModes='1'/>                   
        </MenuGroup>              
        <MenuGroup>
          <Button CommandName='cmdSwitchModes' ApplicationModes ='0,1'/>
          <Button CommandName='cmdExit'/>
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
            
    <!--Tabs-->
    <Ribbon.Tabs>
      <!--Home Tab-->
      <Tab CommandName='cmdHomeTab'>
                    
        <!--Scaling Policy for Home tab-->
        <Tab.ScalingPolicy>
          <ScalingPolicy>
            <ScalingPolicy.IdealSizes>
              <Scale Group='cmdSimpleControlsGroup' Size='Medium'/>                                
            </ScalingPolicy.IdealSizes>                     
          </ScalingPolicy>
        </Tab.ScalingPolicy>     
                    
        <!--Simple Controls Group-->
        <Group CommandName='cmdSimpleControlsGroup' SizeDefinition='ThreeButtons-OneBigAndTwoSmall'>                        
          <Button CommandName="cmdPaste" />
          <Button CommandName='cmdCut'/>                        
          <Button CommandName='cmdCopy'/>                        
        </Group>
      </Tab>
                
      <!--Advanced Tab-->
      <Tab CommandName='cmdAdvancedTab' ApplicationModes='1'>
        <!--Advanced Controls Group-->
        <Group CommandName='cmdMetadataGroup' ApplicationModes='1' SizeDefinition='TwoButtons'>
          <Button CommandName='cmdEditMetadata' />
          <Button CommandName='cmdCheckErrors' />
        </Group>
      </Tab>
    </Ribbon.Tabs>                   
                             
  </Ribbon>         
</Application.Views>
```



En este ejemplo se muestra lo siguiente:

-   No es necesario declarar explícitamente el modo predeterminado 0. Dado que los controles modales que no especifican el atributo *ApplicationModes* se enlazan automáticamente al modo 0 (modo **simple** en el ejemplo RibbonApp), no es necesario declarar explícitamente el atributo para los controles modales predeterminados.
-   Los controles se pueden enlazar a varios modos. En el caso de RibbonApp, la única necesidad del atributo *ApplicationModes* en un control de modo **simple** es el `cmdSwitchModes` botón, ya que forma parte de los modos **simple** y **avanzado** . Si alguno de los modos está activo, este control aparecerá en el menú de la [aplicación](windowsribbon-controls-applicationmenu.md).
-   Los controles modales no heredan de sus elementos primarios. La pestaña **Opciones avanzadas** de RibbonApp contiene un grupo de **metadatos** . ambos controles modales se asignan al modo 1 (modo **avanzado** ). Al asignar la pestaña **Opciones avanzadas** al modo 1, no se asignan automáticamente los controles secundarios, como el grupo de **metadatos** , al modo 1. Esto permite que todos los grupos de una pestaña estén habilitados o deshabilitados de forma independiente en tiempo de ejecución.
-   Los controles no modales todavía pueden confiar en los modificadores de modo. Los botones **editar metadatos** y **comprobar errores** de RibbonApp son para usuarios avanzados y solo están disponibles cuando el usuario cambia al modo **avanzado** . Los controles de botón que no se hospedan dentro del menú de la [aplicación](windowsribbon-controls-applicationmenu.md) no son modales; sin embargo, dado que estos botones se hospedan en un control modal (el grupo de **metadatos** ), son visibles cuando el grupo está visible. Por lo tanto, estos botones aparecen cuando se activa el modo avanzado y el grupo de **metadatos** se expone en la interfaz de usuario de la cinta.

### <a name="switch-modes-at-runtime"></a>Cambiar los modos en tiempo de ejecución

Después de definir los modos en el marcado, se pueden habilitar o deshabilitar con facilidad en respuesta a los eventos contextuales. Como se mencionó anteriormente, las aplicaciones de la cinta de opciones siempre se inician en el modo predeterminado 0. Una vez que la aplicación se ha inicializado y el modo 0 está activo, se puede cambiar el conjunto de modos activos llamando a la función [**IUIFramework:: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) . Esta función toma un entero de 32 bits como una representación bit a bit de los modos que deben estar activos; el bit menos significativo representa el modo 0 y el bit más significativo representa el modo 31. Si un bit se establece en cero, el modo no está activo en la interfaz de usuario de la cinta de opciones.

En RibbonApp, cuando un usuario habilita el modo **avanzado** , los comandos avanzados se muestran junto con los comandos sencillos. El controlador de comandos del botón **cambiar a modo avanzado** llama a [**IUIFramework:: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) para establecer los modos 0 (**simple**) y 1 (**avanzado**) como activo en la interfaz de usuario. El ejemplo siguiente es el código de RibbonApp para esta llamada de función:


```C++
const int SIMPLE_MODE = 0;
const int ADVANCED_MODE = 1;
pFramework->SetModes( UI_MAKEAPPMODE(SIMPLE_MODE) | UI_MAKEAPPMODE(ADVANCED_MODE) );
```



> [!Note]  
> La macro MAKEAPPMODE de la interfaz de usuario del marco de cinta \_ simplifica la tarea de establecer estos bits correctamente como preparación para la llamada a [**IUIFramework:: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes).

 

En este ejemplo se muestra lo siguiente:

-   Use la macro MAKEAPPMODE de la interfaz \_ de usuario para crear un conjunto de modos.
-   Los modos se establecen de forma explícita y atómica. El valor entero que se pasa a [**IUIFramework:: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) representa los modos que estarán activos después de que se devuelva la función. Aunque el modo **simple** estaba activo anteriormente, **IUIFramework:: SetModes** debe indicar que el modo **simple** permanece activo cuando se activa el modo **avanzado** .
-   Se puede quitar el modo predeterminado. Aunque en RibbonApp no se quita nunca el modo predeterminado (modo 0), se puede quitar con la siguiente llamada: `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))` , exponiendo solo los comandos avanzados en la interfaz de usuario.

> [!Note]  
> Cuando se reconfiguran los modos de una aplicación, la cinta de opciones intentará conservar la pestaña seleccionada anteriormente en la interfaz de usuario. Si el nuevo conjunto de modos ya no contiene la pestaña seleccionada antes de la llamada, la cinta de opciones seleccionará la pestaña en su diseño más cercano al menú de la [aplicación](windowsribbon-controls-applicationmenu.md). Esta pestaña está diseñada para contener los comandos que son más relevantes para el usuario. Para obtener más información, vea [directrices de la experiencia del usuario de la cinta](https://msdn.microsoft.com/library/cc872782.aspx).

 

## <a name="remarks"></a>Observaciones

La cinta de opciones debe tener al menos un modo activo en todo momento. Si una aplicación intenta desactivar todos los modos mediante una llamada a [**IUIFramework:: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) con un valor de modo de 0, \_ se devuelve un error y el conjunto de modo activo permanece inalterado.

El marco de trabajo requiere que exista al menos una pestaña en la interfaz de usuario de la cinta de opciones en todo momento. Como resultado, debe haber al menos una pestaña expuesta por el modo predeterminado (modo 0) y después de cada cambio de modo.

No todas las áreas de la interfaz de usuario de la cinta de opciones se ven afectadas por los modos de aplicación. Por ejemplo, si al deshabilitar un modo se produce la desaparición de los botones de la cinta de opciones que se agregaron previamente a la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md), dichos botones permanecen en la barra de herramientas de acceso rápido, lo que permite a los usuarios ejecutar los comandos enlazados a los botones. Como norma general, si un comando pertenece a uno o varios modos inactivos, ese comando también debe deshabilitarse estableciendo la propiedad [ \_ PKEY \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md) de la interfaz de usuario en 0 (variante \_ false).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones para la experiencia del usuario en cinta](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Mostrar pestañas contextuales](ribbon-contextualtabs.md)
</dt> </dl>

 

 