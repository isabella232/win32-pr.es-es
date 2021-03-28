---
description: Muestra cómo usar los métodos de la interfaz IFileOperationProgressSink para supervisar los detalles de las acciones de la interfaz IFileOperation.
title: Receptor de progreso de operación de archivo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082815"
---
# <a name="file-operation-progress-sink"></a>Receptor de progreso de operación de archivo

Muestra cómo usar los métodos de la interfaz [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) para supervisar los detalles de las acciones de la interfaz [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de FileOperationProgressSink](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde la ventana del símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **FileOperationProgressSink** .
2.  Escriba `msbuild FileOperationProgressSinkSample.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **FilesInUse** . Por ejemplo, la ruta de instalación predeterminada completa es `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .
2.  Haga doble clic en el icono del archivo FileOperationProgressSinkSample. sln para abrir el proyecto en Visual Studio.
    > [!Note]  
    > La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada. En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.
2.  En el símbolo del sistema, escriba `FileOperationProgressSinkSample.exe` o, en el explorador de Windows, haga doble clic en el icono de FileOperationProgressSinkSample.exe.

 

 



