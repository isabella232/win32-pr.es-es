---
title: Configuración del entorno
description: El Kit de desarrollo de software (SDK) de plataforma instalado proporciona un archivo Setenv.bat ubicado en el directorio raíz del SDK de plataforma que puede ejecutar para configurar el entorno para compilar aplicaciones que usan el SDK de plataforma.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1b7de27bfc015726786011376c821c5ae0e86a07d95f03098ed376dd022cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739395"
---
# <a name="environment-setup"></a>Configuración del entorno

El Kit de desarrollo de software (SDK) de plataforma instalado proporciona un archivo Setenv.bat ubicado en el directorio raíz del SDK de plataforma que puede ejecutar para configurar el entorno para compilar aplicaciones que usan el SDK de plataforma.

## <a name="settings-and-variables"></a>Configuración y variables

También puede configurar manualmente el entorno agregando algo parecido a lo siguiente al archivo Autoexec.bat usuario. Con Windows, puede editar el archivo Autoexec.bat para incluir estos comandos. Con Windows Server 2003, Windows XP, Windows 2000 o Windows NT, puede editar o agregar esta configuración a las variables de entorno mediante el cuadro de diálogo Sistema que puede ejecutar desde la Panel de control.


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



Esta configuración es adecuada para una plataforma Intel 80386 o posterior que ejecuta Windows Me, Windows 98 o Windows 95 con Microsoft Visual C++ y el SDK de plataforma instalados. Por ejemplo, en este sistema, Visual C++ versión 5.0 se instala en el directorio C: \\ MSDEV. El SDK de plataforma se instala en el directorio D: \\ MSSDK. La configuración del disco puede ser diferente. Los directorios del SDK de plataforma (en este ejemplo, los que tienen D: MSSDK) están todos antes \\ en cada secuencia de ruta de acceso. En esta secuencia se da por supuesto que las compilaciones de línea de comandos están diseñadas para ejecutarse en la ventana del símbolo del sistema y que los archivos de biblioteca .h include y .lib del SDK de plataforma son los preferidos para esas compilaciones.

La variable de entorno de CPU se define para controlar las compilaciones de Win32, en función de la plataforma. Los valores posibles actuales incluyen i386, MIPS, ALPHA y PPC. Para más información, consulte el archivo Win32.mak proporcionado en platform SDK en el directorio INCLUDE de \\ MSSDK. \\ Todos los archivos make de ejemplo de código del tutorial COM incluyen Win32.mak.

 

 




