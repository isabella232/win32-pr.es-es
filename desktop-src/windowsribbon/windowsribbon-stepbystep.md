---
title: Crear una aplicación de cinta de opciones
description: El marco de la cinta de opciones de Windows se compone de dos plataformas de desarrollo distintas, pero dependientes, un lenguaje de marcado basado en lenguaje XAML (XAML) para declarar controles y su diseño visual, y un conjunto de interfaces basadas en el Modelo de objetos componentes (COM) de C++ para definir la funcionalidad de comandos y los enlaces de aplicación. Esta división del trabajo dentro de la arquitectura del marco de la cinta de opciones requiere que un desarrollador que quiera aprovechar las completas funcionalidades de interfaz de usuario que ofrece el marco de trabajo debe diseñar y describir la interfaz de usuario en el marcado y, a continuación, usar las interfaces COM del marco de la cinta de opciones para conectar el marco a la aplicación host.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Windows Cinta de opciones, crear aplicaciones
- Cinta de opciones, crear aplicaciones
- Windows Cinta de opciones, hoja de ruta
- Cinta de opciones, hoja de ruta
- Windows Cinta de opciones, marcado
- Cinta de opciones, marcado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3cc3395b2fe53759152f5d0244c6546c08832bda190035a918af6049a99811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850023"
---
# <a name="creating-a-ribbon-application"></a>Crear una aplicación de cinta de opciones

El marco de la cinta de opciones de Windows se compone de dos plataformas de desarrollo distintas, pero dependientes: un lenguaje de marcado basado en lenguaje XAML (XAML) para declarar controles y su diseño visual, y un conjunto de interfaces basadas en el Modelo de objetos componentes (COM) de C++ para definir la funcionalidad de comandos y los enlaces de aplicación. Esta división del trabajo dentro de la arquitectura del marco de la cinta de opciones requiere que un desarrollador que quiera aprovechar las completas funcionalidades de interfaz de usuario que ofrece el marco de trabajo debe diseñar y describir la interfaz de usuario en el marcado y, a continuación, usar las interfaces COM del marco de la cinta de opciones para conectar el marco a la aplicación host.

