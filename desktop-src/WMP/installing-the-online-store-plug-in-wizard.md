---
title: Instalación del Asistente para complementos de la tienda en línea
description: Instalación del Asistente para complementos de la tienda en línea
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Reproductor de Windows Media en línea, complementos
- tiendas en línea, complementos
- tiendas en línea de tipo 1, complementos
- Reproductor de Windows Media en línea, asistente para complementos
- online stores,plug-in wizard
- tiendas en línea de tipo 1, asistente para complementos
- Reproductor de Windows Media en línea, asistente para instalar complementos
- online stores,installing plug-in wizard
- tiendas en línea de tipo 1, asistente para instalación de complementos
- complementos, Reproductor de Windows Media en línea
- complementos, tiendas en línea
- complementos, escriba 1 tienda en línea
- complementos, asistente para instalar complementos
- complementos, asistente para complementos
- Reproductor de Windows Media complementos, escriba 1 tienda en línea
- Reproductor de Windows Media complementos, tiendas en línea
- Reproductor de Windows Media complementos, Reproductor de Windows Media en línea
- Reproductor de Windows Media complementos, asistente para instalar complementos
- Reproductor de Windows Media complementos, asistente para complementos
- Asistente para instalar complementos
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249573"
---
# <a name="installing-the-online-store-plug-in-wizard"></a>Instalación del Asistente para complementos de la tienda en línea

Para configurar el entorno de desarrollo para crear complementos de tienda en línea de tipo 1, debe instalar los siguientes elementos:

-   Microsoft Visual Studio 2005 o posterior
-   Reproductor de Windows Media 11 o posterior
-   Windows SDK, que incluye el SDK Reproductor de Windows Media
-   Asistente para complementos de tienda en línea

## <a name="installing-the-wizard"></a>Instalación del asistente

Siga estos pasos para instalar el Asistente para complementos de la tienda en línea en Visual Studio.

1.  Busque la carpeta donde instaló el SDK Windows. Expanda la carpeta para ver sus subcarpetas y vaya a Ejemplos \\ de servicios de \\ asistentes de WMP \\ \\ multimedia.
2.  Busque los tres archivos siguientes:
    -   wmpservices.vsz
    -   wmpservices.vsdir
    -   wmpservices.ico
3.  Con un editor de texto como Bloc de notas, edite el archivo wmpservices.vsz.

    Busque la línea siguiente:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Cambie `<VsWizardEngine version goes here>` a uno de los siguientes valores, en función de la versión de Visual Studio que haya instalado.

    

    | Value              | Versión de Visual Studio |
    |--------------------|-----------------------|
    | VsWizardEngine.8.0 | Visual Studio 2005    |
    | VsWizardEngine.9.0 | Visual Studio 2008    |

    

     

    Busque la línea siguiente:

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Cambie `<path to wmpservices directory goes here>` a la ruta de acceso donde se encuentran los archivos del asistente.

    Por ejemplo, supongamos que tiene Visual Studio 2008 y los archivos del asistente están aquí: C: Archivos de programa Sdk de Microsoft Windows asistentes multimedia WMP de ejemplos \\ \\ \\ \\ v7.0. \\ \\ \\ \\ \\ A continuación, el archivo wmpservices.vsz tendría el siguiente aspecto:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Busque la carpeta donde instaló Visual Studio. Expanda la carpeta para ver sus subcarpetas y busque una carpeta denominada vcprojects.
5.  Copie los tres archivos enumerados en el paso 2 en la carpeta vcprojects. El asistente ya está instalado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación del complemento para una tienda en línea de tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




