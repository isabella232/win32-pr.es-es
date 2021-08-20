---
title: Uso del Asistente para complementos de tienda en línea con Visual Studio
description: Uso del Asistente para complementos de tienda en línea con Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Reproductor de Windows Media en línea, complementos
- tiendas en línea, complementos
- tiendas en línea de tipo 1, complementos
- Reproductor de Windows Media tiendas en línea, asistente para complementos
- tiendas en línea, asistente para complementos
- tiendas en línea de tipo 1, asistente para complementos
- Reproductor de Windows Media en línea, Visual Studio
- tiendas en línea, Visual Studio
- tiendas en línea de tipo 1, Visual Studio
- complementos, Reproductor de Windows Media en línea
- complementos, tiendas en línea
- complementos, escriba 1 tienda en línea
- complementos, Visual Studio
- complementos, asistente para complementos
- Reproductor de Windows Media complementos, escriba 1 tienda en línea
- Reproductor de Windows Media complementos,tiendas en línea
- Reproductor de Windows Media complementos, Reproductor de Windows Media tiendas en línea
- Reproductor de Windows Media complementos, Visual Studio
- Reproductor de Windows Media complementos, asistente para complementos
- Visual Studio,Reproductor de Windows Media De tiendas en línea
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd53a1b83f817e4cfcc7dede80361f56f46ea41da8730f4396330c12af05c73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830686"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Uso del Asistente para complementos de tienda en línea con Visual Studio

Después de instalar los componentes necesarios, puede crear rápidamente un complemento que sirva como punto de partida. Los pasos siguientes le guiarán:

1.  Inicie Microsoft Visual Studio.
2.  En el **menú Archivo** , seleccione **Nuevo y,** a continuación, **haga clic Project**.
3.  En **Project ,** haga clic en Visual C++ **Projects**.
4.  En Plantillas , haga clic Reproductor de Windows Media **Asistente para tiendas en línea**.
5.  Escriba un nombre para el proyecto.
6.  Escriba una ubicación para el proyecto. Esta es la carpeta en la que se copiarán los archivos del proyecto.
7.  Haga **clic en** Aceptar para iniciar el asistente.
8.  Seleccione **Tipo 1 (integración profunda)** y haga clic **en Siguiente.**
9.  Escriba un nombre descriptivo y un distribuidor de contenido. Haga clic en **Finalizar**
10. Use el Visual Studio de desarrollo para compilar el proyecto.
    > [!Note]  
    > En Windows Vista y versiones posteriores, el proyecto no se compilará correctamente a menos que ejecute Visual Studio con un token de acceso de administrador completo. Haga clic con el botón derecho en el Visual Studio o icono y haga clic **en Ejecutar como administrador.**

     

Antes de intentar compilar el proyecto, asegúrese de configurar el entorno de desarrollo para que apunte a las carpetas denominadas Include y Lib donde instaló el SDK de Windows. El compilador y el vinculador necesitarán acceso a algunos de los archivos de estas carpetas.

Si ejecutó la utilidad Visual Studio Registration que se incluye con el SDK de Windows, es probable que el entorno de desarrollo ya se haya configurado para que apunte a las carpetas Include y Lib del SDK de Windows. De lo contrario, debe configurar manualmente el entorno de desarrollo.

Para configurar manualmente Visual Studio, siga estos pasos.

1.  En el **menú Herramientas,** haga clic en Opciones.
2.  Haga **clic en Proyectos y soluciones** y, a continuación, haga clic VC++ **directorios**.
3.  En **Mostrar directorios para**, haga clic en Incluir archivos **o** Archivos **de biblioteca.**
4.  Agregue los directorios de los archivos necesarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación del complemento para una tienda en línea de tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




