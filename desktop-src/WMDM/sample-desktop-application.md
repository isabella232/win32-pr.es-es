---
title: Aplicación de escritorio de ejemplo
description: Aplicación de escritorio de ejemplo
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Media Administrador de dispositivos,samples
- Administrador de dispositivos,samples
- aplicaciones de escritorio, ejemplos
- Windows Ejemplo de Administrador de dispositivos multimedia, aplicación de escritorio
- Administrador de dispositivos ejemplo de aplicación de escritorio
- Aplicación de ejemplo wmdmapp
- ejemplos, aplicaciones de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474577"
---
# <a name="sample-desktop-application"></a>Aplicación de escritorio de ejemplo

La Windows media Administrador de dispositivos incluye una aplicación de escritorio de ejemplo denominada wmdmapp. Esta aplicación tiene una interfaz gráfica de usuario que permite examinar los dispositivos conectados, crear listas de reproducción en el dispositivo y arrastrar archivos multimedia al dispositivo.

Esta aplicación de ejemplo consta de dos partes:

-   wmdapp.exe, un ejecutable que muestra una ventana y realiza la mayor parte de la interfaz de usuario y la funcionalidad básica del programa, y
-   proghelp.dll, un archivo DLL auxiliar que realiza funciones de utilidad para la aplicación. Debe registrar este archivo DLL después de compilar el proyecto.

Para compilar la aplicación de ejemplo, puede usar Visual Studio. En la sección siguiente se describe cómo se hace esto:

-   [Compilación de la aplicación de ejemplo mediante Visual Studio](compiling-the-sample-application-using-visual-studio.md)

Después de compilar el proyecto, registre el proghelp.dll archivo. Para registrar este archivo DLL, abra un símbolo del sistema y vaya al directorio que contiene este archivo DLL y escriba `regsvr32 proghelp.dll` .

 

 




