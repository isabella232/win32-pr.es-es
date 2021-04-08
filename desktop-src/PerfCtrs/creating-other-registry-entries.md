---
description: La función OpenPerformanceData de los archivos dll de rendimiento toma un argumento de cadena como entrada.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Crear otras entradas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dfc3b46ce642069210df5112eb41cac9a038797
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001981"
---
# <a name="creating-other-registry-entries"></a>Crear otras entradas del registro

La función [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) de la dll de rendimiento toma un argumento de cadena como entrada. Para proporcionar una cadena de entrada a la función abierta, incluya una clave de **vinculación** en la clave de **servicios** . La clave de **vinculación** contiene un valor de **exportación** . Establezca los datos de valor para **exportar** a la cadena de entrada que desea pasar a la función abierta. El tipo de datos de **Export** es **reg \_ multi \_ SZ**.

Si no se define **Export** (la **exportación** es opcional), el sistema pasa **null** a la función [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .

Normalmente, si más de una aplicación comparte el mismo archivo DLL de rendimiento, cada aplicación incluye una clave de **vinculación** y un valor de **exportación** para proporcionar el contexto en el que la aplicación llama a la dll.

A continuación se muestran las entradas del registro:

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

De forma predeterminada, las funciones [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) y [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) del archivo dll de rendimiento deben volver en 10.000 milisegundos. De lo contrario, el sistema no utiliza los datos devueltos por el archivo DLL. La aplicación puede aumentar o disminuir el valor de tiempo de espera especificando un tiempo de espera de **apertura** o el valor del registro de **tiempo de espera de recopilación** bajo su clave de **rendimiento** , tal como se muestra en el ejemplo siguiente.

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

Para obtener los datos de rendimiento de algunas aplicaciones (las que devuelven contadores mediante la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ), es necesario usar la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir el dispositivo asociado a la aplicación. En este caso, el nombre especificado en **CreateFile** también debe instalarse en el nodo dispositivos dos del registro, como se muestra aquí:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
