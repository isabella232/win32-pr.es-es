---
title: Uso de Visual Studio
description: Para mayor comodidad, Microsoft Visual Studio 6,0 proporciona un archivo de proyecto para cada ejemplo.
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b32359a29d14a6cd5a4d08d015a6598ade376d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772829"
---
# <a name="using-visual-studio"></a>Uso de Visual Studio

Para mayor comodidad, Microsoft Visual Studio 6,0 proporciona un archivo de proyecto para cada ejemplo. Este archivo tiene la extensión DSP. También se proporciona un archivo de área de trabajo de Allsamp. DSW en el directorio principal para que pueda compilar todos los ejemplos a la vez desde Visual Studio.

> [!Note]  
> Las instrucciones siguientes están escritas para Microsoft Visual Studio 6,0. Los comandos pueden diferir en versiones anteriores y posteriores de Visual Studio.

 

Para cargar el proyecto adecuado para un ejemplo, puede ejecutar Visual Studio en el símbolo del sistema en el directorio del ejemplo, tal y como se muestra en el ejemplo siguiente. Debe sustituir el nombre del proyecto de ejemplo por **<project name>** .

**MSDev <project name> . DSP**

También puede hacer doble clic en el archivo. DSP en el explorador de Windows para cargar el área de trabajo de un ejemplo en Visual Studio. Desde dentro de Visual Studio, puede examinar las clases de C++ del origen de ejemplo y, por lo general, realizar las demás operaciones de edición-compilación-depuración.

Como parte del kit de desarrollo de software (SDK) de la plataforma, la compilación de estos ejemplos desde dentro de Visual Studio requiere la configuración adecuada de las rutas de acceso de directorio en Visual Studio. Para establecer las rutas de acceso de directorio, realice los pasos siguientes:

-   Ejecute Microsoft Visual Studio (Visual C++).
-   Elija **Opciones...** en el menú **herramientas** .
-   Elija la pestaña **directorios** en el cuadro de diálogo **Opciones** .
-   En la lista desplegable **Mostrar directorios para** , seleccione **archivos ejecutables** y escriba la ruta de acceso del directorio bin para el SDK de plataforma instalado (por ejemplo, C: \\ archivos de programa \\ Microsoft SDK \\ bin). Haga clic en el botón de flecha arriba para moverlo a la primera entrada de la lista **directorios** .
-   En la lista desplegable **Mostrar directorios para** , seleccione **incluir archivos** y escriba la ruta de acceso del directorio de inclusión para el SDK de la plataforma instalada (por ejemplo, C: \\ archivos de programa \\ Microsoft SDK \\ include). Haga clic en el botón de flecha arriba para moverlo a la primera entrada de la lista **directorios** .
-   En la lista desplegable **Mostrar directorios para** , seleccione **archivos de biblioteca** y escriba la ruta de acceso del directorio lib para el SDK de plataforma instalado (por ejemplo, C: \\ archivos de programa \\ Microsoft SDK \\ lib). Haga clic en los botones de flecha arriba para moverlo a la primera entrada de la lista **directorios** .
-   Haga clic en el botón Aceptar del cuadro de diálogo **Opciones** para completar la configuración.

Desde allí, puede usar el editor, el depurador y las herramientas de proyecto para editar, compilar, vincular y depurar.

Otros IDE visuales también pueden generar fácilmente uno de sus archivos make de proyecto nativos, dados los archivos de código fuente existentes de un ejemplo de código. Si usa este tipo de IDE, la generación de un archivo make de proyecto nativo puede ser muy rentable, ya que ofrece una manera de examinar las clases de C++ del programa. Para obtener más información sobre el uso de archivos make externos o la creación de un archivo make de proyecto nativo mediante un conjunto de archivos de código fuente existentes, consulte la documentación del IDE.

Aparte de la dependencia del código común en los directorios del mismo nivel APPUTIL, INC y LIB, muchos ejemplos de código son independientes. Cree APPUTIL antes de compilar otros ejemplos de código. Algunos ejemplos posteriores de la secuencia pueden funcionar con los resultados compilados de los ejemplos anteriores. Estas interdependencias de ejemplo de código son las siguientes:

-   Any: la compilación de cualquier ejemplo de código necesita la compilación anterior de APPUTIL.
-   DLLUSER: la compilación o ejecución necesita una compilación anterior de DLLSKEL.
-   Comusuario: compilar o ejecutar necesita una compilación anterior de COMOBJ.
-   DLLSERVE: la compilación necesita la compilación anterior del registro.
-   DLLCLIEN: la ejecución requiere la compilación anterior de DLLSERVE.
-   LICSERVE: la compilación necesita la compilación anterior del registro.
-   LICCLIEN: Run requiere la compilación anterior de LICSERVE y DLLSERVE.
-   SERIALización: la compilación necesita una compilación anterior del registro.
-   LOCSERVE: la compilación o ejecución necesita una compilación anterior de registro y SERIALización.
-   LOCCLIEN: la ejecución requiere la compilación anterior de LOCSERVE.
-   APTSERVE: la compilación o ejecución necesita una compilación anterior de registro y SERIALización.
-   APTCLIEN: la ejecución requiere la compilación anterior de APTSERVE.
-   REMCLIEN: la compilación o ejecución requiere la compilación anterior del registro y la SERIALización en el equipo local (cliente). La ejecución requiere la compilación anterior de registro, SERIALización y APTSERVE en el equipo remoto (servidor).
-   FRESERVE: la compilación necesita la compilación anterior del registro.
-   FRECLIEN: la ejecución requiere la compilación anterior de FRESERVE.
-   CONSERVAR: la compilación necesita la compilación anterior del registro.
-   CONCLIEN: la ejecución requiere la compilación anterior de la conservación.
-   STOSERVE: la compilación necesita la compilación anterior del registro.
-   STOCLIEN: la ejecución requiere la compilación anterior de STOSERVE.
-   Peratienda: la compilación necesita la compilación anterior del registro.
-   PERTEXT: la compilación necesita la compilación anterior del registro.
-   Perdraw: la compilación necesita la compilación anterior del registro.
-   PERCLIEN: la ejecución requiere la compilación anterior de peratienda, PERTEXT y perdraw.
-   DCDMARSH: la compilación necesita la compilación anterior del registro.
-   DCDSERVE: la compilación o ejecución necesita una compilación anterior de REGISTER y DCDMARSH.
-   DCOMDRAW: la compilación o ejecución necesita una compilación anterior del registro y el DCDMARSH en el equipo local (cliente). La ejecución requiere la compilación anterior de REGISTER, DCDMARSH y DCOMDRAW en el equipo remoto (servidor).

 

 




