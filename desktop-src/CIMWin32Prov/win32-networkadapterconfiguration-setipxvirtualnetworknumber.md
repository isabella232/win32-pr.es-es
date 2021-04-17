---
description: Establece el número de red virtual de intercambio de paquetes de interredes (IPX) en el sistema del equipo de destino.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Método SetIPXVirtualNetworkNumber de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659706"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="fdd58-103">Método SetIPXVirtualNetworkNumber de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="fdd58-103">SetIPXVirtualNetworkNumber method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="fdd58-104">Establece el número de red virtual de intercambio de paquetes de interredes (IPX) en el sistema del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="fdd58-104">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span> <span data-ttu-id="fdd58-105">Windows 2000 y Windows NT 3,51 o superior usan un número de red interno para el enrutamiento interno.</span><span class="sxs-lookup"><span data-stu-id="fdd58-105">Windows 2000 and Windows NT 3.51 or greater uses an internal network number for internal routing.</span></span> <span data-ttu-id="fdd58-106">El número de red interna también se conoce como un número de red virtual.</span><span class="sxs-lookup"><span data-stu-id="fdd58-106">The internal network number is also known as a virtual network number.</span></span> <span data-ttu-id="fdd58-107">Identifica de forma única el sistema del equipo en la red.</span><span class="sxs-lookup"><span data-stu-id="fdd58-107">It uniquely identifies the computer system on the network.</span></span> <span data-ttu-id="fdd58-108">El método devuelve un valor entero que se puede interpretar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fdd58-108">The method returns an integer value that can be interpretted as follows:</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd58-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdd58-109">Syntax</span></span>


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a><span data-ttu-id="fdd58-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdd58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd58-111">*IPXVirtualNetNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdd58-111">*IPXVirtualNetNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdd58-112">Número de red virtual para este sistema.</span><span class="sxs-lookup"><span data-stu-id="fdd58-112">The virtual network number for this system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd58-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdd58-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="fdd58-114">**Finalización correcta, no es necesario reiniciar** (0)</span><span class="sxs-lookup"><span data-stu-id="fdd58-114">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-115">**Finalización correcta, se requiere un reinicio** (1)</span><span class="sxs-lookup"><span data-stu-id="fdd58-115">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-116">**Método no admitido en esta plataforma** (64)</span><span class="sxs-lookup"><span data-stu-id="fdd58-116">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-117">**Error desconocido** (65)</span><span class="sxs-lookup"><span data-stu-id="fdd58-117">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-118">**Máscara de subred no válida** (66)</span><span class="sxs-lookup"><span data-stu-id="fdd58-118">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-119">**Se produjo un error al procesar una instancia devuelta** (67)</span><span class="sxs-lookup"><span data-stu-id="fdd58-119">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-120">**Parámetro de entrada no válido** (68)</span><span class="sxs-lookup"><span data-stu-id="fdd58-120">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-121">Se **especificaron más de 5 puertas de enlace** (69)</span><span class="sxs-lookup"><span data-stu-id="fdd58-121">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-122">**Dirección IP no válida** (70)</span><span class="sxs-lookup"><span data-stu-id="fdd58-122">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-123">**Dirección IP de puerta de enlace no válida** (71)</span><span class="sxs-lookup"><span data-stu-id="fdd58-123">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-124">**Se produjo un error al obtener acceso al registro para obtener la información solicitada** (72)</span><span class="sxs-lookup"><span data-stu-id="fdd58-124">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-125">**Nombre de dominio no válido** (73)</span><span class="sxs-lookup"><span data-stu-id="fdd58-125">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-126">**Nombre de host no válido** (74)</span><span class="sxs-lookup"><span data-stu-id="fdd58-126">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-127">**No se definió ningún servidor WINS principal/secundario** (75)</span><span class="sxs-lookup"><span data-stu-id="fdd58-127">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-128">**Archivo no válido** (76)</span><span class="sxs-lookup"><span data-stu-id="fdd58-128">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-129">**Ruta de acceso del sistema no válida** (77)</span><span class="sxs-lookup"><span data-stu-id="fdd58-129">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-130">**No se pudo copiar el archivo** (78)</span><span class="sxs-lookup"><span data-stu-id="fdd58-130">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-131">**Parámetro de seguridad no válido** (79)</span><span class="sxs-lookup"><span data-stu-id="fdd58-131">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-132">**No se puede configurar el servicio TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="fdd58-132">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-133">**No se puede configurar el servicio DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="fdd58-133">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-134">**No se puede renovar la concesión DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="fdd58-134">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-135">**No se puede liberar la concesión DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="fdd58-135">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-136">**IP no habilitada en el adaptador** (84)</span><span class="sxs-lookup"><span data-stu-id="fdd58-136">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-137">**IPX no habilitado en el adaptador** (85)</span><span class="sxs-lookup"><span data-stu-id="fdd58-137">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-138">**Error de límite de número de trama/red** (86)</span><span class="sxs-lookup"><span data-stu-id="fdd58-138">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-139">**Tipo de marco no válido** (87)</span><span class="sxs-lookup"><span data-stu-id="fdd58-139">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-140">**Número de red no válido** (88)</span><span class="sxs-lookup"><span data-stu-id="fdd58-140">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-141">**Número de red duplicada** (89)</span><span class="sxs-lookup"><span data-stu-id="fdd58-141">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-142">**Parámetro fuera de los límites** (90)</span><span class="sxs-lookup"><span data-stu-id="fdd58-142">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-143">**Acceso denegado** (91)</span><span class="sxs-lookup"><span data-stu-id="fdd58-143">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-144">**Memoria insuficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="fdd58-144">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-145">**Ya existe** (93)</span><span class="sxs-lookup"><span data-stu-id="fdd58-145">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-146">**Ruta de acceso, archivo u objeto no encontrado** (94)</span><span class="sxs-lookup"><span data-stu-id="fdd58-146">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-147">**No se puede notificar al servicio** (95)</span><span class="sxs-lookup"><span data-stu-id="fdd58-147">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-148">**No se puede notificar al servicio DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="fdd58-148">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-149">**Interfaz no configurable** (97)</span><span class="sxs-lookup"><span data-stu-id="fdd58-149">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-150">**No todas las concesiones DHCP se pueden liberar o renovar** (98)</span><span class="sxs-lookup"><span data-stu-id="fdd58-150">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-151">**DHCP no está habilitado en el adaptador** (100)</span><span class="sxs-lookup"><span data-stu-id="fdd58-151">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="fdd58-152">**Otro** (101 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="fdd58-152">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fdd58-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdd58-153">Requirements</span></span>



| <span data-ttu-id="fdd58-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdd58-154">Requirement</span></span> | <span data-ttu-id="fdd58-155">Value</span><span class="sxs-lookup"><span data-stu-id="fdd58-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd58-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdd58-156">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd58-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdd58-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fdd58-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdd58-158">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd58-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdd58-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fdd58-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fdd58-160">Namespace</span></span><br/>                | <span data-ttu-id="fdd58-161">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fdd58-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fdd58-162">MOF</span><span class="sxs-lookup"><span data-stu-id="fdd58-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdd58-163"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdd58-163"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdd58-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fdd58-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdd58-165"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdd58-165"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdd58-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdd58-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd58-167">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="fdd58-167">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




