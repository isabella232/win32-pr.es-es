---
title: Instalación del Asistente para proyectos
description: Instalación del Asistente para proyectos
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player tiendas en línea, Complementos
- tiendas en línea, Complementos
- tipo 2 tiendas en línea, Complementos
- Windows Media Player tiendas en línea, Asistente para complementos
- tiendas en línea, Asistente para complementos
- tipo 2 tiendas en línea, Asistente para complementos
- Windows Media Player tiendas en línea, Asistente para proyectos
- tiendas en línea, Asistente para proyectos
- tipo 2 tiendas en línea, Asistente para proyectos
- Windows Media Player tiendas en línea, instalar el Asistente para complementos
- tiendas en línea, Asistente para instalar complementos
- tipo 2 tiendas en línea, Asistente para instalar complementos
- Windows Media Player tiendas en línea, instalación del Asistente para proyectos
- tiendas en línea, instalación del Asistente para proyectos
- tipo 2 tiendas en línea, instalación del Asistente para proyectos
- complementos, Windows Media Player tiendas en línea
- complementos, tiendas en línea
- complementos, tipo 2 tiendas en línea
- complementos, Asistente para instalar complementos
- complementos, Asistente para complementos
- complementos, instalación del Asistente para proyectos
- complementos, Asistente para proyectos
- Complementos de Windows Media Player, escriba 2 tiendas en línea
- Complementos de Windows Media Player, tiendas en línea
- Complementos de Windows Media Player, Windows Media Player tiendas en línea
- Complementos de Windows Media Player, instalación del Asistente para complementos
- Complementos de Windows Media Player, Asistente para complementos
- Complementos de Windows Media Player, instalación del Asistente para proyectos
- Complementos de Windows Media Player, Asistente para proyectos
- instalación del Asistente para complementos
- Asistente para complementos
- instalación del Asistente para proyectos
- Asistente para proyectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777526"
---
# <a name="installing-the-project-wizard"></a>Instalación del Asistente para proyectos

Para configurar el entorno de desarrollo para crear complementos de tienda en línea de tipo 2, debe instalar los siguientes elementos:

-   Microsoft Visual Studio .NET 2003 o posterior
-   Windows Media Player 9 series o posterior
-   Windows SDK, que incluye el SDK de Windows Media Player
-   Asistente para complementos de tienda en línea

## <a name="installing-the-wizard"></a>Instalación del asistente

Siga estos pasos para instalar el Asistente para complementos de tienda en línea en Visual Studio.

1.  Busque la carpeta en la que instaló el Windows SDK. Expanda la carpeta para ver sus subcarpetas y vaya a samples \\ multimedia \\ WMP \\ Wizards \\ Services.
2.  Busque los tres archivos siguientes:
    -   wmpservices. vsz
    -   wmpservices. vsdir
    -   wmpservices. ico
3.  Con un editor de texto como el Bloc de notas, edite el archivo wmpservices. vsz.

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
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Cambie `<path to wmpservices directory goes here>` a la ruta de acceso donde se encuentran los archivos del asistente.

    Por ejemplo, supongamos que tiene Visual Studio 2008 y que los archivos del asistente están aquí: C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples multimedia de los servicios de los \\ \\ \\ asistentes \\ . El archivo wmpservices. vsz tendrá el siguiente aspecto:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Busque la carpeta en la que instaló Visual Studio. Expanda la carpeta para ver sus subcarpetas y busque una carpeta denominada VCProjects.
5.  Copie los tres archivos enumerados en el paso 2 en la carpeta VCProjects. El asistente ya está instalado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Compilar el complemento para una tienda en línea de tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




