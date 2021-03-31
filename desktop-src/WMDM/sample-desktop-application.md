---
title: Aplicación de escritorio de ejemplo
description: Aplicación de escritorio de ejemplo
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- aplicaciones de escritorio, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de aplicación de escritorio
- Administrador de dispositivos, ejemplo de aplicación de escritorio
- aplicación de ejemplo wmdmapp
- ejemplos, aplicaciones de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418754"
---
# <a name="sample-desktop-application"></a>Aplicación de escritorio de ejemplo

Windows Media Administrador de dispositivos se suministra con una aplicación de escritorio de ejemplo denominada wmdmapp. Esta aplicación tiene una interfaz gráfica de usuario que le permite examinar los dispositivos conectados, crear listas de reproducción en el dispositivo y arrastrar archivos multimedia al dispositivo.

Esta aplicación de ejemplo consta de dos partes:

-   wmdapp.exe, un archivo ejecutable que muestra una ventana y realiza la mayor parte de la interfaz de usuario y la funcionalidad básica del programa.
-   proghelp.dll, un archivo DLL auxiliar que realiza funciones de utilidad para la aplicación. Debe registrar este archivo DLL después de compilar el proyecto.

Para compilar la aplicación de ejemplo, puede usar Visual Studio. En la siguiente sección se describe cómo hacerlo:

-   [Compilar la aplicación de ejemplo con Visual Studio](compiling-the-sample-application-using-visual-studio.md)

Después de compilar el proyecto, registre el archivo de proghelp.dll. Para registrar este archivo DLL, abra un símbolo del sistema y vaya al directorio que contiene este archivo DLL y escriba `regsvr32 proghelp.dll` .

 

 




