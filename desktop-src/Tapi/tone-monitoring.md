---
description: La supervisión de tonos supervisa el flujo multimedia de una llamada para los tonos especificados.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Supervisión de tonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082762"
---
# <a name="tone-monitoring"></a><span data-ttu-id="9c44a-103">Supervisión de tonos</span><span class="sxs-lookup"><span data-stu-id="9c44a-103">Tone Monitoring</span></span>

<span data-ttu-id="9c44a-104">La supervisión de tonos supervisa el flujo multimedia de una llamada para los tonos especificados.</span><span class="sxs-lookup"><span data-stu-id="9c44a-104">Tone monitoring monitors the media stream of a call for specified tones.</span></span> <span data-ttu-id="9c44a-105">Un tono se describe mediante sus frecuencias de componente y cadencia.</span><span class="sxs-lookup"><span data-stu-id="9c44a-105">A tone is described by its component frequencies and cadence.</span></span> <span data-ttu-id="9c44a-106">Una implementación de la API puede permitir que se supervisen varios tonos diferentes simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="9c44a-106">An implementation of the API may allow several different tones to be monitored simultaneously.</span></span> <span data-ttu-id="9c44a-107">Una aplicación puede etiquetar cada tono para poder distinguir los distintos tonos para los que solicita detección.</span><span class="sxs-lookup"><span data-stu-id="9c44a-107">An application can tag each tone to be able to distinguish the different tones for which it requests detection.</span></span>

<span data-ttu-id="9c44a-108">Una aplicación puede habilitar o deshabilitar la supervisión de tono en una llamada especificada con [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span><span class="sxs-lookup"><span data-stu-id="9c44a-108">An application can enable or disable tone monitoring on a specified call with [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span></span> <span data-ttu-id="9c44a-109">Con esta función, la aplicación indica qué tonos detectar en una llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="9c44a-109">With this function, the application indicates which tones to detect on a specified call.</span></span> <span data-ttu-id="9c44a-110">Cuando está habilitada la supervisión de tonos, los dígitos detectados hacen que la aplicación reciba una notificación con el mensaje [**line \_ MONITORTONE**](line-monitortone.md) .</span><span class="sxs-lookup"><span data-stu-id="9c44a-110">When tone monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORTONE**](line-monitortone.md) message.</span></span> <span data-ttu-id="9c44a-111">Este mensaje proporciona el identificador de llamada en el que se detectó el tono, así como la etiqueta de la aplicación para el tono.</span><span class="sxs-lookup"><span data-stu-id="9c44a-111">This message provides the call handle on which the tone was detected as well as the application's tag for the tone.</span></span>

<span data-ttu-id="9c44a-112">El ámbito de la supervisión de tonos está limitado por la duración de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9c44a-112">The scope of tone monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="9c44a-113">La supervisión de tonos en una llamada finaliza en cuanto la llamada se *desconecta* o se queda *inactiva*.</span><span class="sxs-lookup"><span data-stu-id="9c44a-113">Tone monitoring on a call ends as soon the call *disconnects* or goes *idle*.</span></span>

> [!Note]  
> <span data-ttu-id="9c44a-114">La supervisión de los tonos, los dígitos o los tipos de medios a menudo requiere el uso de recursos de los que el proveedor de servicios solo puede tener una cantidad finita.</span><span class="sxs-lookup"><span data-stu-id="9c44a-114">The monitoring of tones, digits, or media types often requires the use of resources of which the service provider can only have a finite amount.</span></span> <span data-ttu-id="9c44a-115">Si los recursos no están disponibles, se puede rechazar una solicitud de supervisión.</span><span class="sxs-lookup"><span data-stu-id="9c44a-115">A request for monitoring can be rejected if resources are not available.</span></span> <span data-ttu-id="9c44a-116">Por la misma razón, una aplicación debe deshabilitar cualquier supervisión innecesaria.</span><span class="sxs-lookup"><span data-stu-id="9c44a-116">For the same reason, an application should disable any unnecessary monitoring.</span></span>

 

 

 



