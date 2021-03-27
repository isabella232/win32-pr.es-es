---
description: Muestra cómo implementar un verbo de Shell mediante los métodos ExplorerCommand y ExplorerCommandState.
title: Ejemplo de verbo Explorer Command
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912922"
---
# <a name="explorer-command-verb-sample"></a>Ejemplo de verbo Explorer Command

Muestra cómo implementar un verbo de Shell mediante los métodos ExplorerCommand y ExplorerCommandState.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de ExplorerCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **ExplorerCommandVerb** .
2.  Escriba `msbuild ExplorerCommandVerb.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **ExplorerCommandVerb** .
2.  Haga doble clic en el icono del archivo ExplorerCommandVerb. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el ExplorerCommandVerb.dll, mediante el símbolo del sistema o el explorador de Windows. Asegúrese de usar el archivo DLL de 64 bits en Windows de 64 bits.
2.  En la línea de comandos, escriba `regsvr32.exe ExplorerCommandVerb.dll` .
3.  Al hacer clic con el botón secundario en un archivo. txt, se mostrarán dos nuevos verbos en el menú contextual.

 

 



