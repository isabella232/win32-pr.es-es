---
title: Compilar la aplicación de ejemplo con Visual Studio
description: Compilar la aplicación de ejemplo con Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- aplicaciones de escritorio, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de aplicación de escritorio
- Administrador de dispositivos, ejemplo de aplicación de escritorio
- ejemplos, aplicaciones de escritorio
- ejemplos, compilar con Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075492"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Compilar la aplicación de ejemplo con Visual Studio

El SDK de Administrador de dispositivos de Windows Media incluye una solución de Visual Studio que es compatible con Microsoft Visual Studio 2005.

Antes de compilar la aplicación de ejemplo, debe cambiar el nombre del archivo de encabezado shtypes. h para evitar conflictos con un archivo con el mismo nombre que se encuentra en el SDK de la plataforma de Microsoft. Por ejemplo, podría cambiar el nombre de <*ruta de instalación del SDK* > \\ WMFSDK11 \\ incluir \\ shtypes. h a <*ruta de instalación del SDK* > \\ WMFSDK11 \\ incluir \\ shtypes. h. backup.

Para compilar la aplicación, inicie una instancia de Visual Studio 2005, abra el archivo de solución wmdmapp. sln, que se encuentra en la carpeta <*ruta de instalación del SDK* > \\ WMFSDK11 \\ apps \\ wmdmapp y elija la opción **compilar/compilar solución** . Esto creará dos archivos de proyecto: el proyecto auxiliar, proghelp. vcproj, así como la aplicación principal wmdmapp. vcproj. Además, se creará la DLL de aplicación auxiliar de progreso y la aplicación principal (WMDMApp.exe).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Aplicación de escritorio de ejemplo**](sample-desktop-application.md)
</dt> </dl>

 

 




