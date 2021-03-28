---
description: Muestra cómo implementar un verbo de Shell mediante el método DropTarget.
title: Ejemplo de verbo DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985627"
---
# <a name="droptarget-verb-sample"></a>Ejemplo de verbo DropTarget

Muestra cómo implementar un verbo de Shell mediante el método DropTarget.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)

## <a name="description"></a>Descripción

Este ejemplo muestra cómo implementar un verbo de Shell mediante el método DropTarget. Este método es preferible para implementaciones de verbo que deben funcionar en Windows XP. En este ejemplo se implementa un objeto de modelo de objetos componentes (COM) de servidor local independiente, pero se espera que la implementación del verbo se integre en las aplicaciones existentes. Para ello, el objeto de aplicación principal registra un generador de clases para sí mismo. Ese objeto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para los verbos de la aplicación. Tenga en cuenta que COM inicia la aplicación si aún no se está ejecutando pero se conecta a una instancia en ejecución de la aplicación si hay alguna.

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de DropTargetVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **DropTargetVerb** .
2.  Escriba `msbuild DropTargetVerb.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **DropTargetVerb** .
2.  Haga doble clic en el icono del archivo DropTargetVerb. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.
2.  En la línea de comandos, escriba `DropTargetVerb.exe` . Como alternativa, en el explorador de Windows, haga doble clic en el icono de DropTargetVerb.exe.
3.  Siga las instrucciones del cuadro de diálogo que aparece

 

 
