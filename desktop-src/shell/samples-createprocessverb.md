---
description: Muestra cómo implementar un verbo shell mediante el método CreateProcess.
title: Ejemplo de verbo CreateProcess
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c0af34d5ec9f687ec6c58bb73f337b38d512527c0ace4bd20eae12d49c87a62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858345"
---
# <a name="createprocess-verb-sample"></a>Ejemplo de verbo CreateProcess

Muestra cómo implementar un verbo shell mediante el método CreateProcess.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)

## <a name="description"></a>Descripción

Los verbos basados en CreateProcess dependen de ejecutar un ejecutable y de pasarlo un argumento de línea de comandos. Este método no es tan eficaz como los métodos DropTarget y ExecuteCommand, pero logra el comportamiento fuera de proceso deseable.

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de desarrollo de software de Windows (SDK) | 7,0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo CreateProcessVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo desde el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto **CreateProcessVerb.**
2.  Escriba `msbuild CreateProcessVerb.sln`.

Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):

1.  Abra Windows explorador y vaya al directorio del proyecto **CreateProcessVerb.**
2.  Haga doble clic en el icono del archivo CreateProcessVerb.sln para abrir el proyecto en Visual Studio.
3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorer.
2.  En la línea de comandos, escriba `CreateProcessVerb.exe` . Como alternativa, en Windows Explorer haga doble clic en el icono de CreateProcessVerb.exe.
3.  Siga las instrucciones del cuadro de diálogo que se muestra.

 

 



