---
title: Configuración del entorno
description: El kit de desarrollo de software (SDK) de la plataforma instalada proporciona un archivo Setenv.bat ubicado en el directorio raíz del SDK de la plataforma que se puede ejecutar para configurar el entorno para la creación de aplicaciones que usan el SDK de la plataforma.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665631"
---
# <a name="environment-setup"></a>Configuración del entorno

El kit de desarrollo de software (SDK) de la plataforma instalada proporciona un archivo Setenv.bat ubicado en el directorio raíz del SDK de la plataforma que se puede ejecutar para configurar el entorno para la creación de aplicaciones que usan el SDK de la plataforma.

## <a name="settings-and-variables"></a>Configuración y variables

También puede configurar manualmente el entorno agregando algo parecido a lo siguiente en el archivo de Autoexec.bat. Con Windows, puede editar el archivo de Autoexec.bat para incluir estos comandos. Con Windows Server 2003, Windows XP, Windows 2000 o Windows NT, puede editar o agregar estos valores a las variables de entorno mediante el cuadro de diálogo del sistema que puede ejecutar desde el panel de control.


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



Esta configuración es adecuada para una plataforma Intel 80386 o posterior que ejecute Windows me, Windows 98 o Windows 95 con Microsoft Visual C++ y el SDK de la plataforma instalado. Por ejemplo, en este sistema, Visual C++ versión 5,0 se instala en el directorio C: \\ MSDEV El SDK de la plataforma se instala en el \\ directorio D: MSSDK. La configuración del disco puede ser diferente. Los directorios del SDK de la plataforma (para este ejemplo, los que tienen D: \\ MSSDK en ellos) se encuentran anteriormente en cada secuencia de ruta de acceso. Esta secuencia presupone que las compilaciones de la línea de comandos están pensadas para ejecutarse en la ventana del símbolo del sistema y que los archivos de la biblioteca. h include y. lib del SDK de la plataforma son preferibles para esas compilaciones.

La variable de entorno CPU se define para controlar las compilaciones de Win32, dependiendo de la plataforma. Los valores posibles actuales incluyen i386, MIPS, ALPHA y PPC. Para obtener más información, vea el archivo Win32. Mak proporcionado en el SDK de la plataforma en el \\ Directorio de inclusión de MSSDK \\ . Todos los archivos make de ejemplo de código del tutorial de COM incluyen Win32. Mak.

 

 




