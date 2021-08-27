---
title: Uso del control Reproductor de Windows Media con Microsoft Visual Studio
description: Uso del control Reproductor de Windows Media con Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media,.NET Framework
- Reproductor de Windows Media modelo de objetos, .NET Framework
- modelo de objetos, .NET Framework
- Reproductor de Windows Media Mobile,.NET Framework
- Reproductor de Windows Media ActiveX control, .NET Framework
- Reproductor de Windows Media Control ActiveX móvil, .NET Framework
- ActiveX control, .NET Framework
- Reproductor de Windows Media ActiveX control, Visual Studio
- Reproductor de Windows Media Control ActiveX móvil, Visual Studio
- ActiveX control, Visual Studio
- .NET Framework,Visual Studio inserción de programas
- embedding,Visual Studio programas
- Visual Studio, inserción de programas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bb9597b8ad5baadbd51625c68a1d7fb7ebc1791c2d6e8015fb79ba2cab3be6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830454"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>Uso del control Reproductor de Windows Media con Microsoft Visual Studio

Puede agregar el control Reproductor de Windows Media serie 9 o posterior ActiveX a una aplicación .NET Framework a través del cuadro de herramientas de Visual Studio.

## <a name="adding-the-windows-media-player-control"></a>Agregar el control Reproductor de Windows Media control

Antes de crear un proyecto, asegúrese de que la versión más reciente de Reproductor de Windows Media y el SDK Reproductor de Windows Media está instalado en el equipo.

Inicie Visual Studio y, a continuación, cree un nuevo proyecto.

En Visual Studio, abra el Cuadro de herramientas.

Si Reproductor de Windows Media no aparece en la **parte Componentes** del cuadro de herramientas, haga lo siguiente:

1.  Haga clic con el botón derecho en el cuadro de herramientas y, a continuación, **seleccione Elegir elementos**. Se abrirá el cuadro **de diálogo Personalizar cuadro** de herramientas .
2.  En la **pestaña Componentes COM,** seleccione Reproductor de Windows Media.

    Si Reproductor de Windows Media aparece en la lista, haga clic en Examinar y, a continuación, abra Wmp.dll, que debe estar en la carpeta \\ Windows System32.

3.  Haga clic en **Aceptar**. El Reproductor de Windows Media se colocará en la pestaña Cuadro de herramientas actual.

Ahora puede seleccionar Reproductor de Windows Media en el cuadro de herramientas y agregarlo a un formulario.

Visual Studio proporciona al Reproductor de Windows Media un nombre predeterminado, como "axWindowsMediaPlayer1". Es posible que quiera cambiar el nombre a algo más fácil de recordar, como "Player".

Al agregar Reproductor de Windows Media control desde el cuadro de herramientas también se agregan referencias a dos bibliotecas creadas por Visual Studio, AxWMPLib y WMPLib. Puede encontrarlos en la Explorador de soluciones en **Referencias**.

Para facilitar el uso de los objetos en el espacio de nombres Player, debe incluir el espacio de nombres en las directivas using o imports de los archivos, como se muestra a continuación:


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



La directiva garantiza que puede hacer referencia a objetos **player** sin calificar completamente sus nombres.

> [!Note]  
> El Reproductor de Windows Media es un **objeto AxWindowsMediaPlayer** del espacio **de nombres AxWMPLib.** Sin embargo, **la clase AxWindowsMediaPlayer** usa tipos de datos, interfaces y otros elementos del espacio **de nombres WMPLib.**

 

## <a name="configuring-visibility-of-the-control"></a>Configuración de la visibilidad del control

La primera vez que agregue Reproductor de Windows Media control a un formulario, estará visible. Si no desea usar la imagen visible del reproductor en la aplicación, oculte el reproductor predeterminado estableciendo cualquiera de las siguientes propiedades:



| Propiedad        | Valor                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | "invisible" (vea [Player.uiMode).](player-uimode.md) |
| **Visible**     | "false"                                               |
| **Size.Width**  | 0                                                     |
| **Size.Height** | 0                                                     |



 

Puede establecer estas propiedades en el  código o en la ventana Propiedades cuando el control Reproductor de Windows Media está seleccionado en el diseñador de formularios.

## <a name="object-model-compatibility-of-the-control"></a>Compatibilidad del modelo de objetos del control

El modelo de objetos para el control Reproductor de Windows Media es básicamente el mismo en el .NET Framework que en el código y el script no administrados. Sin embargo, hay diferencias en la forma en que se exponen los elementos:

-   La mayoría de los objetos se exponen bajo el nombre de su interfaz COM subyacente. Por ejemplo, el objeto **Playlist** se expone como **IWMPPlaylist.**
-   Algunas interfaces tienen versiones posteriores. Por ejemplo, se ha dado funcionalidad adicional a **IWMPMedia** en **IWMPMedia2** e **IWMPMedia3.** Si declara un objeto como **IWMPMedia**, normalmente tiene acceso a la funcionalidad de todas las versiones de la interfaz. Sin embargo, IntelliSense® no reconocerá los métodos ni las propiedades de las interfaces de versión posterior, y el editor de .NET de Visual Basic no corregirá automáticamente el uso de mayúsculas. Para obtener todas las ventajas de IntelliSense y otras características de Visual Studio, declare el objeto mediante la versión más reciente de la interfaz, como **IWMPMedia3**.
-   No hay propiedades indizadas (C#) ni propiedades predeterminadas (Visual Basic .NET). Por ejemplo, para recuperar **un elemento Playlist.item**, debe llamar al método de accessor **IWMPlaylist.get \_ Item** en C# o recuperar la propiedad **IWMPlayist.Item** en Visual Basic .NET.
-   Debido a un conflicto de nomenclatura entre la propiedad Reproductor de Windows Media **Controls** y la propiedad **Controls** expuesta por cada control, la versión Player de esta propiedad se denomina **CtlControls** en el contexto del control ActiveX. (Sin embargo, este no es el caso cuando se crea el reproductor mediante programación en lugar de como un control ActiveX).

Use el Explorador de objetos Visual Studio para buscar los nombres de API correctos para los métodos y objetos en los espacios de nombres **AxWMPLib** y **WMPLib.**

## <a name="distributing-your-application"></a>Distribuir la aplicación

Al distribuir la aplicación, asegúrese de instalar AxInterop.WMPLib.dll y Interop.WMPLib.dll en la carpeta de la aplicación. También deberá asegurarse de que la versión Reproductor de Windows Media necesaria está instalada en el equipo del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el control Reproductor de Windows Media mediante programación**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**Inserción del control Reproductor de Windows Media en una solución de C#**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**Inserción del control Reproductor de Windows Media en una Visual Basic de .NET**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




