---
description: Muestra cómo personalizar el cuadro de diálogo Archivo en uso para mostrar información adicional y opciones para los archivos que están abiertos actualmente en la aplicación.
title: Ejemplo de File Is In Use
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 27e0a216aed33d7b0295303539c6f46e489b4c4cba37fa7aedf0a7f2eddd7b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968804"
---
# <a name="file-is-in-use-sample"></a>Ejemplo de File Is In Use

Muestra cómo personalizar el cuadro de **diálogo Archivo** en uso para mostrar información adicional y opciones para los archivos que están abiertos actualmente en la aplicación.

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



 

Para obtener requisitos adicionales, vea el archivo IFileIsInUse \_sample.docx incluido con el ejemplo.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo FileIsInUse](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde la ventana del símbolo del sistema:

1.  Abra la ventana símbolo del sistema y vaya al directorio **del proyecto FileIsInUse.**
2.  Escriba `msbuild FileIsInUse.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra Windows Explorador de aplicaciones y vaya al **directorio del proyecto FilesInUse.** Por ejemplo, la ruta de instalación predeterminada completa es `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .
2.  Haga doble clic en el icono del archivo FileIsInUseSample.sln para abrir el proyecto en Visual Studio.
    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o Windows Explorador.
2.  En el símbolo del sistema, escriba , o en Windows Explorer, haga doble clic en `FileIsInUseSample.exe` el icono de FileIsInUseSample.exe.

Para obtener información detallada sobre este ejemplo de código, vea el archivosample.docx IFileIsInUse \_ incluido con el ejemplo.

 

 



