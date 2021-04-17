---
description: Los proveedores de hora usan las siguientes funciones.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Funciones de proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668149"
---
# <a name="time-provider-functions"></a><span data-ttu-id="f0ba4-103">Funciones de proveedor de hora</span><span class="sxs-lookup"><span data-stu-id="f0ba4-103">Time Provider Functions</span></span>

<span data-ttu-id="f0ba4-104">Los proveedores de hora usan las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-104">The following functions are used by time providers.</span></span>



| <span data-ttu-id="f0ba4-105">Función</span><span class="sxs-lookup"><span data-stu-id="f0ba4-105">Function</span></span>                                                               | <span data-ttu-id="f0ba4-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0ba4-106">Description</span></span>                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0ba4-107">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="f0ba4-107">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | <span data-ttu-id="f0ba4-108">Notifica al sistema que hay nuevas muestras disponibles.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-108">Notifies the system that there are new samples available.</span></span>                                              |
| [<span data-ttu-id="f0ba4-109">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="f0ba4-109">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | <span data-ttu-id="f0ba4-110">Recupera la información de estado de hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-110">Retrieves the system time state information.</span></span>                                                           |
| [<span data-ttu-id="f0ba4-111">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="f0ba4-111">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | <span data-ttu-id="f0ba4-112">Registra un evento de proveedor de hora en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-112">Logs a time provider event in the event log.</span></span>                                                           |
| [<span data-ttu-id="f0ba4-113">**SetProviderStatusFunc**</span><span class="sxs-lookup"><span data-stu-id="f0ba4-113">**SetProviderStatusFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | <span data-ttu-id="f0ba4-114">Establece la información de estado del proveedor de hora.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-114">Sets the time provider's status information.</span></span>                                                           |
| [<span data-ttu-id="f0ba4-115">**SetProviderStatusInfoFreeFunc**</span><span class="sxs-lookup"><span data-stu-id="f0ba4-115">**SetProviderStatusInfoFreeFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | <span data-ttu-id="f0ba4-116">Libera una estructura [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) .</span><span class="sxs-lookup"><span data-stu-id="f0ba4-116">Frees a [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) structure.</span></span>                          |
| [<span data-ttu-id="f0ba4-117">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="f0ba4-117">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | <span data-ttu-id="f0ba4-118">Función de devolución de llamada a la que llama el administrador de proveedores de hora para cerrar el proveedor de hora.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-118">A callback function that is called by the time provider manager to shut down the time provider.</span></span>        |
| [<span data-ttu-id="f0ba4-119">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="f0ba4-119">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | <span data-ttu-id="f0ba4-120">Función de devolución de llamada a la que llama el administrador de proveedores de hora para enviar comandos al proveedor de hora.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-120">A callback function that is called by the time provider manager to send commands to the time provider.</span></span> |
| [<span data-ttu-id="f0ba4-121">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="f0ba4-121">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | <span data-ttu-id="f0ba4-122">Función de devolución de llamada a la que llama el administrador de proveedores de hora cuando se carga el archivo DLL del proveedor de hora.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-122">A callback function that is called by the time provider manager when the time provider DLL is loaded.</span></span>  |



 

 

 