-   [Guía básica de la cinta de opciones](#ribbon-roadmap)
-   [Escribir el marcado](#write-the-markup)
    -   [Compilar el marcado](#compile-the-markup)
-   [Compilación de la aplicación](#build-the-application)
    -   [Inicialización de la cinta de opciones](#initialize-the-ribbon)
    -   [Vincular el marcado a la aplicación](#link-the-markup-to-the-application)
    -   [Compilación de la aplicación](#link-the-markup-to-the-application)
-   [Actualizaciones y ejecuciones en tiempo de ejecución](#run-time-updates-and-executions)
-   [Compatibilidad con OLE](#ole-support)
-   [Temas relacionados](#related-topics)

## <a name="ribbon-roadmap"></a>Guía básica de la cinta de opciones

Los [aspectos](windowsribbon-schema.md)visuales de una aplicación de cinta de opciones, como qué controles se muestran y dónde se colocan, se declaran en marcado (vea Declarar comandos y controles con marcado de cinta). La lógica del comando de aplicación, como lo que sucede cuando se presiona un botón, se implementa en el código.

El proceso de implementar una cinta de opciones e incorporarla a una aplicación de Windows requiere cuatro tareas básicas: escribir el marcado, compilar el marcado, escribir el código y compilar y vincular toda la aplicación.

En el diagrama siguiente se muestra el flujo de trabajo para una implementación típica de la cinta de opciones.

![diagrama que muestra el flujo de trabajo de una implementación típica de la cinta de opciones.](images/overviews/ribbonroadmap.png)

En las secciones siguientes se describe este proceso con más detalle.

## <a name="write-the-markup"></a>Escribir el marcado

Una vez diseñada la interfaz de usuario de la cinta de opciones, la primera tarea para un desarrollador de aplicaciones es describir la interfaz de usuario con marcado de cinta.

> [!IMPORTANT]
> El archivo de esquema de marcado del marco de la cinta de opciones, UICC.xsd, se instala con el Kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4.0. Mediante la ruta de acceso de instalación estándar, el archivo se encuentra en la carpeta Bin %ProgramFiles% DE SDK de Microsoft Windows, donde muchos editores XML pueden hacer referencia a él para proporcionar sugerencias y finalización \\ \\ \\ \[ \] \\ automática.

 

Los controles de la cinta de opciones, los comandos de la cinta de opciones (los elementos independientes del control que proporcionan la funcionalidad base para los controles de la cinta de opciones) y todas las relaciones visuales y de diseño de controles se declaran en el marcado. La estructura del marcado de la cinta de opciones resalta la distinción entre los controles de la cinta de opciones y los comandos [a](windowsribbon-reference-elements-command.md) través de dos jerarquías de nodo principal: un árbol Comandos y recursos y un [árbol Vistas.](windowsribbon-reference-elements-view.md)

Todos los contenedores y acciones expuestos por la cinta de opciones se declaran en el [árbol Comandos y](windowsribbon-reference-elements-command.md) recursos. Cada elemento Command está asociado a un conjunto de recursos, como requiere el diseño de la interfaz de usuario.

Después de crear los comandos para una aplicación, declare controles en el árbol [Vistas](windowsribbon-reference-elements-view.md) y enlace cada control a un comando para exponer la funcionalidad Command. El marco de la cinta de opciones determina el posicionamiento real de los controles en función de la jerarquía de controles declarada aquí.

En el ejemplo de código siguiente se muestra cómo declarar un control Button, con la etiqueta Exit application y asociarlo a un comando Exit.


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> Aunque es posible usar cualquier extensión de nombre de archivo para el archivo de marcado de la cinta de opciones, .xml es la extensión recomendada que se usa en toda la documentación.

 

### <a name="compile-the-markup"></a>Compilar el marcado

Una vez creado el archivo de marcado de la cinta de opciones, el compilador de marcado de la cinta de opciones, UICC, debe compilarlo en un formato binario, que se incluye con el kit de desarrollo de software (SDK) de Windows. La aplicación host pasa una referencia a este archivo binario al método [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) durante la inicialización del marco de la cinta de opciones.

UICC se puede ejecutar directamente desde una ventana de línea de comandos o agregarse como un "paso de compilación personalizado" en Visual Studio.

En la imagen siguiente se muestra el compilador de marcado UICC en la Windows shell cmd del SDK de 7.

![captura de pantalla que uicc.exe en una ventana de línea de comandos.](images/overviews/screenshot-intentcl-commandline.png)

En la imagen siguiente se muestra UICC agregado como paso de compilación personalizada en Visual Studio.

![captura de pantalla uicc.exe se agrega como un paso de compilación personalizado en Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

UICC genera tres archivos: una versión binaria del marcado (.bml), un encabezado de definición de identificador (archivo .h) para exponer elementos de marcado a la aplicación host de la cinta de opciones y un [script](../menurc/about-resource-files.md) de definición de recursos (archivo .rc) para vincular recursos de cadena y imagen de la cinta de opciones a la aplicación host en tiempo de compilación.

Para obtener más información sobre cómo compilar el marcado del marco de la cinta de opciones, [vea Compilar marcado de cinta de opciones.](windowsribbon-intentcl.md)

## <a name="build-the-application"></a>Compilar la aplicación

Una vez que la interfaz de usuario preliminar de una aplicación de cinta de opciones se ha diseñado e implementado en el marcado, se debe escribir código de aplicación que inicialice el marco, consuma el marcado y enlace los comandos declarados en el marcado a los controladores de comandos adecuados de la aplicación.

> [!IMPORTANT]
>
> Puesto que el marco de la cinta de opciones está basado en COM, se recomienda que los proyectos de cinta usen el operador \_ uuidof() para hacer referencia a los GUID de las interfaces de marco de la cinta \_ de opciones (GUID). En aquellos casos en los que no es posible usar el operador uuidof(), como cuando se usa un compilador que no es de Microsoft o la aplicación host está basada en C, la aplicación debe definir los IID, ya que no están contenidos en \_ \_ uuid.lib.
>
> Si la aplicación define los GUID, se deben usar los GUID especificados en UIRibbon.idl.
>
> UIRibbon.idl se distribuye como parte del Kit de desarrollo de [software (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) de Windows y se puede encontrar en la ruta de instalación estándar de %ProgramFiles% SDK de \\ Microsoft Windows \\ \\ v7.0 \\ Include.

 

### <a name="initialize-the-ribbon"></a>Inicialización de la cinta de opciones

En el diagrama siguiente se muestran los pasos necesarios para implementar una sencilla aplicación de cinta de opciones.

![diagrama que muestra los pasos necesarios para implementar una implementación sencilla de la cinta de opciones.](images/overviews/initializationsteps.png)

En los pasos siguientes se describe en detalle cómo implementar una aplicación de cinta de opciones sencilla.

1.  Cocreateinstance

    La aplicación llama a la función coCreateInstance com estándar con el identificador de clase de marco de cinta de opciones para obtener un puntero al marco.

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  Initialize(hwnd, IUIApplication \* )

    La aplicación llama a [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), pasando dos parámetros: el identificador a la ventana de nivel superior que contendrá la cinta de opciones y un puntero a la implementación de [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que permite al marco realizar devoluciones de llamada a la aplicación.

    > \[! Importante\]  
    > El marco de la cinta de opciones se inicializa como un apartamento de un solo subproceso (STA).

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  LoadUI(instance, resourceName)

    La aplicación llama a [**IUIFramework::LoadUI para**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) enlazar el recurso de marcado. El primer parámetro de esta función es un identificador para la instancia de la aplicación Ribbon. El segundo parámetro es el nombre del recurso de marcado binario que se compiló anteriormente. Al pasar el marcado binario al marco de la cinta de opciones, la aplicación indica cuál debe ser la estructura de la cinta de opciones y cómo se deben organizar los controles. También proporciona al marco un manifiesto de comandos para exponer (como Pegar, Cortar, Buscar), que usa el marco cuando realiza devoluciones de llamada relacionadas con comandos en tiempo de ejecución.

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  [**Devoluciones de llamada de IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)

    Una vez completados los pasos del 1 al 3, el marco de la cinta de opciones sabe qué comandos se van a exponer en la cinta. Sin embargo, el marco de trabajo todavía necesita dos cosas antes de que la cinta de opciones sea totalmente funcional: una manera de decir a la aplicación cuándo se ejecutan los comandos y una manera de obtener recursos de comando, o propiedades, en tiempo de ejecución. Por ejemplo, si un cuadro combinado va a aparecer en la interfaz de usuario, el marco debe solicitar los elementos con los que rellenar el cuadro combinado.

    Estos dos elementos de funcionalidad se controlan a través de la [**interfaz IUICommandHandler.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) En concreto, para cada comando declarado en el marcado binario (vea el paso 3 anterior), el marco llama a [**IUIApplication::OnCreateUICommand para**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) pedir a la aplicación un objeto **IUICommandHandler** para ese comando.

    > [!Note]  
    > La [**interfaz IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) permite enlazar un controlador Command a uno o varios comandos.

     

Como mínimo, se requiere que la aplicación implemente códigos auxiliares de métodos [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que devuelvan E NOTIMPL, como se \_ muestra en el ejemplo siguiente.


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a>Vincular el marcado a la aplicación

En este momento, los archivos de recursos de marcado deben vincularse a la aplicación host mediante la inclusión de una referencia al archivo de definición de recursos de marcado (que contiene una referencia al archivo de encabezado de marcado) en el archivo de recursos de aplicación. Por ejemplo, una aplicación denominada RibbonApp con un archivo de recursos denominado ribbonUI.rc requiere la siguiente línea en el archivo RibbonApp.rc.


```C++
#include "ribbonUI.rc"
```



Según el compilador y el vinculador que se utilicen, el script de definición de recursos también puede requerir la compilación antes de que se pueda compilar la aplicación de cinta de opciones. La herramienta de línea de comandos del compilador de recursos [(RC)](../menurc/using-rc-the-rc-command-line-.md) que se incluye con Microsoft Visual Studio y el SDK de Windows se puede usar para esta tarea.

### <a name="compile-the-application"></a>Compilación de la aplicación

Una vez compilada la aplicación ribbon, se puede ejecutar y probar la interfaz de usuario. Si la interfaz de usuario requiere ajustes y no hay ningún cambio en los controladores de comandos asociados en el código de aplicación principal, revise el archivo de código fuente de marcado, vuelva a compilar el marcado con UICC.exe y vincule los nuevos archivos de recursos de marcado. Cuando se reinicia la aplicación, se muestra la interfaz de usuario modificada.

Todo esto es posible sin tocar el código principal de la aplicación, una mejora significativa con respecto al desarrollo y distribución de aplicaciones estándar.

## <a name="run-time-updates-and-executions"></a>Actualizaciones y ejecuciones en tiempo de ejecución

La estructura de comunicación en tiempo de ejecución del marco de la cinta de opciones se basa en un modelo de inserción y extracción, o de llamador bidireccional.

Este modelo permite que el marco informe a la aplicación cuando se ejecuta un comando y permite que tanto el marco como la aplicación consulten, actualicen e invaliden los valores de propiedad y los recursos de la cinta de opciones. Esta funcionalidad se proporciona a través de una serie de interfaces y métodos.

El marco extrae información de propiedades actualizada de la aplicación ribbon mediante el método de devolución de llamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) Un identificador de comando y una clave de propiedad, que identifica la propiedad Command que se va a actualizar, se pasan al método que, a continuación, devuelve o inserta un valor para esa clave de propiedad en el marco de trabajo.

El marco llama a [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se ejecuta un comando e identifica tanto el identificador de comando como el tipo de ejecución que se produjo ([**\_ UI EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)). Aquí es donde la aplicación especifica la lógica de ejecución de un comando.

En el diagrama siguiente se muestra la comunicación en tiempo de ejecución para la ejecución de comandos entre el marco y la aplicación.

![diagrama que muestra un ejemplo de la comunicación en tiempo de ejecución entre el marco de la cinta de opciones y una aplicación host.](images/overviews/updatesandexecutions.png)

> [!Note]  
> No es necesario implementar las funciones [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) e [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para mostrar inicialmente una cinta de opciones en una aplicación. Sin embargo, estos métodos son necesarios para asegurarse de que la aplicación funciona correctamente cuando el usuario ejecuta comandos.

 

## <a name="ole-support"></a>Compatibilidad con OLE

Una aplicación de cinta de opciones se puede configurar como un servidor OLE para admitir la activación OLE fuera de contexto.

Los objetos creados en una aplicación de servidor OLE mantienen su asociación con la aplicación de servidor cuando se insertan (ya sea pegadas o colocadas) en una aplicación cliente OLE (o contenedor). En la activación OLE fuera de contexto, al hacer doble clic en el objeto de la aplicación cliente se abre una instancia dedicada de la aplicación de servidor y se carga el objeto para su edición. Cuando se cierra la aplicación de servidor, todos los cambios realizados en el objeto se reflejan en la aplicación cliente.

> [!Note]  
> El marco de la cinta de opciones no admite la activación OLE local. Los objetos creados en un servidor OLE basado en cinta de opciones no se pueden editar desde dentro de la aplicación cliente OLE. Se requiere una instancia dedicada externa de la aplicación de servidor.


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declarar comandos y controles con marcado de cinta](./windowsribbon-schema.md)
</dt> <dt>

[Directrices de la experiencia del usuario de la cinta de opciones](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta de opciones](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




