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
# <a name="creating-the-applications-performance-key"></a><span data-ttu-id="4c851-104">Crear la clave de rendimiento de la aplicación</span><span class="sxs-lookup"><span data-stu-id="4c851-104">Creating the Application's Performance Key</span></span>

<span data-ttu-id="4c851-105">Una aplicación que admite contadores de rendimiento debe tener una clave de **rendimiento** en la clave **servicios** .</span><span class="sxs-lookup"><span data-stu-id="4c851-105">An application that supports performance counters must have a **Performance** key under the **Services** key.</span></span> <span data-ttu-id="4c851-106">En el ejemplo siguiente se muestran los valores que se deben incluir para esta clave.</span><span class="sxs-lookup"><span data-stu-id="4c851-106">The following example shows the values that you must include for this key.</span></span>

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

<span data-ttu-id="4c851-107">El valor de la **biblioteca** proporciona el nombre del archivo dll de rendimiento y los valores de **apertura**, **recopilación** y **cierre** proporcionan los nombres de las funciones exportadas desde el archivo dll de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4c851-107">The **Library** value provides the name of the performance DLL, and the **Open**, **Collect**, and **Close** values provide the names of the functions exported from the performance DLL.</span></span> <span data-ttu-id="4c851-108">El tipo de datos de estos valores es **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="4c851-108">The data type of these values is **REG\_SZ**.</span></span> <span data-ttu-id="4c851-109">Cuando un consumidor solicita datos de rendimiento, el sistema utiliza estos valores para determinar qué archivos dll de rendimiento se deben cargar y a qué funciones de DLL se debe llamar.</span><span class="sxs-lookup"><span data-stu-id="4c851-109">When a consumer requests performance data, the system uses these values to determine which performance DLLs to load and which DLL functions to call.</span></span>

<span data-ttu-id="4c851-110">El valor de la **biblioteca** puede contener el nombre de la dll o una ruta de acceso completa al archivo dll.</span><span class="sxs-lookup"><span data-stu-id="4c851-110">The **Library** value can contain the DLL name or a full path to the DLL.</span></span> <span data-ttu-id="4c851-111">Si usa el tipo de datos **reg \_ Expand \_ SZ** para la **biblioteca**, puede especificar variables de entorno en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4c851-111">If you use the **REG\_EXPAND\_SZ** data type for **Library**, you can specify environment variables in your path.</span></span>

<span data-ttu-id="4c851-112">La clave de servicio de la aplicación debe existir antes de poder ejecutar **LODCTR** para cargar los nombres de contadores y las cadenas de ayuda.</span><span class="sxs-lookup"><span data-stu-id="4c851-112">The application's service key must exist before you can run **lodctr** to load your counter names and help strings.</span></span>

<span data-ttu-id="4c851-113">Para los valores de registro adicionales que puede crear, como la especificación de valores de tiempo de espera para las funciones [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) y [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , consulte [crear otras entradas del registro](creating-other-registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="4c851-113">For additional registry values that you can create, such as specifying time out values for the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions, see [Creating Other Registry Entries](creating-other-registry-entries.md).</span></span>

 

 
