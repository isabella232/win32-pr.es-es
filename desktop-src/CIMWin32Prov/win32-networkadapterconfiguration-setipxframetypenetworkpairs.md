---
description: Establece los pares/número de red IPX (intercambio de paquetes de interredes) para este adaptador de red.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Método SetIPXFrameTypeNetworkPairs de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153423"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="33ce1-103">Método SetIPXFrameTypeNetworkPairs de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="33ce1-103">SetIPXFrameTypeNetworkPairs method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="33ce1-104">Establece los pares/número de red IPX (intercambio de paquetes de interredes) para este adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="33ce1-104">Sets the Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span>

<span data-ttu-id="33ce1-105">Windows 2000 y Windows NT 3,51 y versiones posteriores usan un número de red IPX para fines de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="33ce1-105">Windows 2000 and Windows NT 3.51 and higher use an IPX network number for routing purposes.</span></span> <span data-ttu-id="33ce1-106">Se asigna a cada combinación de adaptador de red o tipo de marco configurado en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="33ce1-106">It is assigned to each configured frame type/network adapter combination on your computer system.</span></span> <span data-ttu-id="33ce1-107">Este número se denomina a veces "número de red externa".</span><span class="sxs-lookup"><span data-stu-id="33ce1-107">This number is sometimes referred to as the "external network number."</span></span> <span data-ttu-id="33ce1-108">Debe ser único para cada segmento de red.</span><span class="sxs-lookup"><span data-stu-id="33ce1-108">It must be unique for each network segment.</span></span> <span data-ttu-id="33ce1-109">Si el tipo de marco se establece en automático, el número de red debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="33ce1-109">If the frame type is set to AUTO, the network number should to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ce1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33ce1-110">Syntax</span></span>


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a><span data-ttu-id="33ce1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33ce1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ce1-112">*IPXNetworkNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33ce1-112">*IPXNetworkNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33ce1-113">Matriz de caracteres que identifica de forma única un adaptador en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="33ce1-113">An array of characters that uniquely identify an adapter on the computer system.</span></span> <span data-ttu-id="33ce1-114">El transporte compatible con IPX/SPX de NetWare Link (NWLink) en Windows 2000 y Windows NT 3,51 o superior usa dos tipos diferentes de números de red.</span><span class="sxs-lookup"><span data-stu-id="33ce1-114">The NetWare Link (NWLink) IPX/SPX-compatible transport in Windows 2000 and Windows NT 3.51 or higher, uses two different types of network numbers.</span></span> <span data-ttu-id="33ce1-115">Este número se conoce a veces como el número de red externa.</span><span class="sxs-lookup"><span data-stu-id="33ce1-115">This number is sometimes referred to as the External Network Number.</span></span> <span data-ttu-id="33ce1-116">Debe ser único para cada segmento de red.</span><span class="sxs-lookup"><span data-stu-id="33ce1-116">It must be unique for each network segment.</span></span> <span data-ttu-id="33ce1-117">Los valores de esta lista de cadenas deben tener un valor correspondiente en el parámetro IPXFrameType que identifica el tipo de marco de paquetes que se usa para esta red.</span><span class="sxs-lookup"><span data-stu-id="33ce1-117">The values in this string list must have a corresponding value in the IPXFrameType parameter identifying the packet frame type used for this network.</span></span>

</dd> <dt>

<span data-ttu-id="33ce1-118">*IPXFrameType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33ce1-118">*IPXFrameType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33ce1-119">Matriz de enteros de los identificadores de tipo de marco.</span><span class="sxs-lookup"><span data-stu-id="33ce1-119">An integer array of frame type identifiers.</span></span> <span data-ttu-id="33ce1-120">Los valores de esta matriz se corresponden con los elementos del parámetro *IPXNetworkNumber* .</span><span class="sxs-lookup"><span data-stu-id="33ce1-120">The values in this array correspond to the elements in the *IPXNetworkNumber* parameter.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="33ce1-121">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="33ce1-121">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="33ce1-122">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="33ce1-122">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="33ce1-123">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="33ce1-123">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="33ce1-124">**Ajuste Ethernet** (3)</span><span class="sxs-lookup"><span data-stu-id="33ce1-124">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="33ce1-125">**Auto** (255)</span><span class="sxs-lookup"><span data-stu-id="33ce1-125">**AUTO** (255)</span></span>


<span data-ttu-id="33ce1-126"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="33ce1-126"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="33ce1-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33ce1-127">Return value</span></span>

<dl> <dt>

