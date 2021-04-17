---
description: Una aplicación que admite contadores de rendimiento debe tener una clave de rendimiento en la clave servicios. En el ejemplo siguiente se muestran los valores que se deben incluir para esta clave.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Crear la clave de rendimiento de las aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d39fb89f7f5feb4e34284b541775b5c093a6bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667337"
---
# <a name="creating-the-applications-performance-key"></a>Crear la clave de rendimiento de la aplicación

Una aplicación que admite contadores de rendimiento debe tener una clave de **rendimiento** en la clave **servicios** . En el ejemplo siguiente se muestran los valores que se deben incluir para esta clave.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Library = Name of your performance DLL
                  Open = Name of your Open function in your DLL
                  Collect = Name of your Collect function in your DLL
                  Close = Name of your Close function in your DLL
```

El valor de la **biblioteca** proporciona el nombre del archivo dll de rendimiento y los valores de **apertura**, **recopilación** y **cierre** proporcionan los nombres de las funciones exportadas desde el archivo dll de rendimiento. El tipo de datos de estos valores es **reg \_ SZ**. Cuando un consumidor solicita datos de rendimiento, el sistema utiliza estos valores para determinar qué archivos dll de rendimiento se deben cargar y a qué funciones de DLL se debe llamar.

El valor de la **biblioteca** puede contener el nombre de la dll o una ruta de acceso completa al archivo dll. Si usa el tipo de datos **reg \_ Expand \_ SZ** para la **biblioteca**, puede especificar variables de entorno en la ruta de acceso.

La clave de servicio de la aplicación debe existir antes de poder ejecutar **LODCTR** para cargar los nombres de contadores y las cadenas de ayuda.

Para los valores de registro adicionales que puede crear, como la especificación de valores de tiempo de espera para las funciones [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) y [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , consulte [crear otras entradas del registro](creating-other-registry-entries.md).

 

 
