---
title: Usar el Asistente para complementos con Visual Studio
description: Usar el Asistente para complementos con Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Complementos de Windows Media Player, Visual Studio
- complementos, Visual Studio
- crear complementos, Visual Studio
- Asistente para complementos de Windows Media Player, Visual Studio
- Asistente para complementos de Windows Media Player de Visual Studio
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357281"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Usar el Asistente para complementos con Visual Studio

Una vez instalados los componentes necesarios, puede crear rápidamente un complemento que sirva como punto de partida. Los siguientes pasos lo guiarán.

1.  Inicie Microsoft Visual Studio.
2.  En el menú **archivo** , seleccione **nuevo** y haga clic en **proyecto**.
3.  En **tipos de proyecto**, seleccione **proyectos de Visual C++**.
4.  En **plantillas**, seleccione **Asistente para complementos de Media Player de Windows**.
5.  Escriba un nombre para el proyecto.
6.  Escriba una ubicación para el proyecto. Esta es la carpeta en la que se copiarán los archivos del proyecto.
7.  Haga clic en **Aceptar** para iniciar el asistente.
8.  Seleccione el tipo de complemento que desea crear.
9.  Complete los demás cuadros de diálogo del asistente.
10. Use el entorno de desarrollo de Visual Studio para compilar el proyecto.
    > [!Note]  
    > En Windows Vista y versiones posteriores, el proyecto no se compilará correctamente a menos que ejecute Visual Studio con un token de acceso de administrador completo. Haga clic con el botón derecho en el nombre o el icono de Visual Studio y haga clic en **Ejecutar como administrador**.

     

Antes de intentar compilar el proyecto, asegúrese de configurar el entorno de desarrollo para que apunte a las carpetas denominadas include y lib en las que instaló el Windows SDK. El compilador y el vinculador deberán tener acceso a algunos de los archivos de estas carpetas.

Si ejecutó la utilidad de registro de Visual Studio que se incluye con el Windows SDK, es probable que el entorno de desarrollo ya se haya configurado para que apunte a las carpetas include y lib de Windows SDK. De lo contrario, debe configurar manualmente el entorno de desarrollo.

Para configurar manualmente Visual Studio, siga estos pasos.

1.  En el menú **Herramientas** , haga clic en **Opciones**.
2.  Haga clic en **proyectos y soluciones** y, a continuación, haga clic en **directorios de VC + +**.
3.  En **Mostrar directorios para**, haga clic en **incluir** archivos o **archivos de biblioteca**.
4.  Agregue los directorios de los archivos necesarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar un complemento](building-a-plug-in.md)
</dt> </dl>

 

 




