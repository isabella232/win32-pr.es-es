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
ms.openlocfilehash: ae9ae3edb2d993f2e42a2556899d45cb3b10722fc7d7a9dc5e9786560fc3078f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719537"
---
# <a name="droptarget-verb-sample"></a>Ejemplo de verbo DropTarget

Muestra cómo implementar un verbo de Shell mediante el método DropTarget.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)

## <a name="description"></a>Descripción

En este ejemplo se muestra cómo implementar un verbo de Shell mediante el método DropTarget. Este método es el preferido para las implementaciones de verbo que deben funcionar en Windows XP. En este ejemplo se implementa un objeto del Modelo de objetos componentes (COM) del servidor local independiente, pero se espera que la implementación del verbo se integre en las aplicaciones existentes. Para ello, el objeto de aplicación principal registra un generador de clases por sí mismo. Ese objeto implementa [**IDropTarget para**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) los verbos de la aplicación. Tenga en cuenta que COM inicia la aplicación si aún no se está ejecutando, pero se conecta a una instancia en ejecución de la aplicación si hay una.

## <a name="requirements"></a>Requisitos



| Product                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de DropTargetVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al **directorio del proyecto DropTargetVerb.**
2.  Escriba `msbuild DropTargetVerb.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows Explorador de aplicaciones y vaya al **directorio del proyecto DropTargetVerb.**
2.  Haga doble clic en el icono del archivo DropTargetVerb.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorador.
2.  En la línea de comandos, escriba `DropTargetVerb.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de DropTargetVerb.exe.
3.  Siga las instrucciones del cuadro de diálogo que se muestra.

 

 
