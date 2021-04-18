---
description: Win32 \_ TCPIPPrinterPort&\# 32; La clase WMI representa un punto de acceso al servicio TCP/IP.
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Win32_TCPIPPrinterPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a0b0f0cb73cc60ff117399a636b0ab8542fac6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652348"
---
# <a name="win32_tcpipprinterport-class"></a><span data-ttu-id="a989c-103">\_Clase Win32 TCPIPPrinterPort</span><span class="sxs-lookup"><span data-stu-id="a989c-103">Win32\_TCPIPPrinterPort class</span></span>

<span data-ttu-id="a989c-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ TCPIPPrinterPort de Win32** representa un punto de acceso al servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a989c-104">The **Win32\_TCPIPPrinterPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a TCP/IP service access point.</span></span>

<span data-ttu-id="a989c-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a989c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a989c-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a989c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a989c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a989c-107">Syntax</span></span>

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a><span data-ttu-id="a989c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a989c-108">Members</span></span>

<span data-ttu-id="a989c-109">La **clase \_ TCPIPPrinterPort de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a989c-109">The **Win32\_TCPIPPrinterPort** class has these types of members:</span></span>

-   [<span data-ttu-id="a989c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a989c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a989c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a989c-111">Properties</span></span>

<span data-ttu-id="a989c-112">La **clase \_ TCPIPPrinterPort de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a989c-112">The **Win32\_TCPIPPrinterPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a989c-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="a989c-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-114">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a989c-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a989c-116">Si **es true**, el equipo cuenta los bytes de un documento antes de enviarlos a la impresora y la impresora devuelve el número de bytes leídos realmente.</span><span class="sxs-lookup"><span data-stu-id="a989c-116">If **TRUE**, the computer counts the bytes in a document before sending them to the printer and the printer reports back the number of bytes actually read.</span></span> <span data-ttu-id="a989c-117">Esta capacidad se usa para el diagnóstico cuando se detectan bytes que faltan en la salida de impresión.</span><span class="sxs-lookup"><span data-stu-id="a989c-117">This capability is used for diagnostics when missing bytes are detected in the print output.</span></span>

</dd> <dt>

<span data-ttu-id="a989c-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a989c-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a989c-121">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a989c-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a989c-122">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a989c-122">A short textual description of the object.</span></span>

<span data-ttu-id="a989c-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a989c-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a989c-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a989c-127">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="a989c-127">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a989c-128">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="a989c-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a989c-129">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="a989c-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a989c-130">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-130">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="a989c-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a989c-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a989c-134">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="a989c-134">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a989c-135">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a989c-135">A textual description of the object.</span></span>

<span data-ttu-id="a989c-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a989c-137">**HostAddress**</span><span class="sxs-lookup"><span data-stu-id="a989c-137">**HostAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a989c-140">Dirección del dispositivo o servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="a989c-140">Address of the device or print server.</span></span>

</dd> <dt>

<span data-ttu-id="a989c-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a989c-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-142">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a989c-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a989c-144">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="a989c-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a989c-145">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a989c-145">Indicates when the object was installed.</span></span> <span data-ttu-id="a989c-146">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="a989c-146">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a989c-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a989c-148">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a989c-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a989c-151">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="a989c-151">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a989c-152">Identifica de forma única el punto de acceso al servicio y proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="a989c-152">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="a989c-153">Esta funcionalidad se describe con más detalle en la propiedad Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a989c-153">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="a989c-154">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-154">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="a989c-155">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="a989c-155">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-156">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a989c-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a989c-158">Número de puertos TCP utilizados por el monitor de puerto para comunicarse con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a989c-158">Number of the TCP ports used by the port monitor to communicate with the device.</span></span>

</dd> <dt>

<span data-ttu-id="a989c-159">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="a989c-159">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a989c-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a989c-162">Protocolo de impresión usado.</span><span class="sxs-lookup"><span data-stu-id="a989c-162">Printing protocol used.</span></span> <span data-ttu-id="a989c-163">Algunas impresoras solo admiten LPR.</span><span class="sxs-lookup"><span data-stu-id="a989c-163">Some printers support only LPR.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="a989c-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a989c-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a989c-165">RAW</span><span class="sxs-lookup"><span data-stu-id="a989c-165">RAW</span></span>

<span data-ttu-id="a989c-166">Imprimir directamente en un dispositivo o servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="a989c-166">Printing directly to a device or print server.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="a989c-167"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="a989c-167"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="a989c-168">LPR</span><span class="sxs-lookup"><span data-stu-id="a989c-168">LPR</span></span>

<span data-ttu-id="a989c-169">Protocolo heredado, que se reemplaza finalmente por RAW.</span><span class="sxs-lookup"><span data-stu-id="a989c-169">Legacy protocol, which is eventually replaced by RAW.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a989c-170">**Cola**</span><span class="sxs-lookup"><span data-stu-id="a989c-170">**Queue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a989c-173">Nombre de la cola de impresión en el servidor cuando se usa con el protocolo LPR.</span><span class="sxs-lookup"><span data-stu-id="a989c-173">Name of the print queue on the server when used with the LPR protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a989c-174">**SNMPCommunity**</span><span class="sxs-lookup"><span data-stu-id="a989c-174">**SNMPCommunity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a989c-177">Valor de nivel de seguridad para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a989c-177">Security level value for the device.</span></span>

<span data-ttu-id="a989c-178">Ejemplo: "Public" "</span><span class="sxs-lookup"><span data-stu-id="a989c-178">Example: "public'"</span></span>

</dd> <dt>

<span data-ttu-id="a989c-179">**SNMPDevIndex**</span><span class="sxs-lookup"><span data-stu-id="a989c-179">**SNMPDevIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-180">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a989c-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a989c-182">Número de índice de SNMP de este dispositivo para el agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="a989c-182">SNMP index number of this device for the SNMP agent.</span></span>

</dd> <dt>

<span data-ttu-id="a989c-183">**SNMPEnabled**</span><span class="sxs-lookup"><span data-stu-id="a989c-183">**SNMPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a989c-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a989c-186">Si **es true**, esta impresora admite [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Protocolo simple de administración de redes) y puede proporcionar información de estado enriquecida desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a989c-186">If **TRUE**, this printer supports [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) and can provide rich status information from the device.</span></span>

</dd> <dt>

<span data-ttu-id="a989c-187">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a989c-187">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a989c-190">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="a989c-190">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a989c-191">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a989c-191">String that indicates the current status of the object.</span></span> <span data-ttu-id="a989c-192">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="a989c-192">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a989c-193">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="a989c-193">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a989c-194">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="a989c-194">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a989c-195">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="a989c-195">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a989c-196">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="a989c-196">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a989c-197">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="a989c-197">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a989c-198">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a989c-199">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a989c-199">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a989c-200">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="a989c-200">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a989c-201">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="a989c-201">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a989c-202">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a989c-202">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a989c-203">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="a989c-203">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a989c-204">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a989c-204">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a989c-205">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="a989c-205">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a989c-206">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="a989c-206">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a989c-207">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="a989c-207">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a989c-208">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="a989c-208">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a989c-209">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a989c-209">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a989c-210">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="a989c-210">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a989c-211">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="a989c-211">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a989c-212">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a989c-212">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a989c-215">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="a989c-215">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a989c-216">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a989c-216">The scoping system's creation class name.</span></span>

<span data-ttu-id="a989c-217">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-217">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="a989c-218">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a989c-218">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a989c-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a989c-221">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="a989c-221">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a989c-222">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a989c-222">The scoping system's name.</span></span>

<span data-ttu-id="a989c-223">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-223">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="a989c-224">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a989c-224">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a989c-225">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a989c-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a989c-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a989c-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a989c-227">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a989c-227">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a989c-228">Tipo de SAP, como adjuntado o redirigido.</span><span class="sxs-lookup"><span data-stu-id="a989c-228">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="a989c-229">Esta propiedad se hereda de [**\_ punto CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-229">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="a989c-230">**Escritura** (1)</span><span class="sxs-lookup"><span data-stu-id="a989c-230">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="a989c-231">**Lectura** (2)</span><span class="sxs-lookup"><span data-stu-id="a989c-231">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="a989c-232">**Redirigido** (4)</span><span class="sxs-lookup"><span data-stu-id="a989c-232">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="a989c-233">**Net \_ Adjunta** (8)</span><span class="sxs-lookup"><span data-stu-id="a989c-233">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a989c-234">**desconocido** (16)</span><span class="sxs-lookup"><span data-stu-id="a989c-234">**unknown** (16)</span></span>


<span data-ttu-id="a989c-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a989c-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a989c-236">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a989c-236">Remarks</span></span>

<span data-ttu-id="a989c-237">La **clase \_ TCPIPPrinterPort de Win32** se deriva [**de \_ punto de CIM**](cim-serviceaccesspoint.md) que deriva [**de \_ CIM LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a989c-237">The **Win32\_TCPIPPrinterPort** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="a989c-238">El privilegio **SeLoadDriverPrivilege** es necesario para eliminar una instancia de esta clase WMI.</span><span class="sxs-lookup"><span data-stu-id="a989c-238">The **SeLoadDriverPrivilege** privilege is required to delete an instance of this WMI class.</span></span> <span data-ttu-id="a989c-239">El siguiente fragmento de script muestra cómo establecer una conexión a WMI que usa este privilegio.</span><span class="sxs-lookup"><span data-stu-id="a989c-239">The following script snippet demonstrates how to make a connection to WMI that uses this privilege.</span></span>

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a><span data-ttu-id="a989c-240">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a989c-240">Examples</span></span>

<span data-ttu-id="a989c-241">En el siguiente ejemplo de PowerShell se quita una impresora y el puerto de impresora TCPIP asociado.</span><span class="sxs-lookup"><span data-stu-id="a989c-241">The following PowerShell sample removes a printer and the associated TCPIP printer port.</span></span>


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a><span data-ttu-id="a989c-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a989c-242">Requirements</span></span>



| <span data-ttu-id="a989c-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="a989c-243">Requirement</span></span> | <span data-ttu-id="a989c-244">Value</span><span class="sxs-lookup"><span data-stu-id="a989c-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a989c-245">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a989c-245">Minimum supported client</span></span><br/> | <span data-ttu-id="a989c-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a989c-246">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a989c-247">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a989c-247">Minimum supported server</span></span><br/> | <span data-ttu-id="a989c-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a989c-248">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a989c-249">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a989c-249">Namespace</span></span><br/>                | <span data-ttu-id="a989c-250">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a989c-250">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="a989c-251">MOF</span><span class="sxs-lookup"><span data-stu-id="a989c-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a989c-252"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a989c-252"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="a989c-253">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a989c-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a989c-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a989c-254"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a989c-255">Vea también</span><span class="sxs-lookup"><span data-stu-id="a989c-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a989c-256">**\_Punto CIM**</span><span class="sxs-lookup"><span data-stu-id="a989c-256">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dt>

[<span data-ttu-id="a989c-257">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="a989c-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
