---
description: Destinos conocidos que contienen los datos recopilados. Solo está disponible si el recopilador se está ejecutando con el registro de estado habilitado.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Clase TargetForwardingDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495850"
---
# <a name="targetforwardingdestination-class"></a><span data-ttu-id="1f5ad-104">Clase TargetForwardingDestination</span><span class="sxs-lookup"><span data-stu-id="1f5ad-104">TargetForwardingDestination class</span></span>

<span data-ttu-id="1f5ad-105">Destinos conocidos que contienen los datos recopilados.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-105">The known destinations containing the collected data.</span></span> <span data-ttu-id="1f5ad-106">Solo está disponible si el recopilador se está ejecutando con el registro de estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-106">Available only if the collector is running with the status log enabled.</span></span>

<span data-ttu-id="1f5ad-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f5ad-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f5ad-108">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
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

## <a name="members"></a><span data-ttu-id="1f5ad-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1f5ad-109">Members</span></span>

<span data-ttu-id="1f5ad-110">La clase **TargetForwardingDestination** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1f5ad-110">The **TargetForwardingDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="1f5ad-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1f5ad-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f5ad-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1f5ad-112">Properties</span></span>

<span data-ttu-id="1f5ad-113">La clase **TargetForwardingDestination** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-113">The **TargetForwardingDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f5ad-114">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-114">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-117">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-117">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-118">La información de host: Puerto del punto de conexión en el lado del recopilador.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-118">The host:port information of the endpoint on the collector side.</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-119">**Equipo**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-122">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-123">Nombre del equipo de destino, determinado por el recopilador según su configuración.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-123">Target computer name, as determined by the collector according to its configuration.</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-125">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-127">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-128">Marca de tiempo de cuando se estableció la conexión.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-128">Timestamp of when the connection was established.</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-129">**Destino**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-132">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-133">Destino de los datos.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-133">Destination of the data.</span></span> <span data-ttu-id="1f5ad-134">El significado depende del tipo de reenviador.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-134">The meaning depends on the forwarder type.</span></span> <span data-ttu-id="1f5ad-135">Puede ser un nombre de archivo u otra identificación.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-135">May be a file name or some other identification.</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-136">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-136">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-139">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-139">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-140">Patrón utilizado para generar el destino de los datos.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-140">Pattern used to generate the destination of the data.</span></span> <span data-ttu-id="1f5ad-141">El significado depende del tipo y la configuración del reenviador.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-141">The meaning depends on the forwarder type and configuration.</span></span> <span data-ttu-id="1f5ad-142">Para un destino fijo, sería el mismo que el propio destino.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-142">For a fixed destination, would be the same as the destination itself.</span></span> <span data-ttu-id="1f5ad-143">Para el destino con rotación de los archivos, contendría los caracteres de patrón que se reemplazarán por el índice real en el destino.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-143">For the destination with rotation of the files would contain the pattern characters that will be replaced with the actual index in the destination.</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-144">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-144">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-145">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-147">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-147">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-148">Marca de tiempo de cuando se quitó la conexión.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-148">Timestamp of when the connection was dropped.</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-149">**Error**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-149">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-152">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-153">Mensaje de error si se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-153">Error message if an error was encountered.</span></span> <span data-ttu-id="1f5ad-154">De lo contrario, estará vacío.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-154">Otherwise will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-155">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-155">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-158">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-159">Tipo del reenviador (por ejemplo, ' ETL ').</span><span class="sxs-lookup"><span data-stu-id="1f5ad-159">Type of the forwarder (such as 'etl').</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-160">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-160">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-163">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-163">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-164">La información del punto de conexión del equipo de destino, en formato legible.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-164">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="1f5ad-165">Esta propiedad tiene el formato de cadena *host*:*Puerto* .</span><span class="sxs-lookup"><span data-stu-id="1f5ad-165">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="1f5ad-166">Por ejemplo, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="1f5ad-166">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-167">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-167">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-170">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-170">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-171">GUID de SMBIOS del equipo de destino (si se conoce).</span><span class="sxs-lookup"><span data-stu-id="1f5ad-171">The target computer's SMBIOS GUID (if known).</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-172">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-172">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-175">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-175">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-176">Dirección MAC del equipo de destino (si se conoce).</span><span class="sxs-lookup"><span data-stu-id="1f5ad-176">The target computer's MAC address (if known).</span></span>

</dd> <dt>

<span data-ttu-id="1f5ad-177">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-177">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f5ad-178">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1f5ad-178">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1f5ad-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f5ad-180">Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f5ad-180">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f5ad-181">Marca de tiempo de Cuándo se registró este cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="1f5ad-181">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f5ad-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f5ad-182">Requirements</span></span>



| <span data-ttu-id="1f5ad-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f5ad-183">Requirement</span></span> | <span data-ttu-id="1f5ad-184">Value</span><span class="sxs-lookup"><span data-stu-id="1f5ad-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f5ad-185">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f5ad-185">Minimum supported client</span></span><br/> | <span data-ttu-id="1f5ad-186">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1f5ad-186">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="1f5ad-187">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f5ad-187">Minimum supported server</span></span><br/> | <span data-ttu-id="1f5ad-188">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1f5ad-188">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="1f5ad-189">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1f5ad-189">Namespace</span></span><br/>                | <span data-ttu-id="1f5ad-190">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="1f5ad-190">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="1f5ad-191">MOF</span><span class="sxs-lookup"><span data-stu-id="1f5ad-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f5ad-192"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f5ad-192"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f5ad-193">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f5ad-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f5ad-194"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f5ad-194"><dt>BEvtCol.exe</dt></span></span> </dl>               |



 

