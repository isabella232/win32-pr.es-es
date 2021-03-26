---
description: Muestra una barra de herramientas en miniatura, un control de barra de herramientas activo incrustado en la vista previa en miniatura de una ventana, que se usa para proporcionar acceso a los comandos clave de una ventana sin hacer que el usuario restaure o Active la ventana de la aplicación.
title: Ejemplo de barra de herramientas de miniaturas de la barra de tareas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985822"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a>Ejemplo de barra de herramientas de miniaturas de la barra de tareas

Muestra una barra de herramientas en miniatura, un control de barra de herramientas activo incrustado en la vista previa en miniatura de una ventana, que se usa para proporcionar acceso a los comandos clave de una ventana sin hacer que el usuario restaure o Active la ventana de la aplicación.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestra cómo proporcionar una barra de herramientas simple a una vista previa en miniatura de la barra de tareas. La barra de herramientas consta de tres botones. Al hacer clic en un botón, se muestra una ventana para confirmar que se activó el botón. Se muestran las siguientes API:

-   [**ITaskbarList3:: ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3:: ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   Estructura [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de TaskbarThumbnailToolbar](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **TaskbarThumbnailToolbar** .
2.  Escriba `msbuild ThumbnailToolbar.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **TaskbarThumbnailToolbar** .
2.  Haga doble clic en el icono del archivo ThumbnailToolbar. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo archivo ejecutable (por ejemplo, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` ), mediante el símbolo del sistema o el explorador de Windows.

    -   Si usa la línea de comandos, escriba `ThumbnailToolbar.exe` .
    -   Si usa el explorador de Windows, haga doble clic en el icono de ThumbnailToolbar.exe.

    Se abrirá una nueva ventana con un botón de la barra de tareas asociado.

2.  Mantenga el cursor sobre el botón de la barra de tareas **ThumbnailToolbar** para que se muestre la vista previa. Haga clic en uno de los tres botones (verde, amarillo, rojo) que se muestra en la barra de herramientas de la vista previa.
3.  Elija **salir** en el menú **archivo** de la ventana para finalizar el programa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensiones de la barra de tareas](taskbar-extensions.md)
</dt> </dl>

 

 



