---
description: Muestra cómo crear un verbo que funcione en un contenedor o elemento de Shell seleccionado para crear una lista de reproducción.
title: Ejemplo de creador de listas de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 086cb0f3fbb4cb009cd156013ce3ea16a2a7dee3b2346824d51b79094c06c45e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592895"
---
# <a name="playlist-creator-sample"></a>Ejemplo de creador de listas de reproducción

Muestra cómo crear un verbo que funcione en un contenedor o elemento de Shell seleccionado para crear una lista de reproducción.

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
| GitHub  | [Ejemplo de PlaylistCreator](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **PlaylistCreator.**
2.  Escriba `msbuild PlaylistCreator.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

> [!Note]  
> Este ejemplo también se puede usar con la Visual C++ Express Edition si el Visual Studio completo no está disponible.

 

1.  Abra Windows explorador y vaya al directorio del proyecto **PlaylistCreator.**
2.  Haga doble clic en el icono del archivo PlaylistCreator.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.
    > [!Note]  
    > Si está compilando 64 bits con Visual C++ Express Edition, debe usar el compilador cruzado x64 proporcionado con el SDK de Windows.

     

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorer.
2.  En la línea de comandos, escriba `PlaylistCreator.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de PlaylistCreator.exe.
3.  Haga clic con el botón derecho en cualquier archivo de música o carpeta que contenga archivos de música en Windows Explorer para crear una lista de reproducción para abrir el menú contextual.
4.  Puede crear una lista de reproducción .m3u o .wpl. Las listas de reproducción se crean en la `%userprofile%\Music\Playlists` carpeta .
    > [!Note]  
    > Los verbos nuevos del menú contextual se pueden encontrar en la carpeta **Música,** pilas de música, pilas de la biblioteca **Música y** colecciones de archivos de música.

     

 

 



