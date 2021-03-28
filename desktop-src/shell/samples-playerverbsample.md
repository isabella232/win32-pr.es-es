---
description: Muestra cómo crear un verbo que opera en elementos de Shell y contenedores que reproducen elementos o agregan elementos a una cola.
title: Ejemplo de verbo del reproductor
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277226"
---
# <a name="player-verb-sample"></a>Ejemplo de verbo del reproductor

Muestra cómo crear un verbo que opera en elementos de Shell y contenedores que reproducen elementos o agregan elementos a una cola. Este ejemplo es especialmente útil para las aplicaciones multimedia.

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
| GitHub  | [Ejemplo de PlayerVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **PlayerVerbSample** .
2.  Escriba `msbuild PlayerVerbSample.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto **PlayerVerbSample** .
2.  Haga doble clic en el icono del archivo PlayerVerbSample. sln para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.
2.  En la línea de comandos, escriba `PlayerVerbSample.exe` . Como alternativa, en el explorador de Windows, haga doble clic en el icono de PlayerVerbSample.exe.
3.  Seleccione `Register Verbs` en el cuadro de diálogo de **ejemplo del verbo de reproductor** .
4.  Haga clic con el botón secundario en elementos de imagen (archivo, carpeta o pila) en el explorador de Windows para agregarlos a una cola o reproducirlos en la aplicación de ejemplo. Usar elementos de música al cambiar el ejemplo para trabajar con música.

 

 



