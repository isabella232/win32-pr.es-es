---
title: Cómo compilar ejemplos
description: Para compilar un ejemplo COM, el entorno del equipo debe configurarse para compilar aplicaciones de Microsoft Win32 C++.
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- Cómo compilar ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782a75bb54127191757a515244d439bbff9570c96f4e0bb2ac603477bedb96a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663125"
---
# <a name="how-to-build-samples"></a>Cómo compilar ejemplos

Para compilar un ejemplo COM, el entorno del equipo debe configurarse para compilar aplicaciones de Microsoft Win32 C++.

## <a name="preparing-a-computer-to-create-com-samples"></a>Preparar un equipo para crear ejemplos COM

El entorno del equipo debe configurarse con un compilador, un vinculador y un compilador de recursos de C++ de 32 bits instalados correctamente que sean compatibles con Microsoft Visual C++ 4.x o posterior, y un SDK de Windows instalado correctamente. Es mejor instalar el sdk de Windows en último lugar. El SDK Windows proporciona archivos de biblioteca .h include y .lib necesarios para la funcionalidad COM codificada en los ejemplos.

Para ejecutar correctamente los ejemplos de Remclien, Freserve y Freclien se necesitan instalaciones del sistema que estén disponibles en los sistemas operativos Windows: Windows Server 2003, Windows XP, Windows 2000 o Windows NT 4.0. Los ejemplos de Remclien, Freserve y Freclien se compilarán, pero no se ejecutarán en los sistemas operativos Windows Me, Windows 98 o Windows 95, a menos que COM distribuido (DCOM) y COM de subproceso libre formen parte del sistema operativo. Esta compatibilidad está disponible para los sistemas operativos Windows Me, Windows 98 y Windows 95 en el complemento DCOM95. DCOM95 se puede obtener actualmente mediante la [descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=31661).

Cada directorio de ejemplo tiene los archivos de origen necesarios para compilar y ejecutar el ejemplo. El directorio de ejemplo primario tiene un Makeall.bat, que puede ejecutar desde el símbolo del sistema para crear todos los ejemplos de código de la rama siguiente. Para obtener más información, vea el Makeall.bat archivo. Si el entorno está configurado para compilar aplicaciones win32 de C++, simplemente puede ejecutar Makeall.bat desde el directorio donde reside para compilar todos los ejemplos de código de la rama siguiente. Makeall garantiza el orden correcto de la compilación para que se cumplen todas las dependencias de ejemplo de código.

El directorio principal también tiene un archivo Make que compila todos los ejemplos de código del tutorial mediante opciones similares a las admitidas por Makeall.bat. Para obtener más información, vea este archivo Make. En este archivo Make se da por supuesto que toda la rama de ejemplos de código está instalada como parte del SDK Windows. Actualmente, esta ubicación tiene una ruta de acceso similar a *D: \\ MSSDK \\ SAMPLES COM \\ \\ TUTSAMP*, donde D: representa la unidad de instalación. Si ha extraído la rama de ejemplo de código del tutorial (por ejemplo, el directorio COM y sus subdirectorios com) en otra ubicación fuera del SDK de Windows (o si obtuvo el conjunto de ejemplo como una descarga independiente del sitio web de Microsoft), use Makeall.bat para compilar todos los ejemplos de la rama. En general, Makeall.bat se recomienda. También Logmall.bat archivo de configuración. Hace lo mismo que makeall archivo por lotes, excepto que registra todos los resultados de compilación en el archivo Errorlog.txt en el directorio principal del tutorial.

También se proporcionan dos archivos por lotes, Regall.bat y Unregall.bat, en el directorio principal para registrar y anular el registro de todos los servidores COM en la serie de ejemplos de código del tutorial. Para registrar todos los servidores, ejecute Regall.bat archivo desde el directorio principal. Para anular el registro de todos los servidores, ejecute Unregall.bat de la misma manera. Estos archivos por lotes requieren una compilación anterior de los ejemplos de código REGISTER, MARSHAL, DLLSERVE, LICSERVE, LOCSERVE, APTSERVE, FRESERVE y CONSERVE. Si realiza una compilación normal de los ejemplos de código, los archivos make del servidor registrarán automáticamente los servidores. En este caso, no es necesario ejecutar el archivo por lotes Regall.

Ejecute el Cleanall.bat por lotes para realizar una limpieza exhaustiva de todos los ejemplos del tutorial com.

> [!WARNING]
> Este archivo por lotes elimina todos Visual Studio archivos de proyecto y otros archivos de trabajo temporales creados por Visual C++ en los ejemplos. Todos los servidores COM integrados en los ejemplos de código del tutorial se anulan del registro. Se eliminan todos los archivos .dll ejecutables. Se eliminan todos los archivos de símbolos de depuración. También se eliminan los archivos generados en diversos entornos de compilación.

 

Ejecute "Makeall Clean" para realizar una limpieza más rápida, pero más discreta, de todos los ejemplos de código. Esta operación de limpieza no intenta ser tan completa como la realizada por Cleanall.bat. Los archivos .obj se eliminan, pero se conservan los archivos binarios de salida. Los servidores COM no se anulan del registro del Registro.

Esta serie de ejemplo se originó como parte integral del SDK de Windows, por lo que la narrativa del tutorial supone un entorno con el SDK de Windows instalado correctamente.

Sin embargo, las versiones Microsoft Visual C++ versión 4.0 y posteriores también pueden proporcionar los archivos de biblioteca .h include y .lib necesarios para la compilación. En tales casos, es posible que no sea necesario instalar Windows SDK para compilar los ejemplos.

Para obtener más información y completar los detalles de compilación de ejemplo, consulte:

[Configuración del entorno](environment-setup.md)

[Makefiles](makefiles.md)

[Uso de Visual Studio](using-visual-studio.md)

[Extracción de los ejemplos de código](extracting-the-code-samples.md)

[Convenciones de estilo de codificación](coding-style-conventions.md)

 

 




