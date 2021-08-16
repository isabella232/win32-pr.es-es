---
title: Declarar comandos y controles con marcado de cinta de opciones
description: El Windows ribbon usa un lenguaje de marcado basado en lenguaje XAML (XAML) para implementar mediante declaración la apariencia de una aplicación de cinta de opciones.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Windows Cinta de opciones, estructura de marcado
- Cinta de opciones, estructura de marcado
- Windows Cinta de opciones, separación de la presentación de la lógica de comandos
- Cinta de opciones, separación de la presentación de la lógica de comandos
- Windows Cinta de opciones, componentes
- Cinta de opciones, componentes
- sistema de comandos para Windows cinta de opciones
- controles para la cinta Windows opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ae6c8d62012fac240c6d044c688295d89d8d5899e3673a3b914d8d142111d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201327"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Declarar comandos y controles con marcado de cinta de opciones

El Windows ribbon usa un lenguaje de marcado basado en lenguaje XAML (XAML) para implementar mediante declaración la apariencia de una aplicación de cinta de opciones.

-   [Separación de la presentación de la lógica de comandos](#separating-presentation-from-command-logic)
-   [Estructura de marcado](#markup-structure)
-   [Componentes de la cinta de opciones](#ribbon-components)
-   [Temas relacionados](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Separación de la presentación de la lógica de comandos

La separación de los atributos visuales y de presentación de la lógica de comandos en el marco de la cinta de opciones se logra a través de dos plataformas de desarrollo distintas, pero dependientes. Los diseños de control, los comportamientos de escalado, las declaraciones de comandos y las especificaciones de recursos son el dominio en tiempo de diseño de una sintaxis de marcado declarativa basada en [la especificación lenguaje XAML (XAML).](/dotnet/framework/wpf/advanced/xaml-in-wpf) La funcionalidad de bajo nivel, los enlaces de aplicación y los controladores de comandos se definen en implementaciones de interfaz basadas en el Modelo de objetos componentes (COM).

Esta separación de la presentación y la lógica proporciona las siguientes ventajas:

-   Un ciclo de desarrollo de aplicaciones más eficaz que permite a los desarrolladores y diseñadores de la interfaz de usuario implementar la GUI de la aplicación de cinta de opciones independientemente de la funcionalidad principal de la aplicación. Esta funcionalidad principal se puede dejar a desarrolladores de software dedicados.
-   Mantenimiento menos costoso porque los cambios en la GUI son posibles sin cambios en la funcionalidad principal (y viceversa).
-   Especificación simple de los recursos de cadena e imagen mediante marcado.
-   Facilidad de creación de prototipos.

## <a name="markup-structure"></a>Estructura de marcado

Existen dos ramas distintas dentro de la estructura del marcado del marco de la cinta de opciones.

La primera rama contiene un manifiesto de declaraciones de comandos y recursos (cadenas e imágenes). El marco usa cada entrada Command para enlazar un control Ribbon, a través de un identificador de comando, a un controlador Command definido en el código de la aplicación.

La segunda rama contiene las declaraciones de control reales. Cada control está asociado a un comando a través de un *atributo CommandName* que se asigna a un *atributo Name* especificado en cada declaración Command.

## <a name="ribbon-components"></a>Componentes de la cinta de opciones

La funcionalidad de interfaz de usuario del marco de opciones se expone a través [de vistas](windowsribbon-reference-elements-view.md). Una vista es básicamente un [](windowsribbon-element-ribbon.md) contenedor, como la cinta de opciones y [**ContextPopup,**](windowsribbon-element-contextpopup.md)que se usa para presentar controles de marco y los comandos a los que están enlazados.

La [](windowsribbon-element-ribbon.md) vista de la cinta de opciones se compone de varios componentes que incluyen un menú de [aplicación,](windowsribbon-controls-applicationmenu.md)la barra [](windowsribbon-controls-group.md) de herramientas de acceso rápido [(QAT)](windowsribbon-controls-quickaccesstoolbar.md) para mostrar comandos usados habitualmente desde la interfaz de usuario de la cinta de opciones, las [pestañas](windowsribbon-controls-tab.md) principales y contextuales que contienen grupos de controles y el sistema de menús contextuales enriquecido de [**ContextPopup**](windowsribbon-element-contextpopup.md).

Todos los componentes de la cinta de opciones se declaran en un archivo de marcado independiente que:

-   Especifica las propiedades básicas de cada elemento.
-   Muestra claramente las relaciones jerárquicas.
-   Proporciona preferencias de diseño y sugerencias de escalado. Para obtener más información sobre las plantillas de diseño del marco de opciones, vea Personalizar una cinta de opciones mediante definiciones [de tamaño y directivas de escalado.](windowsribbon-templates.md)
-   Proporciona una manera de definir recursos como imágenes y etiquetas. Para obtener más información sobre los recursos de imagen, vea [Especificar recursos de imagen de la cinta de opciones.](windowsribbon-imageformats.md)

Los dos ejemplos de marcado de la cinta de opciones siguientes muestran cómo un conjunto de elementos del menú Aplicación de la cinta de opciones se asocian cada uno con un nombre de comando y un identificador.

1.  En esta sección se muestran las declaraciones de comandos necesarias para un menú de aplicación con comandos básicos como Nuevo, Abrir y Guardar.
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

    

2.  En esta sección se muestran las declaraciones de Control asociadas.
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

    

Cuando el marcado se compila con la herramienta Compilador de comandos de interfaz de usuario (UICC), los nombres de comando y los IDs se colocan en un archivo de encabezado usado por la aplicación host de la cinta de opciones.

A continuación se muestra un ejemplo de un archivo de encabezado generado por UICC.


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

[lenguaje XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[Compilación del marcado de la cinta de opciones](windowsribbon-intentcl.md)
</dt> </dl>

 

 