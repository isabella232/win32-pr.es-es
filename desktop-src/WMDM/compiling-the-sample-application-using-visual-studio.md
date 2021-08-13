---
title: Compilar la aplicación de ejemplo mediante Visual Studio
description: Compilar la aplicación de ejemplo mediante Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Archivos Administrador de dispositivos,ejemplos
- Administrador de dispositivos,samples
- aplicaciones de escritorio, ejemplos
- Windows Ejemplo de Administrador de dispositivos multimedia, aplicación de escritorio
- Administrador de dispositivos ejemplo de aplicación de escritorio
- ejemplos, aplicaciones de escritorio
- ejemplos, compilación mediante Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8b32cd5931a88bc41b8eee7171b6ab4ab18b629a8108007d68094180efaa77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586256"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Compilar la aplicación de ejemplo mediante Visual Studio

El SDK Windows Media Administrador de dispositivos incluye una Visual Studio que es compatible con Microsoft Visual Studio 2005.

Antes de compilar la aplicación de ejemplo, debe cambiar el nombre del archivo de encabezado shtypes.h para evitar conflictos con un archivo del mismo nombre que se encuentra en el SDK de plataforma de Microsoft. Por ejemplo, puede cambiar el nombre de la ruta de instalación del *SDK* de > \\ <WMFSDK11 \\ include \\ shtypes.h a <*SDK Installation Path* > \\ WMFSDK11 include \\ \\ shtypes.h.backup.

Para compilar la aplicación, inicie una instancia de Visual Studio 2005, abra el archivo de solución wmdmapp.sln, que se encuentra en la carpeta ruta de instalación del *SDK* de <> \\ WMFSDK11 aplicaciones \\ \\ wmdmapp  y elija la opción Compilar o compilar solución. Esto creará dos archivos de proyecto: el proyecto auxiliar, proghelp.vcproj, así como la aplicación principal wmdmapp.vcproj. Además, creará el archivo DLL del asistente de progreso y la aplicación principal (WMDMApp.exe).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Aplicación de escritorio de ejemplo**](sample-desktop-application.md)
</dt> </dl>

 

 




