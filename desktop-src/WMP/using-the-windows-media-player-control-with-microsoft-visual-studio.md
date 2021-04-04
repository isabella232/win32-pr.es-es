---
title: Usar el control Media Player de Windows con Microsoft Visual Studio
description: Usar el control Media Player de Windows con Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, .NET Framework
- Modelo de objetos de Windows Media Player, .NET Framework
- modelo de objetos, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Control ActiveX de Windows Media Player, .NET Framework
- Control ActiveX móvil de Windows Media Player, .NET Framework
- Control ActiveX, .NET Framework
- Control ActiveX de Windows Media Player, Visual Studio
- Control ActiveX móvil de Windows Media Player, Visual Studio
- Control ActiveX, Visual Studio
- .NET Framework, inserción de programas de Visual Studio
- incrustación, programas de Visual Studio
- Visual Studio, inserción de programas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104076425"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>Usar el control Media Player de Windows con Microsoft Visual Studio

Puede Agregar la serie Windows Media Player 9 o el control ActiveX posterior a una aplicación .NET Framework a través del cuadro de herramientas de Visual Studio.

## <a name="adding-the-windows-media-player-control"></a>Agregar el control Media Player de Windows

Antes de crear un nuevo proyecto, asegúrese de que la versión más reciente de Windows Media Player y el SDK de Windows Media Player está instalado en el equipo.

Inicie Visual Studio y, a continuación, cree un nuevo proyecto.

En Visual Studio, abra el cuadro de herramientas.

Si Windows Media Player no aparece en la parte **componentes** del cuadro de herramientas, haga lo siguiente:

1.  Haga clic con el botón derecho en el cuadro de herramientas y seleccione **elegir elementos**. Se abrirá el cuadro de diálogo Personalizar cuadro de **herramientas** .
2.  En la pestaña **componentes com** , seleccione Windows Media Player.

    Si Windows Media Player no aparece en la lista, haga clic en **examinar** y, a continuación, abra Wmp.dll, que debe estar en la \\ carpeta system32 de Windows.

3.  Haga clic en **OK**. El control Media Player de Windows se colocará en la pestaña actual del cuadro de herramientas.

Ahora puede seleccionar Windows Media Player en el cuadro de herramientas y agregarlo a un formulario.

Visual Studio proporciona a Windows Media Player control un nombre predeterminado como "axWindowsMediaPlayer1". Puede que desee cambiar el nombre por algo más fácil de recordar, como "reproductor".

Al agregar el control Media Player de Windows desde el cuadro de herramientas, también se agregan referencias a dos bibliotecas creadas por Visual Studio, AxWMPLib y WMPLib. Puede encontrarlos en el Explorador de soluciones en **referencias**.

Para facilitar el uso de los objetos del espacio de nombres del reproductor, debe incluir el espacio de nombres en las directivas Using o Imports de los archivos, como se indica a continuación:


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



La Directiva garantiza que puede hacer referencia a los objetos de **reproductor** sin calificar completamente sus nombres.

> [!Note]  
> El control Media Player de Windows es un objeto **AxWindowsMediaPlayer** del espacio de nombres **AxWMPLib** . Sin embargo, la clase **AxWindowsMediaPlayer** usa tipos de datos, interfaces y otros elementos del espacio de nombres **WMPLib** .

 

## <a name="configuring-visibility-of-the-control"></a>Configurar la visibilidad del control

Cuando agregue por primera vez el control de Media Player de Windows a un formulario, será visible. Si no desea usar la imagen visible del reproductor en la aplicación, oculte el reproductor predeterminado estableciendo cualquiera de las siguientes propiedades:



| Propiedad        | Value                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | "invisible" (vea [Player. uiMode](player-uimode.md)). |
| **Visible**     | "false"                                               |
| **Tamaño. ancho**  | 0                                                     |
| **Tamaño. alto** | 0                                                     |



 

Puede establecer estas propiedades en el código o en la ventana **propiedades** cuando se selecciona el control Media Player de Windows en el diseñador de formularios.

## <a name="object-model-compatibility-of-the-control"></a>Compatibilidad del modelo de objetos del control

El modelo de objetos para el control Media Player de Windows es básicamente el mismo en el .NET Framework como en el script y el código no administrado. Sin embargo, hay diferencias en el modo en que se exponen los elementos:

-   La mayoría de los objetos se exponen bajo el nombre de la interfaz COM subyacente. Por ejemplo, el objeto de **lista de reproducción** se expone como **IWMPPlaylist**.
-   Algunas interfaces tienen versiones posteriores. Por ejemplo, a **IWMPMedia** se le proporcionó funcionalidad adicional en **IWMPMedia2** y **IWMPMedia3**. Si declara un objeto como **IWMPMedia**, normalmente tiene acceso a la funcionalidad de todas las versiones de la interfaz. Sin embargo, IntelliSense® no reconocerá los métodos o las propiedades de las interfaces de versiones posteriores, y el editor de .NET de Visual Basic no corregirá automáticamente las mayúsculas. Para obtener todas las ventajas de IntelliSense y otras características de Visual Studio, declare el objeto con la versión más reciente de la interfaz, como **IWMPMedia3**.
-   No hay propiedades indizadas (C#) o propiedades predeterminadas (Visual Basic .NET). Por ejemplo, para recuperar un **elemento playlist. Item**, debe llamar al método de descriptor de acceso **IWMPlaylist. Get \_ Item** en C# o recuperar la propiedad **IWMPlayist. Item** en Visual Basic .net.
-   Debido a un conflicto de nombres entre la propiedad de los **controles** de Windows Media Player y la propiedad **Controls** expuesta por cada control, la versión del reproductor de esta propiedad se denomina **CtlControls** en el contexto del control ActiveX. (Sin embargo, esto no es así cuando se crea el reproductor mediante programación, en lugar de como un control ActiveX).

Use el Examinador de objetos de Visual Studio para buscar los nombres de API correctos para los métodos y objetos de los espacios de nombres **AxWMPLib** y **WMPLib** .

## <a name="distributing-your-application"></a>Distribuir la aplicación

Al distribuir la aplicación, asegúrese de instalar AxInterop.WMPLib.dll y Interop.WMPLib.dll en la carpeta de la aplicación. También debe asegurarse de que la versión de Windows Media Player requerida esté instalada en el equipo del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el control Media Player de Windows mediante programación**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**Incrustar el control Media Player de Windows en una solución de C#**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**Incrustar el control Media Player de Windows en una solución Visual Basic .NET**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




