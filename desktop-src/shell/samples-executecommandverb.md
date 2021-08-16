---
description: Muestra cómo implementar un verbo shell mediante el método ExecuteCommand.
title: Ejemplo de verbo Execute Command
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e32b472d63b9d2d779c97b64833f354e7d4d2eaed034d3a213ae4e101f7beb3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858274"
---
# <a name="execute-command-verb-sample"></a>Ejemplo de verbo Execute Command

Muestra cómo implementar un verbo shell mediante el método ExecuteCommand.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)

## <a name="description"></a>Descripción

Este método es el preferido para las implementaciones de verbo porque proporciona la mayor flexibilidad, es sencillo y admite la activación fuera de proceso. En este ejemplo se implementa un objeto de modelo de objetos componentes (COM) de servidor local independiente, pero se espera que la implementación del verbo se integre en las aplicaciones existentes. Para ello, el objeto de aplicación principal debe registrar un generador de clases para sí mismo. Ese objeto implementa [**IDropTarget para**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) los verbos de la aplicación. Tenga en cuenta que COM inicia la aplicación si aún no se está ejecutando, pero se conecta a una instancia en ejecución de la aplicación si hay una.

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7,0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo ExecuteCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **ExecuteCommandVerb.**
2.  Escriba `msbuild ExecuteCommand.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra Windows explorador y vaya al directorio del proyecto **ExecuteCommandVerb.**
2.  Haga doble clic en el icono del archivo ExecuteCommand.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorer.
2.  En la línea de comandos, escriba `ExecuteCommand.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de ExecuteCommand.exe.
3.  Siga las instrucciones del cuadro de diálogo que se muestra.

 

 
