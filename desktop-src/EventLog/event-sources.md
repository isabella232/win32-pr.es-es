---
description: Cada registro de la clave EventLog contiene subclaves denominadas orígenes de eventos. El origen del evento es el nombre del software que registra el evento.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Orígenes de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666971"
---
# <a name="event-sources"></a><span data-ttu-id="2552c-104">Orígenes de eventos</span><span class="sxs-lookup"><span data-stu-id="2552c-104">Event Sources</span></span>

<span data-ttu-id="2552c-105">Cada registro de la [clave EventLog](eventlog-key.md) contiene subclaves denominadas *orígenes de eventos*.</span><span class="sxs-lookup"><span data-stu-id="2552c-105">Each log in the [Eventlog key](eventlog-key.md) contains subkeys called *event sources*.</span></span> <span data-ttu-id="2552c-106">El origen del evento es el nombre del software que registra el evento.</span><span class="sxs-lookup"><span data-stu-id="2552c-106">The event source is the name of the software that logs the event.</span></span> <span data-ttu-id="2552c-107">Suele ser el nombre de la aplicación o el nombre de un subcomponente de la aplicación si la aplicación es grande.</span><span class="sxs-lookup"><span data-stu-id="2552c-107">It is often the name of the application or the name of a subcomponent of the application if the application is large.</span></span> <span data-ttu-id="2552c-108">Puede Agregar un máximo de 16.384 orígenes de eventos al registro.</span><span class="sxs-lookup"><span data-stu-id="2552c-108">You can add a maximum of 16,384 event sources to the registry.</span></span> <span data-ttu-id="2552c-109">El registro de **seguridad** es solo para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="2552c-109">The **Security** log is for system use only.</span></span> <span data-ttu-id="2552c-110">Los controladores de dispositivo deben agregar sus nombres al registro **del sistema** .</span><span class="sxs-lookup"><span data-stu-id="2552c-110">Device drivers should add their names to the **System** log.</span></span> <span data-ttu-id="2552c-111">Las aplicaciones y los servicios deben agregar sus nombres al registro de la **aplicación** o crear un registro personalizado.</span><span class="sxs-lookup"><span data-stu-id="2552c-111">Applications and services should add their names to the **Application** log or create a custom log.</span></span>

<span data-ttu-id="2552c-112">La estructura de los orígenes de eventos es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="2552c-112">The structure of the event sources is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

