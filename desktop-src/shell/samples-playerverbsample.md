---
description: Muestra cómo crear un verbo que funcione en contenedores y elementos de Shell que reproduce elementos o agrega elementos a una cola.
title: Ejemplo de verbo del reproductor
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a338bef9e06a7d5f4f17afad48037b95b8f1883cf60debadc0a4c5e3f2e34e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677433"
---
# <a name="player-verb-sample"></a>Ejemplo de verbo del reproductor

Muestra cómo crear un verbo que funcione en contenedores y elementos de Shell que reproduce elementos o agrega elementos a una cola. Este ejemplo es especialmente útil para aplicaciones multimedia.

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

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de PlayerVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio **del proyecto PlayerVerbSample.**
2.  Escriba `msbuild PlayerVerbSample.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida):

1.  Abra Windows explorador y vaya al directorio **del proyecto PlayerVerbSample.**
2.  Haga doble clic en el icono del archivo PlayerVerbSample.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable mediante el símbolo del sistema o Windows Explorador.
2.  En la línea de comandos, escriba `PlayerVerbSample.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de PlayerVerbSample.exe.
3.  Seleccione `Register Verbs` en el cuadro de diálogo Ejemplo de verbo **del** reproductor.
4.  Haga clic con el botón derecho en elementos de imagen (archivo, carpeta o pila) en Windows Explorer para agregarlos a una cola o reproducirlos en la aplicación de ejemplo. Use elementos de música al cambiar el ejemplo para trabajar con música.

 

 



