---
title: Declarar comandos y controles con el marcado de la cinta de opciones
description: El marco de cinta de Windows usa un lenguaje de marcado basado en lenguaje XAML (XAML) para implementar de forma declarativa la apariencia de una aplicación de cinta.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Cinta de Windows, estructura de marcado
- Cinta, estructura de marcado
- Cinta de opciones de Windows, separar la presentación de la lógica de comandos
- Cinta de opciones, separar la presentación de la lógica de comandos
- Cinta de Windows, componentes
- Cinta de opciones, componentes
- sistema de comandos para la cinta de Windows
- controles de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421136"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Declarar comandos y controles con el marcado de la cinta de opciones

El marco de cinta de Windows usa un lenguaje de marcado basado en lenguaje XAML (XAML) para implementar de forma declarativa la apariencia de una aplicación de cinta.

-   [Separar la presentación de la lógica de comandos](#separating-presentation-from-command-logic)
-   [Estructura de marcado](#markup-structure)
-   [Componentes de la cinta](#ribbon-components)
-   [Temas relacionados](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Separar la presentación de la lógica de comandos

La separación de los atributos visuales y de presentación de la lógica de comandos en el marco de cinta se realiza a través de dos plataformas de desarrollo distintas, pero dependientes. Los diseños de control, los comportamientos de escalado, las declaraciones de comandos y las especificaciones de recursos son el dominio de tiempo de diseño de una sintaxis de marcado declarativo basada en la especificación [lenguaje XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) . En las implementaciones de interfaz basadas en el modelo de objetos componentes (COM) se definen la funcionalidad de bajo nivel, los enlaces de aplicación y los controladores de comandos.

Esta separación de la presentación y la lógica proporciona las siguientes ventajas:

-   Un ciclo de desarrollo de aplicaciones más eficaz que permite a los desarrolladores y diseñadores de la interfaz de usuario implementar la GUI de la aplicación de cinta independientemente de la funcionalidad básica de la aplicación. Esta funcionalidad principal se puede dejar a los desarrolladores de software dedicados.
-   Mantenimiento menos costoso porque los cambios en la interfaz gráfica de usuario son posibles sin cambios en la funcionalidad básica (y viceversa).
-   Especificación simple de los recursos de cadena e imagen mediante marcado.
-   Facilidad de prototipos.

## <a name="markup-structure"></a>Estructura de marcado

Existen dos ramas distintas dentro de la estructura del marcado del marco de cinta.

La primera bifurcación contiene un manifiesto de declaraciones de comandos y recursos (cadenas e imágenes). El marco de trabajo usa cada entrada de comando para enlazar un control de la cinta de opciones, a través de un identificador de comando, a un controlador de comandos definido en el código de la aplicación.

La segunda bifurcación contiene las declaraciones de control reales. Cada control está asociado a un comando a través de un atributo *CommandName* que se asigna a un atributo de *nombre* especificado en cada declaración de comando.

## <a name="ribbon-components"></a>Componentes de la cinta

La funcionalidad de la interfaz de usuario del marco de cinta se expone a través de [vistas](windowsribbon-reference-elements-view.md). Una vista es esencialmente un contenedor, como la [**cinta**](windowsribbon-element-ribbon.md) de opciones y [**ContextPopup**](windowsribbon-element-contextpopup.md), que se usa para presentar controles de marco y los comandos a los que están enlazados.

La vista de la [**cinta**](windowsribbon-element-ribbon.md) de opciones se compone de varios componentes que incluyen un menú de la [aplicación](windowsribbon-controls-applicationmenu.md), la barra de [herramientas de acceso rápido (Qat)](windowsribbon-controls-quickaccesstoolbar.md) para mostrar los comandos usados habitualmente en la interfaz de usuario de la cinta de opciones, las [pestañas](windowsribbon-controls-tab.md) principal y contextual que contienen [grupos](windowsribbon-controls-group.md) de controles y el completo sistema de menús contextuales del [**ContextPopup**](windowsribbon-element-contextpopup.md).

Todos los componentes de la cinta de opciones se declaran en un archivo de marcado independiente que:

-   Especifica las propiedades básicas de cada elemento.
-   Muestra claramente las relaciones jerárquicas.
-   Proporciona las preferencias de diseño y las sugerencias de escalado. Para obtener más información sobre las plantillas de diseño del marco de cinta, vea [personalizar una cinta a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md).
-   Proporciona una manera de definir recursos como imágenes y etiquetas. Para obtener más información sobre los recursos de imagen, consulte [especificar recursos de imagen de la cinta](windowsribbon-imageformats.md)de opciones.

Los dos ejemplos de marcado de la cinta de opciones siguientes muestran cómo un conjunto de elementos de menú de la aplicación de cinta está asociado a un nombre y un identificador de comando.

1.  En esta sección se muestran las declaraciones de comandos necesarias para un menú de la aplicación con comandos básicos como nuevo, abrir y guardar.
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  En esta sección se muestran las declaraciones de control asociadas.
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

Cuando el marcado se compila con la herramienta del compilador de comandos de la interfaz de usuario (UICC), los nombres y los identificadores de comando se colocan en un archivo de encabezado usado por la aplicación host de la cinta de opciones.

El siguiente es un ejemplo de un archivo de encabezado generado por UICC.


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lenguaje XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[Compilar marcado de cinta](windowsribbon-intentcl.md)
</dt> </dl>

 

 