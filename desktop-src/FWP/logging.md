---
title: Registro (plataforma de filtrado de Windows)
description: La plataforma de filtrado de Windows (WFP) proporciona el registro de caídas de paquetes y errores de IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105665903"
---
# <a name="logging-windows-filtering-platform"></a><span data-ttu-id="e8384-103">Registro (plataforma de filtrado de Windows)</span><span class="sxs-lookup"><span data-stu-id="e8384-103">Logging (Windows Filtering Platform)</span></span>

<span data-ttu-id="e8384-104">La plataforma de filtrado de Windows (WFP) proporciona el registro de caídas de paquetes y errores de IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="e8384-104">The Windows Filtering Platform (WFP) provides logging of packet drops and IKE/AuthIP failures.</span></span>

<span data-ttu-id="e8384-105">Los eventos registrados se definen en el tipo enumerado de [**\_ tipo de \_ evento \_ FWPM net**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) y son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e8384-105">The logged events are defined in the [**FWPM\_NET\_EVENT\_TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) enumerated type and are as follows.</span></span>

-   <span data-ttu-id="e8384-106">Errores de modo principal de IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="e8384-106">IKE/AuthIP main mode failures.</span></span>
-   <span data-ttu-id="e8384-107">Errores de modo rápido de IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="e8384-107">IKE/AuthIP quick mode failures.</span></span>
-   <span data-ttu-id="e8384-108">Errores de modo extendido de AuthIP.</span><span class="sxs-lookup"><span data-stu-id="e8384-108">AuthIP extended mode failures.</span></span>
-   <span data-ttu-id="e8384-109">Paquetes descartados durante la clasificación.</span><span class="sxs-lookup"><span data-stu-id="e8384-109">Packets dropped during classification.</span></span>
-   <span data-ttu-id="e8384-110">Paquetes descartados por IPsec.</span><span class="sxs-lookup"><span data-stu-id="e8384-110">Packets dropped by IPsec.</span></span>

<span data-ttu-id="e8384-111">De forma predeterminada, el registro de WFP está habilitado para los paquetes entrantes de unidifusión y para todos los paquetes salientes (unidifusión, multidifusión y difusión).</span><span class="sxs-lookup"><span data-stu-id="e8384-111">By default, logging for WFP is enabled for unicast inbound packets and for all outbound packets (unicast, multicast, and broadcast).</span></span> <span data-ttu-id="e8384-112">El registro se puede habilitar para el resto de los paquetes o deshabilitarse para todos los paquetes a través de la función de administración [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) .</span><span class="sxs-lookup"><span data-stu-id="e8384-112">Logging can be enabled for the rest of the packets, or disabled for all packets, through the [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) management function.</span></span> <span data-ttu-id="e8384-113">La configuración de eventos se mantiene entre reinicios.</span><span class="sxs-lookup"><span data-stu-id="e8384-113">Event settings persist across reboots.</span></span>

<span data-ttu-id="e8384-114">Los eventos registrados se almacenan en un registro circular, es decir, los nuevos eventos reemplazan a los antiguos cuando el registro alcanza su tamaño máximo y se pueden analizar con las funciones de [Administración de eventos](fwp-mgmt-functions.md) que proporciona WFP.</span><span class="sxs-lookup"><span data-stu-id="e8384-114">Logged events are stored in a circular log, that is new events override old ones when the log reaches its maximum size, and can be analyzed using the [event management](fwp-mgmt-functions.md) functions provided by WFP.</span></span> <span data-ttu-id="e8384-115">El registro de eventos tiene un tamaño máximo de 128 KB y puede contener aproximadamente 100 a 150 eventos.</span><span class="sxs-lookup"><span data-stu-id="e8384-115">The event log has a maximum size of 128 KB and it can hold about 100 to 150 events.</span></span>

<span data-ttu-id="e8384-116">Las funciones de enumeración en general y [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) en concreto, toman una instantánea del registro en el momento en que se crea el identificador de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="e8384-116">Enumeration functions in general, and [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)/[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particular, take a snapshot of the log at the time the enumeration handle is created.</span></span> <span data-ttu-id="e8384-117">Las llamadas subsiguientes que usan el mismo identificador de enumeración devuelven el siguiente conjunto de elementos que se encuentra en el último búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="e8384-117">Subsequent calls using the same enumeration handle return the next set of items following those in the last output buffer.</span></span>

<span data-ttu-id="e8384-118">Cuando una aplicación deshabilita el registro de WFP (llamando a [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), todas las aplicaciones se ven afectadas.</span><span class="sxs-lookup"><span data-stu-id="e8384-118">When an application disables WFP logging (by calling [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)) all applications are affected.</span></span> <span data-ttu-id="e8384-119">El registro de eventos no se limpia hasta que una aplicación vuelve a habilitar el registro de WFP, pero no se puede consultar el registro de eventos antes de.</span><span class="sxs-lookup"><span data-stu-id="e8384-119">The event log is not cleaned up until an application re-enables WFP logging, but the event log cannot be queried before then.</span></span>

<span data-ttu-id="e8384-120">El registro de eventos de WFP se vacía después de un reinicio.</span><span class="sxs-lookup"><span data-stu-id="e8384-120">The WFP event log is emptied after a reboot.</span></span>

 

 




