---
description: Las características de administración de un dispositivo USB.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: CIM_USBDevice (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4b43c57d69f0f9eb92293aa8fa1ff1aa1ebe96c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687347"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="76fe2-103">CIM_USBDevice (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="76fe2-103">CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="76fe2-104">Las características de administración de un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="76fe2-104">The management characteristics of a USB device.</span></span>

## <a name="syntax"></a><span data-ttu-id="76fe2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76fe2-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a><span data-ttu-id="76fe2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="76fe2-106">Members</span></span>

<span data-ttu-id="76fe2-107">La clase **CIM \_ USBDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="76fe2-107">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="76fe2-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="76fe2-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="76fe2-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="76fe2-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="76fe2-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="76fe2-110">Methods</span></span>

<span data-ttu-id="76fe2-111">La clase **CIM \_ USBDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="76fe2-111">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="76fe2-112">Método</span><span class="sxs-lookup"><span data-stu-id="76fe2-112">Method</span></span>                                               | <span data-ttu-id="76fe2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="76fe2-113">Description</span></span>                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [<span data-ttu-id="76fe2-114">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="76fe2-114">**GetDescriptor**</span></span>](cim-usbdevice-getdescriptor.md) | <span data-ttu-id="76fe2-115">Recupera un descriptor de dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="76fe2-115">Retrieves a USB device descriptor.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="76fe2-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="76fe2-116">Properties</span></span>

<span data-ttu-id="76fe2-117">La clase **CIM \_ USBDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="76fe2-117">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76fe2-118">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="76fe2-118">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-119">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="76fe2-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-121">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bDeviceClass")</span><span class="sxs-lookup"><span data-stu-id="76fe2-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceClass")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-122">Código de la clase USB.</span><span class="sxs-lookup"><span data-stu-id="76fe2-122">The USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-123">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="76fe2-123">**CommandTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-124">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="76fe2-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-126">Un intervalo de tiempo de espera que pueden configurarse las aplicaciones de administración que admiten el redireccionamiento USB.</span><span class="sxs-lookup"><span data-stu-id="76fe2-126">A timeout interval that is configurable by management applications that support USB redirection.</span></span> <span data-ttu-id="76fe2-127">Cuando el servicio de redirección redirige un comando de dispositivo USB a un dispositivo remoto, y el dispositivo remoto no responde antes del intervalo de tiempo de espera, el servicio de redireccionamiento emulará un evento de expulsión de medios.</span><span class="sxs-lookup"><span data-stu-id="76fe2-127">When the redirection service redirects a USB device command to a remote device, and the remote device does not respond before timeout interval, the redirection service will emulate a media eject event.</span></span> <span data-ttu-id="76fe2-128">Además, el servicio puede volver a intentar el comando o intentar volver a establecer la conexión con el dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="76fe2-128">In addition, the service may re-try the command or try to re-establish the connection to the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-129">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="76fe2-129">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-130">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="76fe2-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-132">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="76fe2-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-133">Una matriz que contiene la configuración alternativa para cada interfaz en la configuración actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76fe2-133">An array that contains the alternate settings for each interface in the current configuration of the device.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-134">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="76fe2-134">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-135">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="76fe2-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-137">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="76fe2-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-138">La configuración seleccionada actualmente para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76fe2-138">The configuration currently selected for the device.</span></span> <span data-ttu-id="76fe2-139">Si este valor es cero, el dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="76fe2-139">If this value is zero, the Device is not configured.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-140">**DeviceReleaseNumber**</span><span class="sxs-lookup"><span data-stu-id="76fe2-140">**DeviceReleaseNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-141">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76fe2-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-143">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bcdDevice")</span><span class="sxs-lookup"><span data-stu-id="76fe2-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdDevice")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-144">El número de versión del dispositivo en formato BCD.</span><span class="sxs-lookup"><span data-stu-id="76fe2-144">The device release number in BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-145">**Le**</span><span class="sxs-lookup"><span data-stu-id="76fe2-145">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="76fe2-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| iManufacturer")</span><span class="sxs-lookup"><span data-stu-id="76fe2-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iManufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-149">Cadena del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76fe2-149">The manufacturer string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-150">**MaxPacketSize**</span><span class="sxs-lookup"><span data-stu-id="76fe2-150">**MaxPacketSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-151">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="76fe2-151">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-153">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bMaxPacketSize")</span><span class="sxs-lookup"><span data-stu-id="76fe2-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bMaxPacketSize")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-154">El tamaño máximo del paquete para el extremo de cero USB.</span><span class="sxs-lookup"><span data-stu-id="76fe2-154">The maximum packet size for the USB zero endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-155">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="76fe2-155">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-156">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="76fe2-156">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-158">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bNumConfigurations")</span><span class="sxs-lookup"><span data-stu-id="76fe2-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bNumConfigurations")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-159">El número de configuraciones de dispositivo definidas para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76fe2-159">The number of device configurations that are defined for the Device.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-160">**Producto**</span><span class="sxs-lookup"><span data-stu-id="76fe2-160">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="76fe2-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-163">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| iProduct")</span><span class="sxs-lookup"><span data-stu-id="76fe2-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iProduct")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-164">Cadena de producto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76fe2-164">The product string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-165">**ProductID**</span><span class="sxs-lookup"><span data-stu-id="76fe2-165">**ProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-166">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76fe2-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-168">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| idProduct")</span><span class="sxs-lookup"><span data-stu-id="76fe2-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idProduct")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-169">El ID. de producto asignado al dispositivo por fabricante.</span><span class="sxs-lookup"><span data-stu-id="76fe2-169">The product ID assigned to the device by manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-170">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="76fe2-170">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-171">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="76fe2-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-173">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bDeviceProtocol")</span><span class="sxs-lookup"><span data-stu-id="76fe2-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-174">Código del protocolo USB.</span><span class="sxs-lookup"><span data-stu-id="76fe2-174">The USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-175">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="76fe2-175">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="76fe2-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-178">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| iSerialNumber")</span><span class="sxs-lookup"><span data-stu-id="76fe2-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iSerialNumber")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-179">El número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76fe2-179">The serial number of the device.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-180">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="76fe2-180">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-181">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="76fe2-181">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-183">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bDeviceSubClass")</span><span class="sxs-lookup"><span data-stu-id="76fe2-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceSubClass")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-184">Código de la subclase USB.</span><span class="sxs-lookup"><span data-stu-id="76fe2-184">The USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-185">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="76fe2-185">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-186">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76fe2-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-188">La versión USB más reciente compatible con el dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="76fe2-188">The latest USB Version supported by the USB Device.</span></span> <span data-ttu-id="76fe2-189">La propiedad se expresa como un decimal con codificación binaria (BCD) que contiene un separador decimal entre el segundo y el tercer dígito.</span><span class="sxs-lookup"><span data-stu-id="76fe2-189">The property is expressed as a binary-coded decimal (BCD) that contains a decimal point between the 2nd and 3rd digits.</span></span> <span data-ttu-id="76fe2-190">Por ejemplo, un valor de 0x201 indica que se admite la versión 2,01.</span><span class="sxs-lookup"><span data-stu-id="76fe2-190">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-191">**USBVersionInBCD**</span><span class="sxs-lookup"><span data-stu-id="76fe2-191">**USBVersionInBCD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-192">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76fe2-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-194">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| bcdUSB")</span><span class="sxs-lookup"><span data-stu-id="76fe2-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdUSB")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-195">El número de especificación USB que el dispositivo cumple.</span><span class="sxs-lookup"><span data-stu-id="76fe2-195">The USB specification number that the device complies with.</span></span> <span data-ttu-id="76fe2-196">Esta propiedad tiene el formato BCD.</span><span class="sxs-lookup"><span data-stu-id="76fe2-196">This property is formatted with BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="76fe2-197">**VendorID**</span><span class="sxs-lookup"><span data-stu-id="76fe2-197">**VendorID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76fe2-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76fe2-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="76fe2-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76fe2-200">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Especificación de bus serie universal. USB-si el \| descriptor de dispositivo estándar \| idVendor")</span><span class="sxs-lookup"><span data-stu-id="76fe2-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idVendor")</span></span>
</dt> </dl>

<span data-ttu-id="76fe2-201">El identificador de proveedor asignado al dispositivo por USB.org.</span><span class="sxs-lookup"><span data-stu-id="76fe2-201">The vendor ID assigned to the device by USB.org.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76fe2-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76fe2-202">Requirements</span></span>



| <span data-ttu-id="76fe2-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="76fe2-203">Requirement</span></span> | <span data-ttu-id="76fe2-204">Value</span><span class="sxs-lookup"><span data-stu-id="76fe2-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76fe2-205">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76fe2-205">Minimum supported client</span></span><br/> | <span data-ttu-id="76fe2-206">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="76fe2-206">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="76fe2-207">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76fe2-207">Minimum supported server</span></span><br/> | <span data-ttu-id="76fe2-208">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="76fe2-208">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="76fe2-209">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="76fe2-209">Namespace</span></span><br/>                | <span data-ttu-id="76fe2-210">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="76fe2-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="76fe2-211">MOF</span><span class="sxs-lookup"><span data-stu-id="76fe2-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76fe2-212"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76fe2-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76fe2-213">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="76fe2-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76fe2-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76fe2-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76fe2-215">Vea también</span><span class="sxs-lookup"><span data-stu-id="76fe2-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fe2-216">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="76fe2-216">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

