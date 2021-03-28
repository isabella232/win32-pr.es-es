---
description: Muestra cómo implementar un verbo de Shell mediante el método CreateProcess.
title: Ejemplo de verbo CreateProcess
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985826"
---
# <a name="createprocess-verb-sample"></a>Ejemplo de verbo CreateProcess

Muestra cómo implementar un verbo de Shell mediante el método CreateProcess.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)

## <a name="description"></a>Descripción

Los verbos basados en CreateProcess dependen de la ejecución de un ejecutable y de su pasa un argumento de línea de comandos. Este método no es tan eficaz como los métodos DropTarget y ExecuteCommand, pero logra el comportamiento deseado fuera de proceso.

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de CreateProcessVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **CreateProcessVerb** .
2.  Escriba `msbuild CreateProcessVerb.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **CreateProcessVerb** .
2.  Haga doble clic en el icono del archivo CreateProcessVerb. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.
2.  En la línea de comandos, escriba `CreateProcessVerb.exe` . Como alternativa, en el explorador de Windows, haga doble clic en el icono de CreateProcessVerb.exe.
3.  Siga las instrucciones del cuadro de diálogo que aparece

 

 



