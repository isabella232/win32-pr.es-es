---
title: Introducción con el Asistente para complementos
description: Introducción con el Asistente para complementos
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Complementos de Windows Media Player, instalación del Asistente para complementos
- complementos, Asistente para instalar complementos
- crear complementos, Asistente para instalar complementos
- Asistente para complementos de Windows Media Player, instalar
- instalación del Asistente para complementos
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994436"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Introducción con el Asistente para complementos

Para configurar el entorno de desarrollo para crear complementos de Media Player de Windows, debe instalar los siguientes elementos:

-   Microsoft Visual Studio .NET 2003 o posterior
-   Windows Media Player 9 series o posterior
-   Windows SDK, que incluye el SDK de Windows Media Player
-   Asistente para complementos de Media Player de Windows

## <a name="installing-the-wizard"></a>Instalación del asistente

Realice los pasos siguientes para instalar el Asistente para complementos de Windows Media Player.

1.  Busque la carpeta en la que instaló el Windows SDK. Expanda la carpeta para ver sus subcarpetas y vaya a ejemplos \\ multimedia \\ WMP \\ asistentes \\ wmpwiz.
2.  Busque los tres archivos siguientes:
    -   wmpwiz. vsz
    -   wmpwiz. vsdir
    -   wmpwiz. ico
3.  Con un editor de texto, como el Bloc de notas, edite el archivo wmpwiz. vsz.

    Busque la línea siguiente:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Cambie `<VsWizardEngine version goes here>` a uno de los valores siguientes, en función de la versión de Visual Studio que tenga instalada.

    

    | Value              | Versión de Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine. 7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine. 8.0 | Visual Studio 2005      |
    | VsWizardEngine. 9.0 | Visual Studio 2008      |

    

     

    Busque la línea siguiente:

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Cambie `<path to wmpwiz directory goes here>` a la ruta de acceso donde se encuentran los archivos del asistente.

    Por ejemplo, supongamos que tiene Visual Studio 2008 y que los archivos del asistente están aquí: C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples multimedia de los \\ asistentes de \\ \\ \\ wmpwiz. El archivo wmpwiz. vsz tendrá el siguiente aspecto:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Busque la carpeta en la que instaló Visual Studio. Expanda la carpeta para ver sus subcarpetas y busque una carpeta denominada VCProjects.
5.  Copie los tres archivos enumerados en el paso 2 en la carpeta VCProjects. El asistente ya está instalado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar un complemento](building-a-plug-in.md)
</dt> <dt>

[Usar el Asistente para complementos con Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




