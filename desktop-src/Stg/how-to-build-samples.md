---
title: Cómo compilar ejemplos
description: Para compilar un ejemplo COM, el entorno del equipo debe estar configurado para compilar aplicaciones de Microsoft Win32 C++.
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- Cómo compilar ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593d3465d3ebcc32a6768dd8b2dffe1f0a653d07
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "105665777"
---
# <a name="how-to-build-samples"></a>Cómo compilar ejemplos

Para compilar un ejemplo COM, el entorno del equipo debe estar configurado para compilar aplicaciones de Microsoft Win32 C++.

## <a name="preparing-a-computer-to-create-com-samples"></a>Preparar un equipo para crear ejemplos de COM

El entorno del equipo debe configurarse con un compilador de C++ de 32 bits, un vinculador y un compilador de recursos que sean compatibles con Microsoft Visual C++ 4. x o posterior y un Windows SDK instalado correctamente. Es mejor instalar el Windows SDK en último lugar. El Windows SDK proporciona los archivos de biblioteca. h include y. lib necesarios para la funcionalidad de COM codificada en los ejemplos.

Para ejecutar correctamente los ejemplos Remclien, Freserve y Freclien, es necesario disponer de instalaciones del sistema que estén disponibles en los sistemas operativos Windows: Windows Server 2003, Windows XP, Windows 2000 o Windows NT 4,0. Los ejemplos de Remclien, Freserve y Freclien se compilarán, pero no se ejecutarán en los sistemas operativos Windows me, Windows 98 o Windows 95, a menos que COM distribuido (DCOM) y COM de subprocesamiento libre formen parte del sistema operativo. Esta compatibilidad está disponible para los sistemas operativos Windows me, Windows 98 y Windows 95 en el complemento DCOM95. Actualmente, se puede obtener DCOM95 mediante la [descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=31661).

Cada directorio de ejemplo tiene los archivos de código fuente necesarios para compilar y ejecutar el ejemplo. El directorio de ejemplo principal tiene un archivo de Makeall.bat, que puede ejecutar desde el símbolo del sistema para realizar todos los ejemplos de código de la rama siguiente. Para obtener más información, vea el archivo de Makeall.bat. Si su entorno está configurado para compilar aplicaciones Win32 de C++, simplemente puede ejecutar Makeall.bat desde el directorio en el que reside para compilar todos los ejemplos de código de la rama siguiente. Makeall garantiza el orden correcto de la compilación para que se satisfagan todas las dependencias de ejemplo de código.

El directorio principal también tiene un archivo make que compila todos los ejemplos de código del tutorial usando opciones similares a las admitidas por Makeall.bat. Para obtener más información, vea este archivo make. Este archivo make supone que la rama completa de ejemplos de código se instala como parte de la Windows SDK. Actualmente, esta ubicación tiene una ruta de acceso similar a *d: \\ MSSDK \\ Samples \\ com \\ TUTSAMP*, donde D: representa la unidad de instalación. Si ha extraído la rama de ejemplo de código del tutorial (por ejemplo, el directorio COM COM y sus subdirectorios) en otra ubicación fuera del Windows SDK (o si obtuvo el conjunto de ejemplo como una descarga independiente del sitio web de Microsoft), use Makeall.bat para compilar todos los ejemplos de la rama. En general, se recomienda Makeall.bat. También se proporciona un archivo de Logmall.bat. Hace lo mismo que el archivo por lotes de Makeall, con la diferencia de que registra todos los resultados de compilación en Errorlog.txt de archivo en el directorio principal del tutorial.

También se proporcionan dos archivos por lotes, Regall.bat y Unregall.bat, en el directorio principal para registrar y anular el registro de todos los servidores COM en la serie de ejemplos de código del tutorial. Para registrar todos los servidores, ejecute Regall.bat archivo desde el directorio principal. Para anular el registro de todos los servidores, ejecute Unregall.bat de la misma manera. Estos archivos por lotes requieren una compilación anterior de los ejemplos de código registro, SERIALización, DLLSERVE, LICSERVE, LOCSERVE, APTSERVE, FRESERVE y conservar. Si realiza una compilación normal de los ejemplos de código, los archivos make del servidor registrarán automáticamente los servidores. En este caso, no es necesario ejecutar el archivo por lotes Regall.

Ejecute el archivo por lotes Cleanall.bat para realizar un cleanAll exhaustivo de todos los ejemplos de tutoriales de COM.

> [!WARNING]
> Este archivo por lotes elimina todos los archivos de proyecto de Visual Studio y otros archivos de trabajo temporales creados por Visual C++ en los ejemplos. Todos los servidores COM compilados en los ejemplos de código del tutorial no se registran en el registro. Se eliminan todos los archivos ejecutables exe y. dll. Se eliminan todos los archivos de símbolos de depuración. También se eliminan los archivos generados en una variedad de entornos de compilación.

 

Ejecute "Makeall Clean" para realizar una limpieza más rápida, pero más modesta, de todos los ejemplos de código. Esta operación de limpieza no intenta ser tan completa como la que realiza Cleanall.bat. Se eliminan los archivos. obj, pero se conservan los binarios de salida. No se anula el registro de los servidores COM del registro.

Esta serie de ejemplo se originó como parte integral del Windows SDK, por lo que el tutorial narrativa presupone un entorno con el Windows SDK instalado correctamente.

Sin embargo, las versiones de Microsoft Visual C++ versión 4,0 y posteriores también pueden proporcionar los archivos de biblioteca. h include y. lib necesarios para la compilación. En tales casos, puede que no sea necesario instalar el Windows SDK para compilar los ejemplos.

Para obtener más información y completar los detalles de la compilación de ejemplo, vea:

[Configuración del entorno](environment-setup.md)

[Archivos make](makefiles.md)

[Uso de Visual Studio](using-visual-studio.md)

[Extraer los ejemplos de código](extracting-the-code-samples.md)

[Convenciones de estilo de codificación](coding-style-conventions.md)

 

 




