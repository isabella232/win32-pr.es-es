---
description: Recupera los datos de reenvío de un equipo de destino.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: Clase TargetForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: aba0a40ccd5611cecfe7450e518620d4d41ec1e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538332"
---
# <a name="targetforwarding-class"></a><span data-ttu-id="e6024-103">Clase TargetForwarding</span><span class="sxs-lookup"><span data-stu-id="e6024-103">TargetForwarding class</span></span>

<span data-ttu-id="e6024-104">Recupera los datos de reenvío de un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="e6024-104">Retrieves forwarding data from a target computer.</span></span>

> [!Note]  
> <span data-ttu-id="e6024-105">Un equipo de destino puede tener varios reenviadores configurados.</span><span class="sxs-lookup"><span data-stu-id="e6024-105">A target computer may have multiple forwarders configured.</span></span>

 

<span data-ttu-id="e6024-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e6024-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6024-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6024-107">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
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
};
```

## <a name="members"></a><span data-ttu-id="e6024-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e6024-108">Members</span></span>

<span data-ttu-id="e6024-109">La clase **TargetForwarding** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e6024-109">The **TargetForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="e6024-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6024-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6024-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6024-111">Properties</span></span>

<span data-ttu-id="e6024-112">La clase **TargetForwarding** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e6024-112">The **TargetForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6024-113">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="e6024-113">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6024-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-116">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-116">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-117">La información del punto de conexión del servidor del recopilador.</span><span class="sxs-lookup"><span data-stu-id="e6024-117">The endpoint information of the collector server.</span></span> <span data-ttu-id="e6024-118">Esta propiedad tiene el formato de cadena *host*:*Puerto* .</span><span class="sxs-lookup"><span data-stu-id="e6024-118">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="e6024-119">**Equipo**</span><span class="sxs-lookup"><span data-stu-id="e6024-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6024-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-122">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-123">El nombre de equipo del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="e6024-123">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="e6024-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="e6024-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-125">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6024-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-127">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-128">Marca de tiempo que indica cuándo se estableció la conexión para los datos de reenvío.</span><span class="sxs-lookup"><span data-stu-id="e6024-128">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="e6024-129">**Destino**</span><span class="sxs-lookup"><span data-stu-id="e6024-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6024-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-132">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-132">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-133">El destino de los datos de reenvío, como un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="e6024-133">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="e6024-134">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="e6024-134">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6024-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-137">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-137">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-138">Formato utilizado para generar el destino de los datos de reenvío.</span><span class="sxs-lookup"><span data-stu-id="e6024-138">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="e6024-139">**Error**</span><span class="sxs-lookup"><span data-stu-id="e6024-139">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6024-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-142">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-143">Un mensaje de error que describe un error encontrado.</span><span class="sxs-lookup"><span data-stu-id="e6024-143">An error message that describes an encountered error.</span></span> <span data-ttu-id="e6024-144">Esta propiedad está vacía si no se encuentra ningún error.</span><span class="sxs-lookup"><span data-stu-id="e6024-144">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="e6024-145">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="e6024-145">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6024-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-148">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-148">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-149">El tipo de archivo que contiene los datos de reenvío, como ETL.</span><span class="sxs-lookup"><span data-stu-id="e6024-149">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="e6024-150">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="e6024-150">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6024-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-153">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-154">La información del punto de conexión del equipo de destino, en formato legible.</span><span class="sxs-lookup"><span data-stu-id="e6024-154">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="e6024-155">Esta propiedad tiene el formato de cadena *host*:*Puerto* .</span><span class="sxs-lookup"><span data-stu-id="e6024-155">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="e6024-156">Por ejemplo, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="e6024-156">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="e6024-157">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="e6024-157">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6024-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-160">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-160">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-161">**GUID** de SMBIOS del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="e6024-161">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="e6024-162">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="e6024-162">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6024-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6024-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6024-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6024-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6024-165">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e6024-165">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e6024-166">Dirección MAC del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="e6024-166">The MAC address of the target computer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6024-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6024-167">Requirements</span></span>



| <span data-ttu-id="e6024-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6024-168">Requirement</span></span> | <span data-ttu-id="e6024-169">Value</span><span class="sxs-lookup"><span data-stu-id="e6024-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6024-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6024-170">Minimum supported client</span></span><br/> | <span data-ttu-id="e6024-171">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e6024-171">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="e6024-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6024-172">Minimum supported server</span></span><br/> | <span data-ttu-id="e6024-173">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e6024-173">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="e6024-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e6024-174">Namespace</span></span><br/>                | <span data-ttu-id="e6024-175">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="e6024-175">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="e6024-176">MOF</span><span class="sxs-lookup"><span data-stu-id="e6024-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6024-177"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6024-177"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6024-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e6024-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6024-179"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6024-179"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e6024-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6024-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6024-181">Proveedor WMI del recopilador de eventos de arranque</span><span class="sxs-lookup"><span data-stu-id="e6024-181">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

