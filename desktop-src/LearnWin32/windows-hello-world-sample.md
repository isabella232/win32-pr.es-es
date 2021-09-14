---
title: Windows Hello Ejemplo de mundo
description: En esta aplicación de ejemplo se muestra cómo crear un programa Windows mínimo.
ms.assetid: ec316ad8-d01d-4558-91b6-19fdbba3d520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932d3b0c524c643022904b08402507d4a603adb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159917"
---
# <a name="windows-hello-world-sample"></a>Windows Hello Ejemplo de mundo

En esta aplicación de ejemplo se muestra cómo crear un programa Windows mínimo.

## <a name="description"></a>Descripción

La Windows Hello de ejemplo world crea y muestra una ventana vacía, como se muestra en la captura de pantalla siguiente. Este ejemplo se describe en [el módulo 1. Su primer Windows programa](your-first-windows-program.md).

![captura de pantalla del programa de ejemplo.](images/window01.png)

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible [aquí.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/HelloWorld)

Para descargarlo, vaya a la raíz del repositorio de ejemplo en GitHub[(microsoft/Windows-classic-samples)](https://github.com/microsoft/Windows-classic-samples/)y haga clic en el botón Clonar o descargar para descargar el archivo ZIP de todos los ejemplos en el equipo.  A continuación, descomprima la carpeta.

Para abrir el ejemplo en Visual Studio, seleccione Archivo / Abrir **/ Project / Solución** y vaya a la ubicación en la que descomprimió la carpeta y **Windows-classic-samples-master / Samples / Win7Samples / begin / LearnWin32 / HelloWorld / cpp**. Abra el archivo **HelloWorld.sln**.

Una vez cargado el ejemplo, deberá actualizarlo para que funcione con Windows 10. En el **Project** de Visual Studio, seleccione **Propiedades.** Actualice la **versión Windows SDK** a un SDK de Windows 10, como 10.0.17763.0 o una versión posterior. A **continuación,** cambie Conjunto de herramientas de Visual Studio 2017 o una versión posterior. Ahora puede ejecutar el ejemplo presionando F5.


## <a name="related-topics"></a>Temas relacionados

* [Aprender a programar para Windows: código de ejemplo](learn-to-program-for-windows--sample-code.md)
* [Módulo 1. Su primer Windows programa](your-first-windows-program.md)
