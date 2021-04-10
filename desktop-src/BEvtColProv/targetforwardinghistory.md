---
description: El historial reciente de cambios en los datos de reenvío para un equipo de destino.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: Clase TargetForwardingHistory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153573"
---
# <a name="targetforwardinghistory-class"></a><span data-ttu-id="585dd-103">Clase TargetForwardingHistory</span><span class="sxs-lookup"><span data-stu-id="585dd-103">TargetForwardingHistory class</span></span>

<span data-ttu-id="585dd-104">El historial reciente de cambios en los datos de reenvío para un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="585dd-104">The recent history of changes to the forwarding data for a target computer.</span></span>

<span data-ttu-id="585dd-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="585dd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="585dd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="585dd-106">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a><span data-ttu-id="585dd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="585dd-107">Members</span></span>

<span data-ttu-id="585dd-108">La clase **TargetForwardingHistory** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="585dd-108">The **TargetForwardingHistory** class has these types of members:</span></span>

-   [<span data-ttu-id="585dd-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="585dd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="585dd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="585dd-110">Properties</span></span>

<span data-ttu-id="585dd-111">La clase **TargetForwardingHistory** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="585dd-111">The **TargetForwardingHistory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="585dd-112">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="585dd-112">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="585dd-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-115">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-115">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-116">La información del punto de conexión del servidor del recopilador.</span><span class="sxs-lookup"><span data-stu-id="585dd-116">The endpoint information of the collector server.</span></span> <span data-ttu-id="585dd-117">Esta propiedad tiene el formato de cadena *host*:*Puerto* .</span><span class="sxs-lookup"><span data-stu-id="585dd-117">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-118">**Equipo**</span><span class="sxs-lookup"><span data-stu-id="585dd-118">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="585dd-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-121">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-121">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-122">El nombre de equipo del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="585dd-122">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-123">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="585dd-123">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-124">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="585dd-124">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-126">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-126">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-127">Marca de tiempo que indica cuándo se estableció la conexión para los datos de reenvío.</span><span class="sxs-lookup"><span data-stu-id="585dd-127">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-128">**Destino**</span><span class="sxs-lookup"><span data-stu-id="585dd-128">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="585dd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-131">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-131">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-132">El destino de los datos de reenvío, como un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="585dd-132">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-133">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="585dd-133">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="585dd-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-136">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-136">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-137">Formato utilizado para generar el destino de los datos de reenvío.</span><span class="sxs-lookup"><span data-stu-id="585dd-137">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-138">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="585dd-138">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-139">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="585dd-139">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-141">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-141">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-142">Marca de tiempo que indica cuándo se desconectó la conexión.</span><span class="sxs-lookup"><span data-stu-id="585dd-142">The timestamp that indicates when the connection was disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-143">**Error**</span><span class="sxs-lookup"><span data-stu-id="585dd-143">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="585dd-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-146">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-146">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-147">Un mensaje de error que describe un error encontrado.</span><span class="sxs-lookup"><span data-stu-id="585dd-147">An error message that describes an encountered error.</span></span> <span data-ttu-id="585dd-148">Esta propiedad está vacía si no se encuentra ningún error.</span><span class="sxs-lookup"><span data-stu-id="585dd-148">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-149">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="585dd-149">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="585dd-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-152">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-153">El tipo de archivo que contiene los datos de reenvío, como ETL.</span><span class="sxs-lookup"><span data-stu-id="585dd-153">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-154">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="585dd-154">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="585dd-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-157">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-158">La información del punto de conexión del equipo de destino, en formato legible.</span><span class="sxs-lookup"><span data-stu-id="585dd-158">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="585dd-159">Esta propiedad tiene el formato de cadena *host*:*Puerto* .</span><span class="sxs-lookup"><span data-stu-id="585dd-159">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="585dd-160">Por ejemplo, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="585dd-160">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="585dd-161">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="585dd-161">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="585dd-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-164">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-165">**GUID** de SMBIOS del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="585dd-165">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-166">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="585dd-166">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="585dd-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-169">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-169">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-170">Dirección MAC del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="585dd-170">The MAC address of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="585dd-171">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="585dd-171">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="585dd-172">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="585dd-172">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="585dd-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="585dd-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="585dd-174">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="585dd-174">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="585dd-175">Marca de tiempo de Cuándo se registró este cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="585dd-175">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="585dd-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="585dd-176">Requirements</span></span>



| <span data-ttu-id="585dd-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="585dd-177">Requirement</span></span> | <span data-ttu-id="585dd-178">Value</span><span class="sxs-lookup"><span data-stu-id="585dd-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="585dd-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="585dd-179">Minimum supported client</span></span><br/> | <span data-ttu-id="585dd-180">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="585dd-180">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="585dd-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="585dd-181">Minimum supported server</span></span><br/> | <span data-ttu-id="585dd-182">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="585dd-182">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="585dd-183">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="585dd-183">Namespace</span></span><br/>                | <span data-ttu-id="585dd-184">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="585dd-184">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="585dd-185">MOF</span><span class="sxs-lookup"><span data-stu-id="585dd-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="585dd-186"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="585dd-186"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="585dd-187">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="585dd-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="585dd-188"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="585dd-188"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="585dd-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="585dd-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="585dd-190">Proveedor WMI del recopilador de eventos de arranque</span><span class="sxs-lookup"><span data-stu-id="585dd-190">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

