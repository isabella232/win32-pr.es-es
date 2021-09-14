---
title: Reconfiguración de la cinta con modos de aplicación
description: El marco Windows Ribbon admite la reconfiguración dinámica y la exposición de elementos principales de la interfaz de usuario de la cinta en tiempo de ejecución, en función del estado de la aplicación (también denominado contexto).
ms.assetid: 8e9d85c5-33e4-4212-b9e4-2fc3b492c273
keywords:
- Windows Cinta de opciones, reconfiguración con modos de aplicación
- Cinta de opciones, reconfiguración con modos de aplicación
- volver a configurar Windows cinta de opciones con modos de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d206c238e6fe7463562077daaa52a5522a79d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247503"
---
# <a name="reconfiguring-the-ribbon-with-application-modes"></a>Reconfiguración de la cinta con modos de aplicación

El marco Windows Ribbon admite la reconfiguración dinámica y la exposición de elementos principales de la interfaz de usuario de la cinta en tiempo de ejecución, en función del estado de la aplicación (también denominado contexto). Declarados y asociados a elementos específicos en el marcado, los distintos estados admitidos por una aplicación se conocen como modos de aplicación.

-   [Introducción](#introduction)
-   [Contexto Interfaz de usuario](#contextual-user-interface)
    -   [Un escenario de modo de aplicación simple](#a-simple-application-mode-scenario)
-   [Implementación de modos de aplicación](#implementing-application-modes)
    -   [Identificar los modos](#identify-the-modes)
    -   [Asignar controles a modos de aplicación](#assign-controls-to-application-modes)
    -   [Cambiar modos en tiempo de ejecución](#switch-modes-at-runtime)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Los modos de aplicación constan de grupos lógicos de controles que exponen algunas funcionalidades principales de la aplicación en la interfaz de usuario de la cinta de opciones. La aplicación habilita o deshabilita dinámicamente estos modos mediante una llamada al método del marco [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes), lo que activa o desactiva la visibilidad de uno o varios modos de aplicación.

## <a name="contextual-user-interface"></a>Contexto Interfaz de usuario

El marco de la cinta de opciones proporciona una experiencia de usuario enriquecida mediante la incorporación de controles dinámicos que responden sin problemas a la interacción del usuario y al contexto de la aplicación. Esta interfaz de usuario contextual enriquecte se entrega a través de una combinación de los siguientes mecanismos:

-   Galerías: controles basados en colecciones que admiten la manipulación dinámica de sus colecciones de elementos.
-   Pestañas contextuales: pestañas de la cinta que tienen su visibilidad determinada por un cambio en el contexto del área de trabajo, como la selección de una imagen en un documento.
-   Modos de aplicación: funcionalidad de aplicación principal que depende del contexto de la aplicación.

En algunos aspectos, los modos de aplicación parecen funcionalmente similares a las pestañas contextuales. Sin embargo, la distinción fundamental reside en la intención y el ámbito de cada uno.

Los controles contextuales se activan en respuesta a un cambio de contexto dentro de una aplicación. Por ejemplo, en Microsoft Paint para Windows 7, se muestra una pestaña contextual que contiene grupos de comandos relacionados con texto cuando un usuario inserta un área de texto en el área de trabajo. Esta pestaña contextual no contiene comandos principales para la aplicación y solo se expone en la interfaz de usuario porque el contexto *dentro* de la aplicación ha cambiado. La funcionalidad principal de la aplicación (los comandos de edición de imágenes) sigue siendo pertinente y está disponible para el usuario, incluso con la pestaña contextual visible.

Los modos de aplicación difieren de los controles contextuales en que reconfiguran la funcionalidad en respuesta a los cambios en el contexto en el que funciona la aplicación. Los modos de aplicación están en un nivel superior de abstracción; proporcionan una manera de volver a configurar la funcionalidad principal de una aplicación en lugar de exponer temporalmente la funcionalidad que no es un componente básico de la interfaz de usuario. Por ejemplo, en Microsoft Paint para Windows 7, se produce un cambio en el modo de aplicación cuando se invoca el comando **Vista** previa de impresión. Cuando Microsoft Paint cambia a Vista previa **de** impresión , el contexto en el que la aplicación funciona cambia de edición a vista previa. Como resultado, la funcionalidad principal de la aplicación cambia hasta que se cancela **la** vista previa de impresión y la aplicación vuelve a entrar en el contexto de edición.

### <a name="a-simple-application-mode-scenario"></a>Un escenario de modo de aplicación simple

En el siguiente escenario se muestra cómo se usan los modos de aplicación, en una aplicación denominada RibbonApp, para exponer aspectos discretos de la funcionalidad principal.

En RibbonApp se definen dos modos de aplicación:

-   **El modo** simple expone comandos básicos en toda la interfaz de usuario de la cinta de opciones. Estos comandos aparecen en todo momento, independientemente del modo de aplicación que esté activo.
-   **El** modo avanzado expone comandos complejos destinados a usuarios expertos de la aplicación. Estos comandos avanzados aparecen en toda la interfaz de usuario de la cinta de opciones, además de los comandos simples.

De forma predeterminada, RibbonApp está establecido en abrirse en modo **Simple** y  los comandos requeridos por los usuarios principiantes se muestran en el menú Aplicación y en la **pestaña** Inicio. En las capturas de pantalla siguientes se muestran el menú **De** la aplicación RibbonApp y la pestaña **Inicio** en modo **simple,** resaltando los controles modales.

![captura de pantalla que muestra una pestaña para el modo de aplicación simple.](images/overviews/appmode-hometab.png)![captura de pantalla que muestra el menú de la aplicación para el modo de aplicación simple.](images/overviews/appmode-simpleappmenu.png)

Aunque estos comandos pueden ser suficientes para los usuarios principiantes,  RibbonApp también admite usuarios  expertos a través de un modo avanzado que, cuando se activa al hacer clic en el botón Cambiar al modo avanzado del menú de la **aplicación,** muestra funcionalidad principal adicional.

Este escenario se implementa fácilmente enlazando varios elementos del marcado a modos de aplicación discretos que se pueden activado y desactivado según sea necesario. En las siguientes capturas de pantalla se muestran las pestañas RibbonApp **Application Menu** (Menú de la aplicación RibbonApp) **y Home** **(Inicio)** en modo Avanzado, resaltando los controles modales.

![captura de pantalla que muestra una pestaña para el modo de aplicación avanzada.](images/overviews/appmode-advancedtab.png)![captura de pantalla que muestra el menú de la aplicación para el modo de aplicación avanzada.](images/overviews/appmode-advancedappmenu.png)

## <a name="implementing-application-modes"></a>Implementación de modos de aplicación

En esta sección se describen los tres pasos que normalmente se requieren para la implementación de los modos de aplicación del marco de cinta de opciones. RibbonApp se usa para proporcionar un ejemplo para cada paso.

### <a name="identify-the-modes"></a>Identificar los modos

Cada modo de una aplicación debe representar un conjunto lógico de funcionalidades que depende del contexto en el que una aplicación pueda funcionar. Por ejemplo, si una aplicación muestra controles que solo son pertinentes cuando se detecta una conexión de red, esos controles funcionan dentro de un contexto de red que podría justificar la creación de un **modo de** red.

RibbonApp tiene dos contextos que pueden estar activos en un momento dado: **Simple** y **Advanced**. Por lo tanto, RibbonApp requiere dos modos: **Simple** y **Advanced**.

### <a name="assign-controls-to-application-modes"></a>Asignar controles a modos de aplicación

Una vez identificados los modos de aplicación, asigne cada control ribbon a un modo declarando un atributo *ApplicationModes* en el marcado para los elementos de control que admiten modos de aplicación.

La vista de la cinta de opciones permite especificar modos en los siguientes elementos de control:

-   Elementos [**De tabulación**](windowsribbon-element-tab.md) principal.
-   [**Agrupar**](windowsribbon-element-group.md) elementos que son elementos secundarios de un elemento [**Tab**](windowsribbon-element-tab.md) principal.
-   [**Elementos Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md)y [**DropDownButton**](windowsribbon-element-dropdownbutton.md) asignados a [**un elemento MenuGroup**](windowsribbon-element-menugroup.md) dentro del [menú de la aplicación.](windowsribbon-controls-applicationmenu.md)
    > [!Note]  
    > [**Los**](windowsribbon-element-button.md)elementos Button , [**SplitButton**](windowsribbon-element-splitbutton.md)y [**DropDownButton**](windowsribbon-element-dropdownbutton.md) no se pueden asignar a un modo a menos que se hospedan en el [menú de la aplicación](windowsribbon-controls-applicationmenu.md).

     

En el marco de la cinta de opciones, estos elementos de control se conocen como controles modales. Solo aparecen si un modo al que están enlazados está activo en la interfaz de usuario.

Los elementos de control contenidos dentro de un control modal heredan el comportamiento del modo de aplicación. Por ejemplo, si un control [**modal**](windowsribbon-element-group.md) Grupo se  asigna a un modo  Avanzado y el modo Avanzado no está activo, ese grupo y los controles que tenga, modales o de otro tipo, no estarán visibles en la interfaz de usuario de la cinta de opciones. 

Con el uso del atributo *ApplicationModes,* los modos se asignan a controles modales en una relación 1:N (uno a varios), donde un único control modal se puede asociar a varios modos.

El marco de la cinta de opciones hace referencia numéricamente a los modos, de 0 a 31, con el modo 0 considerado el modo predeterminado que se activa automáticamente cuando se inicia una aplicación de cinta de opciones. Cualquier control modal que no especifique un atributo *ApplicationModes* se considera miembro del modo predeterminado.

En RibbonApp, **Simple** es el modo predeterminado, con la **funcionalidad** de modo avanzado mostrada solo cuando el usuario la inicia.

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

-   No es necesario declarar explícitamente el modo predeterminado 0. Dado que los controles modales que no especifican el atributo *ApplicationModes* se enlazan automáticamente al modo 0 (modo **simple** en el ejemplo de RibbonApp), no es necesario declarar explícitamente el atributo para los controles modales predeterminados.
-   Los controles se pueden enlazar a varios modos. Para RibbonApp, la única necesidad del atributo  *ApplicationModes* en un control de modo simple es el botón , ya que forma parte de los modos `cmdSwitchModes` **Simple** **y Advanced.** Si cualquiera de los dos modo está activo, este control aparecerá en el [menú de la aplicación](windowsribbon-controls-applicationmenu.md).
-   Los controles modales no heredan de sus padres. La **pestaña Avanzadas** de RibbonApp contiene un grupo De **metadatos;** ambos controles modales se asignan al modo 1 **(modo** avanzado). La **asignación de la pestaña** Avanzadas al modo 1  no asigna automáticamente controles secundarios, como el grupo Metadatos, al modo 1. Esto permite que cualquier grupo dentro de una pestaña se habilite o deshabilite de forma independiente en tiempo de ejecución.
-   Los controles no modales pueden seguir dependiendo de los modificadores de modo. Los **botones Editar metadatos** y **Comprobar** errores de RibbonApp son para usuarios avanzados y solo están disponibles cuando el usuario cambia al **modo** Avanzado. Los controles de botón que no se hospedan en el [menú de la aplicación](windowsribbon-controls-applicationmenu.md) no son modales; sin embargo, dado que estos botones se hospedan dentro de un control modal (el grupo **Metadatos),** son visibles cuando el grupo está visible. Por lo tanto, estos botones aparecen cuando se activa el modo avanzado y el **grupo Metadatos** se expone en la interfaz de usuario de la cinta de opciones.

### <a name="switch-modes-at-runtime"></a>Cambiar modos en tiempo de ejecución

Una vez definidos los modos en el marcado, se pueden habilitar o deshabilitar fácilmente en respuesta a eventos contextuales. Como se mencionó anteriormente, las aplicaciones de cinta de opciones siempre se inician en el modo predeterminado 0. Una vez que la aplicación se ha inicializado y el modo 0 está activo, se puede cambiar el conjunto de modos activos llamando a la función [**IUIFramework::SetModes.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) Esta función toma un entero de 32 bits como una representación bit a bit de los modos que deben estar activos; el bit menos significativo representa el modo 0 y el bit más significativo representa el modo 31. Si un bit se establece en cero, el modo no está activo en la interfaz de usuario de la cinta de opciones.

En RibbonApp, cuando un usuario habilita **el modo** avanzado, los comandos avanzados se muestran junto con los comandos simples. El controlador de comandos del botón **Cambiar** al modo avanzado llama a [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) para establecer los modos 0 **(Simple)** y 1 **(Avanzado)** como activos en la interfaz de usuario. El ejemplo siguiente es el código RibbonApp para esta llamada de función :


```C++
const int SIMPLE_MODE = 0;
const int ADVANCED_MODE = 1;
pFramework->SetModes( UI_MAKEAPPMODE(SIMPLE_MODE) | UI_MAKEAPPMODE(ADVANCED_MODE) );
```



> [!Note]  
> La macro MAKEAPPMODE de la interfaz de usuario del marco de la cinta de opciones simplifica la tarea de establecer estos bits correctamente como preparación para la llamada a \_ [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes).

 

En este ejemplo se muestra lo siguiente:

-   Use la macro \_ MAKEAPPMODE de la interfaz de usuario para crear un conjunto de modos.
-   Los modos se establecen explícita y atómicamente. El valor entero que se pasa a [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) representa los modos que estarán activos después de que se devuelva la función. Aunque el modo **Simple** estaba activo anteriormente, **IUIFramework::SetModes** debe indicar  que el modo **Simple** permanece activo cuando se activa el modo Avanzado.
-   Se puede quitar el modo predeterminado. Aunque en RibbonApp el modo predeterminado (modo 0) nunca se quita, se puede quitar con la siguiente llamada: , que expone solo los comandos avanzados en la interfaz `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))` de usuario.

> [!Note]  
> Cuando se vuelvan a configurar los modos de una aplicación, la cinta de opciones intentará conservar la pestaña seleccionada anteriormente en la interfaz de usuario. Si el nuevo conjunto de modos ya no contiene la pestaña que se seleccionó antes de la llamada, la cinta de opciones seleccionará la pestaña en su diseño más cercana al [menú Aplicación](windowsribbon-controls-applicationmenu.md). Esta pestaña está pensada para contener los comandos más relevantes para el usuario. Para obtener más información, vea [Directrices de la experiencia del usuario de la cinta de opciones](https://msdn.microsoft.com/library/cc872782.aspx).

 

## <a name="remarks"></a>Observaciones

La cinta de opciones debe tener al menos un modo activo en todo momento. Si una aplicación intenta desactivar todos los modos mediante una llamada a [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) con un valor de modo de 0, se devuelve E FAIL y el conjunto de modo activo permanece \_ sin cambios.

El marco requiere que exista al menos una pestaña en la interfaz de usuario de la cinta de opciones en todo momento. Como resultado, debe haber al menos una pestaña expuesta por el modo predeterminado (modo 0) y después de cada cambio de modo.

No todas las áreas de la interfaz de usuario de la cinta de opciones se ven afectadas por los modos de aplicación. Por ejemplo, si la deshabilitación de un modo provoca la pérdida de botones de la cinta de opciones que se agregaron previamente a la barra de herramientas de acceso rápido [,](windowsribbon-controls-quickaccesstoolbar.md)esos botones permanecen en la barra de herramientas de acceso rápido, lo que permite a los usuarios ejecutar los comandos enlazados a los botones. Como regla general, si un comando pertenece a uno o varios modos inactivos, ese comando también debe deshabilitarse estableciendo la propiedad [ \_ PKEY \_ Enabled](windowsribbon-reference-properties-uipkey-enabled.md) de la interfaz de usuario en 0 (VARIANT \_ FALSE).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices de la experiencia del usuario de la cinta de opciones](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Mostrar pestañas contextuales](ribbon-contextualtabs.md)
</dt> </dl>

 

 