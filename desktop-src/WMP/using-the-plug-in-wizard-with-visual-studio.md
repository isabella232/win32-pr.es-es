---
title: Uso del Asistente para complementos con Visual Studio
description: Uso del Asistente para complementos con Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Reproductor de Windows Media complementos, Visual Studio
- complementos, Visual Studio
- compilar complementos, Visual Studio
- Reproductor de Windows Media Asistente para complementos, Visual Studio
- Visual Studio,Reproductor de Windows Media asistente para complementos
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534d084d2c57d3546427db59274d1bd135bc66e8bf396906ff7776cae9a370f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134338"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Uso del Asistente para complementos con Visual Studio

Después de instalar los componentes necesarios, puede crear rápidamente un complemento que sirva como punto de partida. Los pasos siguientes le guiarán.

1.  Inicie Microsoft Visual Studio.
2.  En el **menú Archivo** , seleccione **Nuevo y,** a continuación, haga clic **Project**.
3.  En **Project ,** seleccione **Visual C++ Projects**.
4.  En **Plantillas,** seleccione **Reproductor de Windows Media asistente para complementos**.
5.  Escriba un nombre para el proyecto.
6.  Escriba una ubicación para el proyecto. Esta es la carpeta en la que se copiarán los archivos del proyecto.
7.  Haga **clic en** Aceptar para iniciar el asistente.
8.  Seleccione el tipo de complemento que desea crear.
9.  Complete los cuadros de diálogo restantes del asistente.
10. Use el Visual Studio de desarrollo para compilar el proyecto.
    > [!Note]  
    > En Windows Vista y versiones posteriores, el proyecto no se compilará correctamente a menos que ejecute Visual Studio con un token de acceso de administrador completo. Haga clic con el botón derecho en Visual Studio o icono y haga clic **en Ejecutar como administrador.**

     

Antes de intentar compilar el proyecto, asegúrese de configurar el entorno de desarrollo para que apunte a las carpetas denominadas Include y Lib donde instaló Windows SDK. El compilador y el vinculador necesitarán acceso a algunos de los archivos de estas carpetas.

Si ejecutó la utilidad Visual Studio Registration que viene con el SDK de Windows, es probable que el entorno de desarrollo ya se haya configurado para que apunte a las carpetas include y Lib del SDK de Windows. De lo contrario, debe configurar manualmente el entorno de desarrollo.

Para configurar manualmente Visual Studio, siga estos pasos.

1.  En el menú **Herramientas** , haga clic en **Opciones**.
2.  Haga **clic en Proyectos y soluciones** y, a continuación, haga clic VC++ **directorios**.
3.  En **Mostrar directorios para**, haga clic en Incluir archivos **o** Archivos **de biblioteca.**
4.  Agregue los directorios de los archivos necesarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un complemento](building-a-plug-in.md)
</dt> </dl>

 

 




