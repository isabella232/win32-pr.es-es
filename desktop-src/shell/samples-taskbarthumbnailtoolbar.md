---
description: Muestra una barra de herramientas en miniatura, un control de barra de herramientas activo insertado en la vista previa de miniaturas de una ventana, que se usa para proporcionar acceso a los comandos clave de una ventana sin hacer que el usuario restaure o active la ventana de la aplicación.
title: Ejemplo de barra de herramientas de miniaturas de la barra de tareas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: cd16ee40bfb480b3e7eacef2bc4681e61fdb24ace1ac68985e2016ce11b7c0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219634"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a>Ejemplo de barra de herramientas de miniaturas de la barra de tareas

Muestra una barra de herramientas en miniatura, un control de barra de herramientas activo insertado en la vista previa de miniaturas de una ventana, que se usa para proporcionar acceso a los comandos clave de una ventana sin hacer que el usuario restaure o active la ventana de la aplicación.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestra cómo proporcionar una barra de herramientas sencilla a una vista previa de miniaturas de la barra de tareas. La barra de herramientas consta de tres botones. Al hacer clic en un botón se muestra una ventana para confirmar que el botón se ha activado. Se muestran las SIGUIENTES API:

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**Estructura THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7,0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo taskbarThumbnailToolbar](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **TaskbarThumbnailToolbar.**
2.  Escriba `msbuild ThumbnailToolbar.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows explorador de herramientas y vaya al directorio del proyecto **TaskbarThumbnailToolbar.**
2.  Haga doble clic en el icono del archivo ThumbnailToolbar.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo archivo ejecutable (por ejemplo, ), mediante el símbolo del `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` sistema o Windows Explorer.

    -   Si usa la línea de comandos, escriba `ThumbnailToolbar.exe` .
    -   Si usa Windows Explorer, haga doble clic en el icono de ThumbnailToolbar.exe.

    Se abrirá una nueva ventana, con un botón de la barra de tareas asociado.

2.  Mantenga el cursor sobre el botón de la barra de **tareas ThumbnailToolbar** para que se muestre la vista previa. Haga clic en uno de los tres botones (verde, amarillo y rojo) que se muestran en la barra de herramientas de la vista previa.
3.  Elija **Salir** en el menú Archivo **de la** ventana para finalizar el programa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensiones de la barra de tareas](taskbar-extensions.md)
</dt> </dl>

 

 



