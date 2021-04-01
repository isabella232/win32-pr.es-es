---
description: El proveedor WMI del recopilador de eventos de arranque proporciona acceso a la información de conexión y configuración para la característica de recopilación de eventos de instalación y arranque en Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Proveedor WMI del recopilador de eventos de arranque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906946"
---
# <a name="boot-event-collector-wmi-provider"></a><span data-ttu-id="252c6-103">Proveedor WMI del recopilador de eventos de arranque</span><span class="sxs-lookup"><span data-stu-id="252c6-103">Boot Event Collector WMI Provider</span></span>

## <a name="purpose"></a><span data-ttu-id="252c6-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="252c6-104">Purpose</span></span>

<span data-ttu-id="252c6-105">El proveedor WMI del recopilador de eventos de arranque proporciona acceso a la información de conexión y configuración para la característica de recopilación de eventos de instalación y arranque en Windows Server.</span><span class="sxs-lookup"><span data-stu-id="252c6-105">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span> <span data-ttu-id="252c6-106">Esto le permite ver una lista de las conexiones actuales y el historial de conexiones entre un servidor del recopilador y sus equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="252c6-106">This allows you to view a list of the current connections and the connection history between a collector server and its target computers.</span></span> <span data-ttu-id="252c6-107">Además, este proveedor le permite administrar la configuración de un servidor de recopilador.</span><span class="sxs-lookup"><span data-stu-id="252c6-107">In addition, this provider allows you to manage the configuration of a collector server.</span></span>

> [!Note]  
> <span data-ttu-id="252c6-108">El proveedor WMI del recopilador de eventos de arranque se implementa en BEvtCol.exe.</span><span class="sxs-lookup"><span data-stu-id="252c6-108">The Boot Event Collector WMI provider is implemented in BEvtCol.exe.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="252c6-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="252c6-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="252c6-110">**TargetForwarding**</span><span class="sxs-lookup"><span data-stu-id="252c6-110">**TargetForwarding**</span></span>](targetforwarding.md)
</dt> <dd>

<span data-ttu-id="252c6-111">Recupera los datos de reenvío de un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="252c6-111">Retrieves forwarding data from a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="252c6-112">**TargetForwardingDestination**</span><span class="sxs-lookup"><span data-stu-id="252c6-112">**TargetForwardingDestination**</span></span>](targetforwardingdestination.md)
</dt> <dd>

<span data-ttu-id="252c6-113">Destinos conocidos que contienen los datos recopilados.</span><span class="sxs-lookup"><span data-stu-id="252c6-113">The known destinations containing the collected data.</span></span> <span data-ttu-id="252c6-114">Solo está disponible si el recopilador se está ejecutando con el registro de estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="252c6-114">Available only if the collector is running with the status log enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="252c6-115">**TargetForwardingHistory**</span><span class="sxs-lookup"><span data-stu-id="252c6-115">**TargetForwardingHistory**</span></span>](targetforwardinghistory.md)
</dt> <dd>

<span data-ttu-id="252c6-116">El historial reciente de cambios en los datos de reenvío para un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="252c6-116">The recent history of changes to the forwarding data for a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="252c6-117">**Control**</span><span class="sxs-lookup"><span data-stu-id="252c6-117">**Control**</span></span>](control.md)
</dt> <dd>

<span data-ttu-id="252c6-118">Control de la instancia del recopilador.</span><span class="sxs-lookup"><span data-stu-id="252c6-118">Control of the collector instance.</span></span> <span data-ttu-id="252c6-119">Requiere los privilegios de administrador (BA).</span><span class="sxs-lookup"><span data-stu-id="252c6-119">Requires the Administrator (BA) privileges.</span></span>

</dd> </dl>

 

 



