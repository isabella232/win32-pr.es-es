---
title: Crear una aplicación de cinta
description: El marco de la cinta de Windows se compone de dos plataformas de desarrollo distintas, pero dependientes, un lenguaje de marcado basado en lenguaje XAML (XAML) para declarar controles y su diseño visual, y un conjunto de interfaces basado en el modelo de objetos componentes (COM) de C++ para definir la funcionalidad de comandos y los enlaces de la aplicación. Esta división de mano de obra dentro de la arquitectura del marco de cinta requiere que un desarrollador que desee aprovechar las capacidades enriquecidas de la interfaz de usuario que ofrece el marco de trabajo debe diseñar y describir la interfaz de usuario en el marcado y, a continuación, usar las interfaces COM del marco de cinta para conectar el marco de trabajo a la aplicación host.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Cinta de Windows, crear aplicaciones
- Cinta, crear aplicaciones
- Cinta de opciones de Windows, mapa de ruta
- Cinta, guía básica
- Cinta de Windows, marcado
- Cinta de opciones, marcado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421137"
---
# <a name="creating-a-ribbon-application"></a>Crear una aplicación de cinta

El marco de la cinta de opciones de Windows se compone de dos plataformas de desarrollo distintas pero dependientes: un lenguaje de marcado basado en lenguaje XAML (XAML) para declarar controles y su diseño visual, y un conjunto de interfaces basado en el modelo de objetos componentes (COM) de C++ para definir la funcionalidad del comando y los enlaces de la aplicación. Esta división de mano de obra dentro de la arquitectura del marco de cinta requiere que un desarrollador que desee aprovechar las capacidades enriquecidas de la interfaz de usuario que ofrece el marco de trabajo debe diseñar y describir la interfaz de usuario en el marcado y, a continuación, usar las interfaces COM del marco de cinta para conectar el marco de trabajo a la aplicación host.