<span data-ttu-id="2552c-113">No se puede usar un nombre de origen que ya se haya usado como nombre de registro.</span><span class="sxs-lookup"><span data-stu-id="2552c-113">You cannot use a source name that has already been used as a log name.</span></span> <span data-ttu-id="2552c-114">Además, los nombres de origen no pueden ser jerárquicos; es decir, no pueden contener el carácter de barra diagonal inversa (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="2552c-114">In addition, source names cannot be hierarchical; that is, they cannot contain the backslash character ("\\").</span></span>

<span data-ttu-id="2552c-115">Cada origen de eventos contiene información (por ejemplo, un [archivo de mensajes](message-files.md)) específica del software que registrará los eventos, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2552c-115">Each event source contains information (such as a [message file](message-files.md)) specific to the software that will be logging the events, as shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2552c-116">Valor del registro</span><span class="sxs-lookup"><span data-stu-id="2552c-116">Registry Value</span></span></th>
<th><span data-ttu-id="2552c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2552c-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2552c-118"><strong>CategoryCount</strong></span><span class="sxs-lookup"><span data-stu-id="2552c-118"><strong>CategoryCount</strong></span></span></td>
<td><span data-ttu-id="2552c-119">Número de categorías de eventos admitidas.</span><span class="sxs-lookup"><span data-stu-id="2552c-119">Number of event categories supported.</span></span> <span data-ttu-id="2552c-120">Este valor es de tipo <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="2552c-120">This value is of type <strong>REG_DWORD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2552c-121"><strong>CategoryMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="2552c-121"><strong>CategoryMessageFile</strong></span></span></td>
<td><span data-ttu-id="2552c-122">Ruta de acceso al archivo de mensajes de categoría.</span><span class="sxs-lookup"><span data-stu-id="2552c-122">Path to the category message file.</span></span> <span data-ttu-id="2552c-123">Un archivo de mensaje de categoría contiene cadenas dependientes del idioma que describen las categorías.</span><span class="sxs-lookup"><span data-stu-id="2552c-123">A category message file contains language-dependent strings that describe the categories.</span></span> <span data-ttu-id="2552c-124">Este valor puede ser de tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="2552c-124">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2552c-125"><strong>EventMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="2552c-125"><strong>EventMessageFile</strong></span></span></td>
<td><span data-ttu-id="2552c-126">Ruta de acceso a uno o más archivos de mensajes de eventos; Use un punto y coma para delimitar varios archivos.</span><span class="sxs-lookup"><span data-stu-id="2552c-126">Path to one or more event message files; use a semicolon to delimit multiple files.</span></span> <span data-ttu-id="2552c-127">Un archivo de mensajes de evento contiene cadenas dependientes del lenguaje que describen los eventos.</span><span class="sxs-lookup"><span data-stu-id="2552c-127">An event message file contains language-dependent strings that describe the events.</span></span> <span data-ttu-id="2552c-128">Este valor puede ser de tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="2552c-128">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2552c-129"><strong>ParameterMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="2552c-129"><strong>ParameterMessageFile</strong></span></span></td>
<td><span data-ttu-id="2552c-130">Ruta de acceso al archivo de mensajes de parámetros.</span><span class="sxs-lookup"><span data-stu-id="2552c-130">Path to the parameter message file.</span></span> <span data-ttu-id="2552c-131">Un archivo de mensajes de parámetros contiene cadenas independientes del lenguaje que se van a insertar en las cadenas de Descripción del evento.</span><span class="sxs-lookup"><span data-stu-id="2552c-131">A parameter message file contains language-independent strings that are to be inserted into the event description strings.</span></span> <span data-ttu-id="2552c-132">Este valor puede ser de tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="2552c-132">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2552c-133"><strong>TypesSupported</strong></span><span class="sxs-lookup"><span data-stu-id="2552c-133"><strong>TypesSupported</strong></span></span></td>
<td><span data-ttu-id="2552c-134">Máscara de máscara de los tipos admitidos.</span><span class="sxs-lookup"><span data-stu-id="2552c-134">Bitmask of supported types.</span></span> <span data-ttu-id="2552c-135">Este valor es de tipo <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="2552c-135">This value is of type <strong>REG_DWORD</strong>.</span></span> <span data-ttu-id="2552c-136">Puede ser uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2552c-136">It can be one or more of the following values:</span></span> <dl> <span data-ttu-id="2552c-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span><span class="sxs-lookup"><span data-stu-id="2552c-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span></span><br /><span data-ttu-id="2552c-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span><span class="sxs-lookup"><span data-stu-id="2552c-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span></span><br /><span data-ttu-id="2552c-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span><span class="sxs-lookup"><span data-stu-id="2552c-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span></span><br /><span data-ttu-id="2552c-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span><span class="sxs-lookup"><span data-stu-id="2552c-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span></span><br /><span data-ttu-id="2552c-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span><span class="sxs-lookup"><span data-stu-id="2552c-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2552c-142">Cuando una aplicación utiliza la función [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para obtener un identificador de un registro de eventos, el servicio de registro de eventos busca el origen de eventos especificado en el registro.</span><span class="sxs-lookup"><span data-stu-id="2552c-142">When an application uses the [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to get a handle to an event log, the event logging service searches for the specified event source in the registry.</span></span> <span data-ttu-id="2552c-143">Por ejemplo, el registro de **aplicación** puede contener orígenes de eventos para Microsoft SQL Server y Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="2552c-143">For example, the **Application** log might contain event sources for Microsoft SQL Server and Microsoft Excel.</span></span> <span data-ttu-id="2552c-144">Si una aplicación utiliza [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o **OpenEventLog** con un nombre de origen de aplicación, SQL o Excel, el servicio de registro de eventos devuelve un identificador al registro de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="2552c-144">If an application uses [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or **OpenEventLog** with a source name of Application, SQL, or Excel, the event logging service returns a handle to the **Application** log.</span></span>

<span data-ttu-id="2552c-145">Una aplicación puede utilizar el registro de **aplicaciones** sin agregar un nuevo origen de eventos al registro.</span><span class="sxs-lookup"><span data-stu-id="2552c-145">An application can use the **Application** log without adding a new event source to the registry.</span></span> <span data-ttu-id="2552c-146">Si la aplicación llama a [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) y pasa un nombre de origen que no se encuentra en el registro, el servicio de registro de eventos utiliza el registro de la **aplicación** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2552c-146">If the application calls [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) and passes a source name that cannot be found in the registry, the event-logging service uses the **Application** log by default.</span></span> <span data-ttu-id="2552c-147">Sin embargo, dado que no hay archivos de mensajes, el Visor de eventos no puede asignar ningún identificador de evento o categoría de eventos a una cadena de descripción, y mostrará un error.</span><span class="sxs-lookup"><span data-stu-id="2552c-147">However, because there are no message files, the Event Viewer cannot map any event identifiers or event categories to a description string, and will display an error.</span></span> <span data-ttu-id="2552c-148">Por esta razón, debe agregar un origen de eventos único al registro de la aplicación y especificar un archivo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2552c-148">For this reason, you should add a unique event source to the registry for your application and specify a message file.</span></span>

 

 



