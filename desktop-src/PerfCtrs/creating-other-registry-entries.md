---
description: La función OpenPerformanceData de archivos DLL de rendimiento toma un argumento de cadena como entrada.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Crear otras entradas del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ad9fe960713a481ba5a9b8f4b73e11bdbdd4d9fe9474b04b994e373ce8e1bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683975"
---
# <a name="creating-other-registry-entries"></a>Crear otras entradas del Registro

La función [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) del archivo DLL de rendimiento toma un argumento de cadena como entrada. Para proporcionar una cadena de entrada a la función abierta, incluya una **clave de vinculación** en la **clave de** servicios. La **clave Vinculación** contiene un **valor export.** Establezca los datos de valor de **Exportar** en la cadena de entrada que desea pasar a la función abierta. El tipo de datos **de Export** es REG **MULTI \_ \_ SZ.**

Si **no** se define Export **(La exportación** es opcional), el sistema pasa **NULL** a la [**función OpenPerformanceData.**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))

Normalmente, si más de una aplicación comparte el  mismo archivo  DLL de rendimiento, cada aplicación incluye una clave de vinculación y un valor de exportación para proporcionar contexto sobre a qué aplicación llama al archivo DLL.

A continuación se muestran las entradas del Registro:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

De forma predeterminada, las funciones [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) y [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) de la DLL de rendimiento deben devolver en un plazo de 10 000 milisegundos. Si no es así, el sistema no usa los datos que devuelve el archivo DLL. La aplicación puede aumentar o disminuir el valor  de tiempo de  espera especificando un valor del Registro Tiempo de espera de apertura o Recopilar tiempo de espera en su clave de rendimiento, como se muestra en el ejemplo siguiente. 

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

Para obtener los datos de rendimiento de algunas aplicaciones (aquellas que devuelven contadores mediante la función [**DeviceIoControl),**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) es necesario usar la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir el dispositivo asociado a la aplicación. En este caso, el nombre especificado en **CreateFile** también debe instalarse en el nodo Dispositivos DOS del Registro, como se muestra aquí:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
