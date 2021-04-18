---
title: Usar el Asistente para complementos de la tienda en línea con Visual Studio
description: Usar el Asistente para complementos de la tienda en línea con Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player tiendas en línea, Complementos
- tiendas en línea, Complementos
- tipo 1 tiendas en línea, Complementos
- Windows Media Player tiendas en línea, Asistente para complementos
- tiendas en línea, Asistente para complementos
- tipo 1 tiendas en línea, Asistente para complementos
- Windows Media Player tiendas en línea, Visual Studio
- tiendas en línea, Visual Studio
- tipo 1 tiendas en línea, Visual Studio
- complementos, Windows Media Player tiendas en línea
- complementos, tiendas en línea
- complementos, escriba 1 tiendas en línea
- complementos, Visual Studio
- complementos, Asistente para complementos
- Complementos de Windows Media Player, escriba 1 tiendas en línea
- Complementos de Windows Media Player, tiendas en línea
- Complementos de Windows Media Player, Windows Media Player tiendas en línea
- Complementos de Windows Media Player, Visual Studio
- Complementos de Windows Media Player, Asistente para complementos
- Asistente para tiendas en línea de Visual Studio, Windows Media Player
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704575"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Usar el Asistente para complementos de la tienda en línea con Visual Studio

Una vez instalados los componentes necesarios, puede crear rápidamente un complemento que sirva como punto de partida. Los pasos siguientes le guiarán:

1.  Inicie Microsoft Visual Studio.
2.  En el menú **archivo** , seleccione **nuevo** y haga clic en **proyecto**.
3.  En **tipos de proyecto**, haga clic en **proyectos de Visual C++**.
4.  En **plantillas**, haga clic en el **asistente de Windows Media Player tiendas en línea**.
5.  Escriba un nombre para el proyecto.
6.  Escriba una ubicación para el proyecto. Esta es la carpeta en la que se copiarán los archivos del proyecto.
7.  Haga clic en **Aceptar** para iniciar el asistente.
8.  Seleccione **tipo 1 (integración profunda)** y haga clic en **siguiente**.
9.  Escriba un nombre descriptivo y un distribuidor de contenido. Haga clic en **Finalizar**
10. Use el entorno de desarrollo de Visual Studio para compilar el proyecto.
    > [!Note]  
    > En Windows Vista y versiones posteriores, el proyecto no se compilará correctamente a menos que ejecute Visual Studio con un token de acceso de administrador completo. Haga clic con el botón derecho en el nombre o el icono de Visual Studio y haga clic en **Ejecutar como administrador**.

     

Antes de intentar compilar el proyecto, asegúrese de configurar el entorno de desarrollo para que apunte a las carpetas denominadas include y lib en las que instaló el Windows SDK. El compilador y el vinculador deberán tener acceso a algunos de los archivos de estas carpetas.

Si ejecutó la utilidad de registro de Visual Studio que se incluye con el Windows SDK, es probable que el entorno de desarrollo ya se haya configurado para que apunte a las carpetas include y lib de Windows SDK. De lo contrario, debe configurar manualmente el entorno de desarrollo.

Para configurar manualmente Visual Studio, siga estos pasos.

1.  En el menú **herramientas** , haga clic en opciones.
2.  Haga clic en **proyectos y soluciones** y, a continuación, haga clic en **directorios de VC + +**.
3.  En **Mostrar directorios para**, haga clic en **incluir** archivos o **archivos de biblioteca**.
4.  Agregue los directorios de los archivos necesarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar el complemento para una tienda en línea de tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




