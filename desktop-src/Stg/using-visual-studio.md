---
title: Uso de Visual Studio
description: Para mayor comodidad, Microsoft Visual Studio 6.0 proporciona un archivo de proyecto para cada ejemplo.
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee6edc1b19cb0e56495c8af6f96d28e4d255e40d53161671f52a1a7d27939f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796855"
---
# <a name="using-visual-studio"></a>Uso de Visual Studio

Para mayor comodidad, Microsoft Visual Studio 6.0 proporciona un archivo de proyecto para cada ejemplo. Este archivo tiene la extensión DSP. También se proporciona un archivo de área de trabajo Allsamp.dsw en el directorio principal para que pueda compilar todos los ejemplos a la vez desde dentro Visual Studio.

> [!Note]  
> Las instrucciones siguientes se escriben para Microsoft Visual Studio 6.0. Los comandos pueden diferir en versiones anteriores y posteriores de Visual Studio.

 

Para cargar el proyecto adecuado para un ejemplo, puede ejecutar Visual Studio en el símbolo del sistema en el directorio del ejemplo, como se muestra en el ejemplo siguiente. Debe sustituir el nombre del proyecto de ejemplo por **<project name>** .

**msdev <project name> .dsp**

También puede hacer doble clic en el archivo .dsp en Windows Explorer para cargar el área de trabajo de un ejemplo en Visual Studio. Desde dentro Visual Studio puede examinar las clases de C++ del origen de ejemplo y, por lo general, realizar las otras operaciones de edición,compilación y depuración.

Como parte del Kit de desarrollo de software de plataforma (SDK), la compilación de estos ejemplos desde dentro de Visual Studio requiere la configuración adecuada de las rutas de acceso de directorio en Visual Studio. Para establecer las rutas de acceso del directorio, realice los pasos siguientes:

-   Ejecute Microsoft Visual Studio (Visual C++).
-   Elija **Opciones...** en el **menú** Herramientas.
-   Elija la **pestaña Directorios** en el **cuadro de diálogo** Opciones.
-   En la lista desplegable **Mostrar** directorios  para, seleccione Archivos ejecutables y escriba la ruta de acceso del directorio BIN para el SDK de plataforma instalado (por ejemplo, C: Archivos de programa Microsoft \\ SDK \\ \\ Bin). Haga clic en el botón de flecha arriba para mover esta ruta de acceso recién especificada para que sea la primera entrada de la **lista Directorios.**
-   En la lista desplegable **Mostrar** directorios para, seleccione Incluir archivos y escriba la ruta de acceso del directorio INCLUDE para el SDK de plataforma instalado (por ejemplo, C: Archivos de programa que incluye el SDK de  \\ \\ \\ Microsoft). Haga clic en el botón de flecha arriba para mover esta ruta de acceso recién especificada para que sea la primera entrada de la **lista Directorios.**
-   En la lista desplegable **Mostrar** directorios para, seleccione Archivos de biblioteca y escriba la ruta de acceso del directorio LIB para el SDK de plataforma instalado (por ejemplo, C: Archivos de programa Biblioteca del SDK de  \\ \\ \\ Microsoft). Haga clic en los botones de flecha arriba para mover esta ruta de acceso recién especificada para que sea la primera entrada de la **lista Directorios.**
-   Haga clic en el botón Aceptar del **cuadro de diálogo** Opciones para completar la configuración.

Desde allí puede usar el editor, el depurador y las instalaciones del proyecto para editar, compilar, vincular y depurar.

Otros IDE visuales también pueden generar fácilmente uno de sus archivos Make del proyecto nativo, dados los archivos de código fuente existentes de un ejemplo de código. Si usa este IDE, la generación de este tipo de archivo make del proyecto nativo puede merecer la pena, ya que ofrece una manera de examinar las clases de C++ del programa. Para obtener más información sobre el uso de archivos Make externos o la creación de un archivo Make de proyecto nativo mediante un conjunto de archivos de origen existentes, consulte la documentación del IDE.

Aparte de la dependencia del código común en los directorios APPUTIL, INC y LIB relacionados, muchos ejemplos de código son independientes. Compile APPUTIL antes de compilar otros ejemplos de código. Algunos ejemplos más adelante en la secuencia pueden funcionar con los resultados compilados de ejemplos anteriores. Estas interdependencias de ejemplo de código son las siguientes:

-   Cualquiera: la compilación de cualquier ejemplo de código necesita una compilación anterior de APPUTIL.
-   DLLUSER: la compilación o ejecución necesita la compilación anterior de DLLSUSER.
-   COMUSER: la compilación o ejecución necesita una compilación anterior de COMOBJ.
-   DLLSERVE: la compilación necesita la compilación anterior de REGISTER.
-   DLLCLIEN: la ejecución necesita una compilación anterior de DLLSERVE.
-   LICSERVE: La compilación necesita una compilación anterior de REGISTER.
-   LICCLIEN: la ejecución necesita una compilación anterior de LICSERVE y DLLSERVE.
-   MARSHAL: la compilación necesita la compilación anterior de REGISTER.
-   LOCSERVE: la compilación o ejecución necesita una compilación anterior de REGISTER y MARSHAL.
-   LOCCLIEN: la ejecución necesita una compilación anterior de LOCSERVE.
-   APTSERVE: la compilación o ejecución necesita una compilación anterior de REGISTER y MARSHAL.
-   APTCLIEN: la ejecución necesita una compilación anterior de APTSERVE.
-   REMCLIEN: la compilación o ejecución necesita una compilación anterior de REGISTER y MARSHAL en el equipo local (cliente). La ejecución necesita la compilación anterior de REGISTER, MARSHAL y APTSERVE en el equipo remoto (servidor).
-   FRESERVE: la compilación necesita la compilación anterior de REGISTER.
-   FRECLIEN: la ejecución necesita una compilación anterior de FRESERVE.
-   CONSERVE: la compilación necesita la compilación anterior de REGISTER.
-   CONCLIEN: la ejecución necesita una compilación anterior de CONSERVE.
-   STOSERVE: la compilación necesita una compilación anterior de REGISTER.
-   STOCLIEN: la ejecución necesita una compilación anterior de STOSERVE.
-   PERSERVE: la compilación necesita la compilación anterior de REGISTER.
-   PERTEXT: la compilación necesita la compilación anterior de REGISTER.
-   PERDRAW: la compilación necesita la compilación anterior de REGISTER.
-   PERCLIEN: la ejecución necesita una compilación anterior de PERSERVE, PERTEXT y PERDRAW.
-   DCDMARSH: la compilación necesita la compilación anterior de REGISTER.
-   DCDSERVE: la compilación o ejecución necesita la compilación anterior de REGISTER y DCDMARSH.
-   DCOMDRAW: la compilación o ejecución necesita una compilación anterior de REGISTER y DCDMARSH en el equipo local (cliente). La ejecución necesita la compilación anterior de REGISTER, DCDMARSH y DCOMDRAW en el equipo remoto (servidor).

 

 




