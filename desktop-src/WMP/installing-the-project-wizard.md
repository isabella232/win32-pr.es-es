---
title: Instalar el Asistente para Project aplicación
description: Instalar el Asistente para Project aplicación
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Reproductor de Windows Media en línea, complementos
- tiendas en línea, complementos
- tiendas en línea de tipo 2, complementos
- Reproductor de Windows Media tiendas en línea, asistente para complementos
- tiendas en línea, asistente para complementos
- tiendas en línea de tipo 2, asistente para complementos
- Reproductor de Windows Media tiendas en línea,Asistente para proyectos
- tiendas en línea, asistente para proyectos
- tiendas en línea de tipo 2, asistente para proyectos
- Reproductor de Windows Media tiendas en línea, asistente para instalación de complementos
- tiendas en línea, asistente para instalación de complementos
- tiendas en línea de tipo 2, asistente para instalación de complementos
- Reproductor de Windows Media tiendas en línea, instalar el Asistente para proyectos
- tiendas en línea, asistente para instalar proyectos
- tienda en línea de tipo 2, asistente para instalación de proyectos
- complementos, Reproductor de Windows Media tiendas en línea
- complementos, tiendas en línea
- complementos, escriba 2 tiendas en línea
- complementos, asistente para instalar complementos
- complementos, asistente para complementos
- complementos, asistente para instalar proyectos
- complementos, asistente para proyectos
- Reproductor de Windows Media complementos, escriba 2 tiendas en línea
- Reproductor de Windows Media complementos,tiendas en línea
- Reproductor de Windows Media complementos, Reproductor de Windows Media tiendas en línea
- Reproductor de Windows Media complementos, instalar el Asistente para complementos
- Reproductor de Windows Media complementos, asistente para complementos
- Reproductor de Windows Media complementos, asistente para instalar proyectos
- Reproductor de Windows Media complementos, asistente para proyectos
- Asistente para instalar complementos
- Asistente para complementos
- Asistente para instalar proyectos
- Asistente para proyectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249572"
---
# <a name="installing-the-project-wizard"></a>Instalar el Asistente para Project aplicación

Para configurar el entorno de desarrollo para crear complementos de tienda en línea de tipo 2, debe instalar los siguientes elementos:

-   Microsoft Visual Studio .NET 2003 o posterior
-   Reproductor de Windows Media serie 9 o posterior
-   Windows SDK, que incluye el SDK de Reproductor de Windows Media
-   Asistente para complementos de tienda en línea

## <a name="installing-the-wizard"></a>Instalación del asistente

Siga estos pasos para instalar el Asistente para complementos de tienda en línea en Visual Studio.

1.  Busque la carpeta donde instaló el SDK Windows. Expanda la carpeta para ver sus subcarpetas y vaya a Ejemplos \\ de servicios \\ de asistentes de WMP \\ \\ multimedia.
2.  Busque los tres archivos siguientes:
    -   wmpservices.vsz
    -   wmpservices.vsdir
    -   wmpservices.ico
3.  Con un editor de texto como Bloc de notas, edite el archivo wmpservices.vsz.

    Busque la línea siguiente:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Cambie a uno de los siguientes valores, en función de la versión de `<VsWizardEngine version goes here>` Visual Studio que haya instalado.

    

    | Value              | Versión de Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine.7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine.8.0 | Visual Studio 2005      |
    | VsWizardEngine.9.0 | Visual Studio 2008      |

    

     

    Busque la línea siguiente:

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Cambie `<path to wmpservices directory goes here>` a la ruta de acceso donde se encuentran los archivos del asistente.

    Por ejemplo, supongamos que tiene Visual Studio 2008 y los archivos del asistente están aquí: C: Archivos de programa SDK de Microsoft Windows asistentes de WMP multimedia de ejemplos \\ \\ \\ \\ v7.0. \\ \\ \\ \\ \\ A continuación, el archivo wmpservices.vsz tendría este aspecto:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Busque la carpeta en la que instaló Visual Studio. Expanda la carpeta para ver sus subcarpetas y busque una carpeta denominada vcprojects.
5.  Copie los tres archivos enumerados en el paso 2 en la carpeta vcprojects. El asistente ya está instalado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación del complemento para una tienda en línea de tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




