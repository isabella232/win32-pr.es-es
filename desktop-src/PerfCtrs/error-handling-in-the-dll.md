---
description: Utilice el registro de eventos para registrar los errores que se producen en el archivo DLL de rendimiento.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Control de errores en el archivo DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001978"
---
# <a name="error-handling-in-the-dll"></a><span data-ttu-id="63dbc-103">Control de errores en el archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63dbc-103">Error Handling in the DLL</span></span>

<span data-ttu-id="63dbc-104">Utilice el registro de eventos para registrar los errores que se producen en el archivo DLL de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="63dbc-104">Use event logging to record errors that occur in the performance DLL.</span></span> <span data-ttu-id="63dbc-105">El registro de eventos de error ayuda en la solución de problemas de aplicaciones que proporcionan datos de rendimiento durante el desarrollo y después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="63dbc-105">Logging error events aids in troubleshooting applications that provide performance data during development and after installation.</span></span> <span data-ttu-id="63dbc-106">Debe limitar la cantidad de registro de errores que se produce en la función [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) porque la recopilación de datos puede ser frecuente.</span><span class="sxs-lookup"><span data-stu-id="63dbc-106">You should limit the amount of error logging that occurs in the [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) function because data collection can be frequent.</span></span>

<span data-ttu-id="63dbc-107">El sistema registra los siguientes errores en el registro de eventos si hay problemas con la función [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="63dbc-107">The system logs the following errors to the event log if there are problems with the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span> <span data-ttu-id="63dbc-108">Si se produce uno de los siguientes errores, el sistema no vuelve a llamar al archivo DLL de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="63dbc-108">If one of the following errors occurs, the system does not call the performance DLL again.</span></span> <span data-ttu-id="63dbc-109">En su lugar, se descarga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="63dbc-109">Instead, the DLL is unloaded.</span></span>

-   <span data-ttu-id="63dbc-110">**PERFLIB \_ OPEN \_ proc \_ not \_ found**: se registra cuando el nombre de procedimiento definido en el registro no se pudo encontrar en el archivo dll como una función exportada.</span><span class="sxs-lookup"><span data-stu-id="63dbc-110">**PERFLIB\_OPEN\_PROC\_NOT\_FOUND**—Logged when the procedure name defined in the registry could not be found in the DLL as an exported function.</span></span> <span data-ttu-id="63dbc-111">Esto suele ocurrir cuando el archivo DLL o el servicio no está instalado correctamente o se ha cambiado el nombre de la función sin actualizar el procedimiento de instalación.</span><span class="sxs-lookup"><span data-stu-id="63dbc-111">This usually occurs when the DLL or the service is not installed correctly or the function name has been renamed without updating the installation procedure.</span></span>
-   <span data-ttu-id="63dbc-112">**PERFLIB \_ OPEN \_ proc \_ error**: se registra cuando el procedimiento abierto devolvió un estado de error que no es \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="63dbc-112">**PERFLIB\_OPEN\_PROC\_FAILURE**—Logged when the open procedure returned an error status other than ERROR\_SUCCESS.</span></span> <span data-ttu-id="63dbc-113">En caso de que esto suceda, el archivo DLL debe haber especificado también una entrada en el registro de eventos que describe las condiciones que han provocado el error.</span><span class="sxs-lookup"><span data-stu-id="63dbc-113">Should this happen, the DLL should have also entered an event log entry describing the conditions that caused the failure.</span></span>
-   <span data-ttu-id="63dbc-114">**PERFLIB \_ OPEN \_ proc \_ Exception**: se registra cuando el procedimiento abierto encuentra una excepción no controlada.</span><span class="sxs-lookup"><span data-stu-id="63dbc-114">**PERFLIB\_OPEN\_PROC\_EXCEPTION**—Logged when the open procedure encounters an unhandled exception.</span></span> <span data-ttu-id="63dbc-115">Esto suele deberse a una condición de error inesperada detectada por el procedimiento abierto.</span><span class="sxs-lookup"><span data-stu-id="63dbc-115">This is usually due to an unexpected error condition encountered by the open procedure.</span></span>

 

 
