---
description: Una aplicación que admita contadores de rendimiento debe tener una clave de rendimiento en la clave Servicios. En el ejemplo siguiente se muestran los valores que debe incluir para esta clave.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Creación de la clave de rendimiento de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149e8142b892edeb43f5459fe68bc6ad4b7453118c64cb2e288bb334c054fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144038"
---
# <a name="creating-the-applications-performance-key"></a>Creación de la clave de rendimiento de la aplicación

Una aplicación que admita contadores de rendimiento debe tener una **clave de** rendimiento en la **clave** Servicios. En el ejemplo siguiente se muestran los valores que debe incluir para esta clave.

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

El **valor** Biblioteca proporciona el nombre del archivo DLL  de rendimiento y los valores **Abrir,** **Recopilar** y Cerrar proporcionan los nombres de las funciones exportadas desde el archivo DLL de rendimiento. El tipo de datos de estos valores es **REG \_ SZ.** Cuando un consumidor solicita datos de rendimiento, el sistema usa estos valores para determinar qué archivos DLL de rendimiento se cargarán y a qué funciones DLL llamar.

El **valor** biblioteca puede contener el nombre del archivo DLL o una ruta de acceso completa al archivo DLL. Si usa el tipo **de datos REG EXPAND \_ \_ SZ** para **Library**, puede especificar variables de entorno en la ruta de acceso.

La clave de servicio de la aplicación debe existir antes de poder ejecutar **lodctr** para cargar los nombres de los contadores y las cadenas de ayuda.

Para obtener valores del Registro adicionales que puede crear, como especificar valores de tiempo de espera para las funciones [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) y [**CollectPerformanceData,**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) vea [Creating Other Registry Entries](creating-other-registry-entries.md).

 

 
