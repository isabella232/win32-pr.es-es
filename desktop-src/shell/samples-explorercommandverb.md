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
ms.openlocfilehash: 3ec8f4c88ea01aad410e982fc24fd248f3c1826d8c8657e904844b535e621fd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719187"
---
# <a name="explorer-command-verb-sample"></a>Ejemplo de verbo Explorer Command

Muestra cómo implementar un verbo de Shell mediante los métodos ExplorerCommand y ExplorerCommandState.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7,0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo ExplorerCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **ExplorerCommandVerb.**
2.  Escriba `msbuild ExplorerCommandVerb.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows explorador y vaya al directorio del proyecto **ExplorerCommandVerb.**
2.  Haga doble clic en el icono del archivo ExplorerCommandVerb.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el ExplorerCommandVerb.dll, mediante el símbolo del sistema o Windows Explorador. Asegúrese de usar el archivo DLL de 64 bits en archivos de 64 Windows.
2.  En la línea de comandos, escriba `regsvr32.exe ExplorerCommandVerb.dll` .
3.  Se mostrarán dos verbos nuevos en el menú contextual al hacer clic con el botón derecho en .txt archivo.

 

 



