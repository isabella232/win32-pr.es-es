---
description: Muestra las superposiciones de los iconos de la barra de tareas y las barras de progreso.
title: Ejemplo de estado periférico de la barra de tareas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997889"
---
# <a name="taskbar-peripheral-status-sample"></a>Ejemplo de estado periférico de la barra de tareas

Muestra las superposiciones de los iconos de la barra de tareas y las barras de progreso.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

Este ejemplo crea un botón de la barra de tareas de ejemplo en el que se muestra el uso de [**ITaskbarList3:: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) permitiéndole aplicar varias superposiciones elegidas en un menú.

El ejemplo también proporciona la opción de simular un indicador de progreso en el botón, mostrando el uso de [**ITaskbarList3:: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) y [**ITaskbarList3:: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) al mostrar en primer lugar un indicador de progreso indeterminado (TBPF \_ indeterminado) y, a continuación, un indicador proporcional normal (TBPF \_ normal).

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de TaskBarPeripheralStatus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **TaskbarPeripheralStatus** .
2.  Escriba `msbuild PeripheralStatus.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **TaskbarPeripheralStatus** .
2.  Haga doble clic en el icono del archivo PeripheralStatus. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo archivo ejecutable (por ejemplo, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` ), mediante el símbolo del sistema o el explorador de Windows.

    -   Si usa la línea de comandos, escriba `PeripheralStatus.exe` .
    -   Si usa el explorador de Windows, haga doble clic en el icono de PeripheralStatus.exe.

    Se abrirá una nueva ventana con un botón de la barra de tareas asociado.

2.  Para mostrar las superposiciones, elija **superposición 1** o **superposición 2** en el menú de **Estado de periféricos** de la ventana. La superposición elegida aparece en el botón de la barra de tareas. Para quitar la superposición, elija **Borrar superposición**.
3.  Para mostrar la barra de progreso, elija **simular progreso** en el menú de **Estado de periféricos** de la ventana. El botón de la barra de tareas mostrará un indicador de progreso indeterminado y cambiará a un indicador normal.
4.  Elija **salir** en el menú **archivo** de la ventana para finalizar el programa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensiones de la barra de tareas](taskbar-extensions.md)
</dt> </dl>

 

 



