---
description: Muestra cómo usar los métodos de interfaz IFileOperationProgressSink para supervisar los detalles de las acciones de la interfaz IFileOperation.
title: Receptor de progreso de operación de archivo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fe0ba5c86fdb2df5fe168559aa019941897563823e75670b0813ecb7e9e44d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820355"
---
# <a name="file-operation-progress-sink"></a>Receptor de progreso de operación de archivo

Muestra cómo usar los métodos de interfaz [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) para supervisar los detalles de las acciones de la interfaz [**IFileOperation.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation)

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo FileOperationProgressSink](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde la ventana del símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **FileOperationProgressSink.**
2.  Escriba `msbuild FileOperationProgressSinkSample.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra Windows Explorador de aplicaciones y vaya al **directorio del proyecto FilesInUse.** Por ejemplo, la ruta de instalación predeterminada completa es `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .
2.  Haga doble clic en el icono del archivo FileOperationProgressSinkSample.sln para abrir el proyecto en Visual Studio.
    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o Windows Explorador.
2.  En el símbolo del sistema, escriba , o en Windows Explorer, haga doble clic en `FileOperationProgressSinkSample.exe` el icono de FileOperationProgressSinkSample.exe.

 

 



