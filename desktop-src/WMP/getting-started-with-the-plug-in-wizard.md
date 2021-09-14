---
title: Tareas iniciales con el Asistente para complementos
description: Tareas iniciales con el Asistente para complementos
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Reproductor de Windows Media complementos, asistente para instalar complementos
- complementos, asistente para instalar complementos
- compilar complementos, instalar el asistente para complementos
- Reproductor de Windows Media Asistente para complementos, instalar
- Asistente para instalar complementos
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068432"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Tareas iniciales con el Asistente para complementos

Para configurar el entorno de desarrollo para crear Reproductor de Windows Media complementos, debe instalar los siguientes elementos:

-   Microsoft Visual Studio .NET 2003 o posterior
-   Reproductor de Windows Media serie 9 o posterior
-   Windows SDK, que incluye el SDK Reproductor de Windows Media
-   Reproductor de Windows Media Asistente para complementos

## <a name="installing-the-wizard"></a>Instalación del asistente

Realice los pasos siguientes para instalar el Asistente para Reproductor de Windows Media complemento.

1.  Busque la carpeta donde instaló el SDK Windows. Expanda la carpeta para ver sus subcarpetas y vaya a Ejemplos \\ \\ asistentes de WMP multimedia \\ \\ wmpwiz.
2.  Busque los tres archivos siguientes:
    -   wmpwiz.vsz
    -   wmpwiz.vsdir
    -   wmpwiz.ico
3.  Con un editor de texto, como Bloc de notas, edite el archivo wmpwiz.vsz.

    Busque la línea siguiente:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Cambie `<VsWizardEngine version goes here>` a uno de los siguientes valores, en función de la versión de Visual Studio que haya instalado.

    

    | Value              | Versión de Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine.7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine.8.0 | Visual Studio 2005      |
    | VsWizardEngine.9.0 | Visual Studio 2008      |

    

     

    Busque la línea siguiente:

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Cambie `<path to wmpwiz directory goes here>` a la ruta de acceso donde se encuentran los archivos del asistente.

    Por ejemplo, supongamos que Visual Studio 2008 y los archivos del asistente están aquí: C: Archivos de programa SDK de Microsoft Windows asistentes multimedia WMP de ejemplos de \\ \\ \\ \\ v7.0 \\ \\ \\ \\ \\ wmpwiz. A continuación, el archivo wmpwiz.vsz tendría el siguiente aspecto:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Busque la carpeta donde instaló Visual Studio. Expanda la carpeta para ver sus subcarpetas y busque una carpeta denominada vcprojects.
5.  Copie los tres archivos enumerados en el paso 2 en la carpeta vcprojects. El asistente ya está instalado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un complemento](building-a-plug-in.md)
</dt> <dt>

[Uso del Asistente para complementos con Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




