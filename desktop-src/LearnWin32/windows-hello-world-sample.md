---
title: Ejemplo de Hola mundo de Windows
description: En esta aplicación de ejemplo se muestra cómo crear un programa de Windows mínimo.
ms.assetid: ec316ad8-d01d-4558-91b6-19fdbba3d520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932d3b0c524c643022904b08402507d4a603adb
ms.sourcegitcommit: e084958628fb997e9e11fe08574d82edbba07dbf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2019
ms.locfileid: "104357818"
---
# <a name="windows-hello-world-sample"></a>Ejemplo de Hola mundo de Windows

En esta aplicación de ejemplo se muestra cómo crear un programa de Windows mínimo.

## <a name="description"></a>Descripción

La aplicación de ejemplo de Windows Hola mundo crea y muestra una ventana vacía, tal y como se muestra en la captura de pantalla siguiente. Este ejemplo se describe en el [módulo 1. Su primer programa de Windows](your-first-windows-program.md).

![captura de pantalla del programa de ejemplo.](images/window01.png)

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible [aquí](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/HelloWorld).

Para descargarlo, vaya a la raíz del repositorio de ejemplo en GitHub ([Microsoft/Windows-Classic-samples](https://github.com/microsoft/Windows-classic-samples/)) y haga clic en el botón **clonar o descargar** para descargar el archivo zip de todos los ejemplos en el equipo. A continuación, descomprima la carpeta.

Para abrir el ejemplo en Visual Studio, seleccione **archivo/Abrir/proyecto/solución** y navegue hasta la ubicación en la que descomprimió la carpeta y **Windows-Classic-samples-Master/samples/Win7Samples/Begin/LearnWin32/HelloWorld/CPP**. Abra el archivo **HelloWorld. sln**.

Una vez que se haya cargado el ejemplo, deberá actualizarlo para que funcione con Windows 10. En el menú **proyecto** de Visual Studio, seleccione **propiedades**. Actualice la **versión de Windows SDK** a un SDK de Windows 10, como 10.0.17763.0 o superior. A continuación, cambie el **conjunto de herramientas** de la plataforma a Visual Studio 2017 o superior. Ahora puede ejecutar el ejemplo presionando F5.


## <a name="related-topics"></a>Temas relacionados

* [Aprender a programar para Windows: código de ejemplo](learn-to-program-for-windows--sample-code.md)
* [Módulo 1. Su primer programa de Windows](your-first-windows-program.md)