<span data-ttu-id="33ce1-128">**Finalización correcta, no es necesario reiniciar** (0)</span><span class="sxs-lookup"><span data-stu-id="33ce1-128">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-129">**Finalización correcta, se requiere un reinicio** (1)</span><span class="sxs-lookup"><span data-stu-id="33ce1-129">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-130">**Método no admitido en esta plataforma** (64)</span><span class="sxs-lookup"><span data-stu-id="33ce1-130">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-131">**Error desconocido** (65)</span><span class="sxs-lookup"><span data-stu-id="33ce1-131">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-132">**Máscara de subred no válida** (66)</span><span class="sxs-lookup"><span data-stu-id="33ce1-132">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-133">**Se produjo un error al procesar una instancia devuelta** (67)</span><span class="sxs-lookup"><span data-stu-id="33ce1-133">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-134">**Parámetro de entrada no válido** (68)</span><span class="sxs-lookup"><span data-stu-id="33ce1-134">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-135">Se **especificaron más de 5 puertas de enlace** (69)</span><span class="sxs-lookup"><span data-stu-id="33ce1-135">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-136">**Dirección IP no válida** (70)</span><span class="sxs-lookup"><span data-stu-id="33ce1-136">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-137">**Dirección IP de puerta de enlace no válida** (71)</span><span class="sxs-lookup"><span data-stu-id="33ce1-137">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-138">**Se produjo un error al obtener acceso al registro para obtener la información solicitada** (72)</span><span class="sxs-lookup"><span data-stu-id="33ce1-138">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-139">**Nombre de dominio no válido** (73)</span><span class="sxs-lookup"><span data-stu-id="33ce1-139">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-140">**Nombre de host no válido** (74)</span><span class="sxs-lookup"><span data-stu-id="33ce1-140">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-141">**No se definió ningún servidor WINS principal/secundario** (75)</span><span class="sxs-lookup"><span data-stu-id="33ce1-141">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-142">**Archivo no válido** (76)</span><span class="sxs-lookup"><span data-stu-id="33ce1-142">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-143">**Ruta de acceso del sistema no válida** (77)</span><span class="sxs-lookup"><span data-stu-id="33ce1-143">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-144">**No se pudo copiar el archivo** (78)</span><span class="sxs-lookup"><span data-stu-id="33ce1-144">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-145">**Parámetro de seguridad no válido** (79)</span><span class="sxs-lookup"><span data-stu-id="33ce1-145">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-146">**No se puede configurar el servicio TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="33ce1-146">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-147">**No se puede configurar el servicio DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="33ce1-147">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-148">**No se puede renovar la concesión DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="33ce1-148">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-149">**No se puede liberar la concesión DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="33ce1-149">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-150">**IP no habilitada en el adaptador** (84)</span><span class="sxs-lookup"><span data-stu-id="33ce1-150">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-151">**IPX no habilitado en el adaptador** (85)</span><span class="sxs-lookup"><span data-stu-id="33ce1-151">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-152">**Error de límite de número de trama/red** (86)</span><span class="sxs-lookup"><span data-stu-id="33ce1-152">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-153">**Tipo de marco no válido** (87)</span><span class="sxs-lookup"><span data-stu-id="33ce1-153">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-154">**Número de red no válido** (88)</span><span class="sxs-lookup"><span data-stu-id="33ce1-154">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-155">**Número de red duplicada** (89)</span><span class="sxs-lookup"><span data-stu-id="33ce1-155">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-156">**Parámetro fuera de los límites** (90)</span><span class="sxs-lookup"><span data-stu-id="33ce1-156">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-157">**Acceso denegado** (91)</span><span class="sxs-lookup"><span data-stu-id="33ce1-157">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-158">**Memoria insuficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="33ce1-158">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-159">**Ya existe** (93)</span><span class="sxs-lookup"><span data-stu-id="33ce1-159">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-160">**Ruta de acceso, archivo u objeto no encontrado** (94)</span><span class="sxs-lookup"><span data-stu-id="33ce1-160">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-161">**No se puede notificar al servicio** (95)</span><span class="sxs-lookup"><span data-stu-id="33ce1-161">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-162">**No se puede notificar al servicio DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="33ce1-162">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-163">**Interfaz no configurable** (97)</span><span class="sxs-lookup"><span data-stu-id="33ce1-163">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-164">**No todas las concesiones DHCP se pueden liberar o renovar** (98)</span><span class="sxs-lookup"><span data-stu-id="33ce1-164">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-165">**DHCP no está habilitado en el adaptador** (100)</span><span class="sxs-lookup"><span data-stu-id="33ce1-165">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="33ce1-166">**Otro** (101 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="33ce1-166">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="33ce1-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33ce1-167">Requirements</span></span>



| <span data-ttu-id="33ce1-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ce1-168">Requirement</span></span> | <span data-ttu-id="33ce1-169">Value</span><span class="sxs-lookup"><span data-stu-id="33ce1-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33ce1-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33ce1-170">Minimum supported client</span></span><br/> | <span data-ttu-id="33ce1-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33ce1-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33ce1-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33ce1-172">Minimum supported server</span></span><br/> | <span data-ttu-id="33ce1-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33ce1-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33ce1-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="33ce1-174">Namespace</span></span><br/>                | <span data-ttu-id="33ce1-175">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="33ce1-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33ce1-176">MOF</span><span class="sxs-lookup"><span data-stu-id="33ce1-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33ce1-177"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33ce1-177"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33ce1-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="33ce1-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33ce1-179"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33ce1-179"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ce1-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="33ce1-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ce1-181">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="33ce1-181">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