-   [Guía básica de la cinta](#ribbon-roadmap)
-   [Escribir el marcado](#write-the-markup)
    -   [Compilar el marcado](#compile-the-markup)
-   [Compilar la aplicación](#build-the-application)
    -   [Inicializar la cinta de opciones](#initialize-the-ribbon)
    -   [Vincular el marcado a la aplicación](#link-the-markup-to-the-application)
    -   [Compilar la aplicación](#link-the-markup-to-the-application)
-   [Actualizaciones y ejecuciones en tiempo de ejecución](#run-time-updates-and-executions)
-   [Compatibilidad con OLE](#ole-support)
-   [Temas relacionados](#related-topics)

## <a name="ribbon-roadmap"></a>Guía básica de la cinta

Los aspectos visuales de una aplicación de la cinta de opciones, como los controles que se muestran y dónde se colocan, se declaran en el marcado (vea [declarar comandos y controles con el marcado de la cinta de](windowsribbon-schema.md)opciones). La lógica de comandos de la aplicación, como lo que sucede cuando se presiona un botón, se implementa en el código.

El proceso de implementación de una cinta de opciones y su incorporación en una aplicación Windows requiere cuatro tareas básicas: escribir el marcado, compilar el marcado, escribir el código y compilar y vincular toda la aplicación.

En el diagrama siguiente se ilustra el flujo de trabajo para una implementación de cinta de opciones típica.

![diagrama que muestra el flujo de trabajo para una implementación de cinta típica.](images/overviews/ribbonroadmap.png)

En las secciones siguientes se describe este proceso con más detalle.

## <a name="write-the-markup"></a>Escribir el marcado

Una vez diseñada la interfaz de usuario de la cinta de opciones, la primera tarea para el desarrollador de la aplicación es describir la interfaz de usuario con el marcado de la cinta.

> [!IMPORTANT]
> El archivo de esquema de marcado del marco de cinta, UICC. xsd, se instala con el kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4,0. Con la ruta de instalación estándar, el archivo se encuentra en la carpeta% ProgramFiles% \\ Microsoft SDK \\ Windows \\ \[ número \] \\ bin, donde se puede hacer referencia a él mediante muchos editores XML para proporcionar sugerencias y la finalización automática.

 

Controles de la cinta de opciones, comandos de la cinta de opciones (los elementos independientes del control que proporcionan la funcionalidad básica para los controles de la cinta) y todas las relaciones visuales y de diseño del control se declaran en el marcado. La estructura del marcado de la cinta de opciones destaca la distinción entre los controles y comandos de la cinta de opciones a través de dos jerarquías de nodos principales: un árbol de [comandos y recursos](windowsribbon-reference-elements-command.md) y un árbol de [vistas](windowsribbon-reference-elements-view.md) .

Todos los contenedores y las acciones que expone la cinta de opciones se declaran en el árbol de [comandos y recursos](windowsribbon-reference-elements-command.md) . Cada elemento de comando está asociado a un conjunto de recursos, tal y como requiere el diseño de la interfaz de usuario.

Después de crear los comandos para una aplicación, se declaran los controles en el árbol de [vistas](windowsribbon-reference-elements-view.md) y se enlaza cada control a un comando para exponer la funcionalidad del comando. El marco de cinta determina el posicionamiento real de los controles en función de la jerarquía de controles declarada aquí.

En el ejemplo de código siguiente se muestra cómo declarar un control de botón, con la etiqueta aplicación de salida, y asociarlo a un comando de salida.


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
> Aunque es posible usar cualquier extensión de nombre de archivo para el archivo de marcado de la cinta,. XML es la extensión recomendada que se utiliza en toda la documentación.

 

### <a name="compile-the-markup"></a>Compilar el marcado

Una vez creado el archivo de marcado de la cinta de opciones, el compilador de marcado de la cinta de opciones (UICC), que se incluye con el kit de desarrollo de software (SDK) de Windows, debe compilarse en un formato binario. Una referencia a este archivo binario se pasa al método [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) durante la inicialización del marco de la cinta de opciones de la aplicación host.

UICC se puede ejecutar directamente desde una ventana de línea de comandos o agregarse como un "paso de compilación personalizada" en Visual Studio.

En la imagen siguiente se muestra el compilador de marcado UICC en la ventana de Shell CMD del SDK de Windows 7.

![captura de pantalla que muestra uicc.exe en una ventana de línea de comandos.](images/overviews/screenshot-intentcl-commandline.png)

La siguiente imagen muestra UICC agregado como un paso de compilación personalizado en Visual Studio.

![captura de pantalla que muestra uicc.exe agregado como un paso de compilación personalizado en Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

UICC genera tres archivos: una versión binaria del marcado (. BML), un encabezado de definición de identificador (archivo. h) para exponer los elementos de marcado en la aplicación host de la cinta de opciones y un [script de definición de recursos](../menurc/about-resource-files.md) (archivo. RC) para vincular los recursos de cadena y imagen de la cinta de opciones a la aplicación host en tiempo de compilación.

Para obtener más información sobre cómo compilar el marcado del marco de cinta, consulte [compilar el marcado de cinta](windowsribbon-intentcl.md).

## <a name="build-the-application"></a>Compilar la aplicación

Una vez que la interfaz de usuario preliminar para una aplicación de cinta se ha diseñado e implementado en el marcado, debe escribirse código de aplicación que inicialice el marco de trabajo, consume el marcado y enlaza los comandos declarados en el marcado a los controladores de comandos adecuados en la aplicación.

> [!IMPORTANT]
>
> Dado que el marco de la cinta de opciones está basado en COM, se recomienda que los proyectos de la cinta de opciones utilicen el \_ \_ operador uuidof () para hacer referencia a los GUID de las interfaces del marco de cinta (IID). En aquellos casos en los que no es posible usar el \_ \_ operador uuidof (), como cuando se usa un compilador que no es de Microsoft o la aplicación host se basa en C, la aplicación debe definir los IID, ya que no están incluidos en UUID. lib.
>
> Si la aplicación define los IID, se deben usar los GUID especificados en UIRibbon. idl.
>
> UIRibbon. idl se incluye como parte del [Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windows/bb980924.aspx) y puede encontrarse en la ruta de instalación estándar de% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ include.

 

### <a name="initialize-the-ribbon"></a>Inicializar la cinta de opciones

En el diagrama siguiente se muestran los pasos necesarios para implementar una aplicación de cinta de opciones simple.

![diagrama que muestra los pasos necesarios para implementar una implementación de cinta de opciones simple.](images/overviews/initializationsteps.png)

En los pasos siguientes se describe en detalle cómo implementar una aplicación de cinta de opciones simple.

1.  CoCreateInstance

    La aplicación llama a la función CoCreateInstance de COM estándar con el identificador de clase de marco de cinta para obtener un puntero al marco de trabajo.

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

    

2.  Initialize (HWND, IUIApplication \* )

    La aplicación llama a [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), pasando dos parámetros: el identificador de la ventana de nivel superior que contendrá la cinta de opciones y un puntero a la implementación de [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que permite que el marco de trabajo realice devoluciones de llamada a la aplicación.

    > \[! Aún\]  
    > El marco de la cinta de opciones se inicializa como un contenedor uniproceso (STA).

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  LoadUI (instancia, resourceName)

    La aplicación llama a [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) para enlazar el recurso de marcado. El primer parámetro de esta función es un identificador de la instancia de la aplicación de cinta. El segundo parámetro es el nombre del recurso de marcado binario que se compiló anteriormente. Al pasar el marcado binario al marco de la cinta de opciones, la aplicación indica cuál debe ser la estructura de la cinta y cómo deben organizarse los controles. También proporciona el marco de trabajo con un manifiesto de comandos para exponer (como pegar, cortar, buscar), que usa el marco de trabajo cuando realiza devoluciones de llamada relacionadas con el comando en tiempo de ejecución.

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  Devoluciones de llamada [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)

    Una vez completados los pasos del 1 al 3, el marco de la cinta de opciones sabe qué comandos exponer en la cinta de opciones. Sin embargo, el marco sigue necesitando dos cosas antes de que la cinta sea totalmente funcional: una manera de indicar a la aplicación Cuándo se ejecutan los comandos y una manera de obtener recursos de comando o propiedades en tiempo de ejecución. Por ejemplo, si un cuadro combinado va a aparecer en la interfaz de usuario, el marco de trabajo debe solicitar los elementos con los que rellenar el cuadro combinado.

    Estos dos fragmentos de funcionalidad se controlan a través de la interfaz [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) . En concreto, para cada comando declarado en el marcado binario (vea el paso 3 anterior), el marco llama a [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) para solicitar a la aplicación un objeto **IUICommandHandler** para ese comando.

    > [!Note]  
    > La interfaz [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) permite enlazar un controlador de comandos a uno o varios comandos.

     

Como mínimo, la aplicación debe implementar los códigos auxiliares de los métodos [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que devuelven E \_ NOTIMPL como se muestra en el ejemplo siguiente.


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

En este momento, los archivos de recursos de marcado deben estar vinculados a la aplicación host mediante la inclusión de una referencia al archivo de definición de recursos de marcado (que contiene una referencia al archivo de encabezado de marcado) en el archivo de recursos de la aplicación. Por ejemplo, una aplicación denominada RibbonApp con un archivo de recursos denominado ribbonUI. RC requiere la siguiente línea en el archivo RibbonApp. rc.


```C++
#include "ribbonUI.rc"
```



Dependiendo del compilador y del vinculador que se use, es posible que el script de definición de recursos también requiera la compilación antes de que se pueda compilar la aplicación de cinta. La herramienta de línea de comandos [del compilador de recursos (RC)](../menurc/using-rc-the-rc-command-line-.md) que se incluye con Microsoft Visual Studio y el Windows SDK se puede usar para esta tarea.

### <a name="compile-the-application"></a>Compilar la aplicación

Una vez compilada la aplicación de cinta, se puede ejecutar y se ha probado la interfaz de usuario. Si la interfaz de usuario requiere la modificación y no hay ningún cambio en los controladores de comandos asociados en el código de aplicación principal, revise el archivo de código fuente de marcado, vuelva a compilar el marcado con UICC.exe y vincule los nuevos archivos de recursos de marcado. Cuando se reinicia la aplicación, se muestra la interfaz de usuario modificada.

Todo esto es posible sin tocar el código de aplicación principal, una mejora significativa sobre el desarrollo y la distribución de aplicaciones estándar.

## <a name="run-time-updates-and-executions"></a>Actualizaciones y ejecuciones en tiempo de ejecución

La estructura de comunicación en tiempo de ejecución del marco de la cinta de opciones se basa en un modelo de llamador de inserción y extracción, o de llamada bidireccional.

Este modelo permite que el marco de trabajo informe a la aplicación cuando se ejecuta un comando y permite que el marco y la aplicación consulten, actualicen e invaliden los valores de propiedad y los recursos de la cinta de opciones. Esta funcionalidad se proporciona a través de una serie de interfaces y métodos.

El marco extrae información de propiedades actualizada de la aplicación de cinta a través del método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) . Un identificador de comando y una clave de propiedad, que identifica la propiedad de comando que se va a actualizar, se pasan al método que devuelve, o inserciones, un valor para esa clave de propiedad en el marco de trabajo.

El marco de trabajo llama a [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) cuando se ejecuta un comando, que identifica el identificador de comando y el tipo de ejecución que se ha producido ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)). Aquí es donde la aplicación especifica la lógica de ejecución de un comando.

En el diagrama siguiente se muestra la comunicación en tiempo de ejecución para la ejecución de comandos entre el marco de trabajo y la aplicación.

![diagrama que muestra un ejemplo de la comunicación en tiempo de ejecución entre el marco de la cinta de opciones y una aplicación host.](images/overviews/updatesandexecutions.png)

> [!Note]  
> No es necesario implementar las funciones [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para mostrar inicialmente una cinta en una aplicación. Sin embargo, estos métodos son necesarios para garantizar que la aplicación funciona correctamente cuando el usuario ejecuta los comandos.

 

## <a name="ole-support"></a>Compatibilidad con OLE

Una aplicación de la cinta de opciones se puede configurar como un servidor OLE para admitir la activación OLE fuera de la ubicación.

Los objetos creados en una aplicación de servidor OLE mantienen su asociación con la aplicación de servidor cuando se insertan (se pegan o colocan) en una aplicación cliente OLE (o contenedor). En la activación OLE fuera de la ubicación, al hacer doble clic en el objeto en la aplicación cliente, se abre una instancia dedicada de la aplicación de servidor y se carga el objeto para su edición. Cuando se cierra la aplicación de servidor, todos los cambios realizados en el objeto se reflejan en la aplicación cliente.

> [!Note]  
> El marco de la cinta de opciones no admite la activación OLE en contexto. Los objetos creados en un servidor OLE basado en cinta no se pueden editar desde la aplicación cliente OLE. Se requiere una instancia externa dedicada de la aplicación de servidor.


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declarar comandos y controles con el marcado de la cinta de opciones](./windowsribbon-schema.md)
</dt> <dt>

[Instrucciones para la experiencia del usuario en cinta](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




