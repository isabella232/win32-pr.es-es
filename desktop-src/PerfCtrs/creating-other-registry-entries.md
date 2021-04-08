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
# <a name="creating-other-registry-entries"></a><span data-ttu-id="26c2f-103">Crear otras entradas del registro</span><span class="sxs-lookup"><span data-stu-id="26c2f-103">Creating Other Registry Entries</span></span>

<span data-ttu-id="26c2f-104">La función [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) de la dll de rendimiento toma un argumento de cadena como entrada.</span><span class="sxs-lookup"><span data-stu-id="26c2f-104">The performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function takes a string argument as input.</span></span> <span data-ttu-id="26c2f-105">Para proporcionar una cadena de entrada a la función abierta, incluya una clave de **vinculación** en la clave de **servicios** .</span><span class="sxs-lookup"><span data-stu-id="26c2f-105">To provide an input string to your open function, include a **Linkage** key under your **Services** key.</span></span> <span data-ttu-id="26c2f-106">La clave de **vinculación** contiene un valor de **exportación** .</span><span class="sxs-lookup"><span data-stu-id="26c2f-106">The **Linkage** key contains an **Export** value.</span></span> <span data-ttu-id="26c2f-107">Establezca los datos de valor para **exportar** a la cadena de entrada que desea pasar a la función abierta.</span><span class="sxs-lookup"><span data-stu-id="26c2f-107">Set the value data for **Export** to the input string that you want to pass to your open function.</span></span> <span data-ttu-id="26c2f-108">El tipo de datos de **Export** es **reg \_ multi \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="26c2f-108">The data type of **Export** is **REG\_MULTI\_SZ**.</span></span>

<span data-ttu-id="26c2f-109">Si no se define **Export** (la **exportación** es opcional), el sistema pasa **null** a la función [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="26c2f-109">If **Export** is not defined (**Export** is optional), the system passes **NULL** to your [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span>

<span data-ttu-id="26c2f-110">Normalmente, si más de una aplicación comparte el mismo archivo DLL de rendimiento, cada aplicación incluye una clave de **vinculación** y un valor de **exportación** para proporcionar el contexto en el que la aplicación llama a la dll.</span><span class="sxs-lookup"><span data-stu-id="26c2f-110">Typically, if more than one application shares the same performance DLL, each application includes a **Linkage** key and **Export** value to provide context as to which application is calling the DLL.</span></span>

<span data-ttu-id="26c2f-111">A continuación se muestran las entradas del registro:</span><span class="sxs-lookup"><span data-stu-id="26c2f-111">The following shows the registry entries:</span></span>

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

<span data-ttu-id="26c2f-112">De forma predeterminada, las funciones [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) y [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) del archivo dll de rendimiento deben volver en 10.000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="26c2f-112">By default, the performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions must return within 10,000 milliseconds.</span></span> <span data-ttu-id="26c2f-113">De lo contrario, el sistema no utiliza los datos devueltos por el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="26c2f-113">If not, the system does not use the data that the DLL returns.</span></span> <span data-ttu-id="26c2f-114">La aplicación puede aumentar o disminuir el valor de tiempo de espera especificando un tiempo de espera de **apertura** o el valor del registro de **tiempo de espera de recopilación** bajo su clave de **rendimiento** , tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="26c2f-114">The application can increase or decrease the timeout value by specifying an **Open Timeout** or **Collect Timeout** registry value under their **Performance** key as shown in the following example.</span></span>

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

<span data-ttu-id="26c2f-115">Para obtener los datos de rendimiento de algunas aplicaciones (las que devuelven contadores mediante la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ), es necesario usar la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir el dispositivo asociado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="26c2f-115">To obtain the performance data for some applications (those that return counters using the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function), it is necessary to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the device associated with the application.</span></span> <span data-ttu-id="26c2f-116">En este caso, el nombre especificado en **CreateFile** también debe instalarse en el nodo dispositivos dos del registro, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="26c2f-116">In this case, the name specified in **CreateFile** must also be installed in the DOS Devices node of the registry, as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
