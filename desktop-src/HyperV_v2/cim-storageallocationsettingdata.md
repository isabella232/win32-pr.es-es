---
description: Representa la configuración para la asignación de almacenamiento virtual.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: Clase CIM_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e66322f20987e2d1f99042430f0f57cdc2e399d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813851"
---
# <a name="cim_storageallocationsettingdata-class"></a><span data-ttu-id="9639f-103">\_Clase StorageAllocationSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="9639f-103">CIM\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="9639f-104">Representa la configuración para la asignación de almacenamiento virtual.</span><span class="sxs-lookup"><span data-stu-id="9639f-104">Represents settings for the allocation of virtual storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="9639f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9639f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a><span data-ttu-id="9639f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9639f-106">Members</span></span>

<span data-ttu-id="9639f-107">La clase **CIM \_ StorageAllocationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9639f-107">The **CIM\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9639f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9639f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9639f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9639f-109">Properties</span></span>

<span data-ttu-id="9639f-110">La clase **CIM \_ StorageAllocationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9639f-110">The **CIM\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9639f-111">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="9639f-111">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9639f-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-114">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Acceso**")</span><span class="sxs-lookup"><span data-stu-id="9639f-114">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**Access**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-115">Compatibilidad de lectura y escritura de la asignación de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9639f-115">The read/write support of the storage allocation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9639f-116">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9639f-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="9639f-117">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="9639f-117">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="9639f-118">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="9639f-118">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="9639f-119">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="9639f-119">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9639f-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9639f-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9639f-121">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="9639f-121">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9639f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-124">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","**\_ StorageAllocationSettingData CIM**.**HostExtentNameNamespace**","[**\_ StorageExtent CIM**](cim-storageextent.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="9639f-124">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-125">Identificador único de la extensión de almacenamiento del host.</span><span class="sxs-lookup"><span data-stu-id="9639f-125">A unique identifier of the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="9639f-126">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="9639f-126">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9639f-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-129">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**\_ StorageAllocationSettingData CIM**.**OtherHostExtentNameFormat**","[**\_ StorageExtent CIM**](cim-storageextent.md).**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="9639f-129">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-130">Formato del valor de la propiedad **HostExtentName** .</span><span class="sxs-lookup"><span data-stu-id="9639f-130">The format that of the **HostExtentName** property value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9639f-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9639f-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9639f-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9639f-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="9639f-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="9639f-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9639f-134">Número de serie/proveedor/modelo (SNVM) SNVM es 3 cadenas que representan el nombre del proveedor, el nombre del producto en el espacio de nombres del proveedor y el número de serie del espacio de nombres del modelo.</span><span class="sxs-lookup"><span data-stu-id="9639f-134">Serial Number/Vendor/Model (SNVM) SNVM is 3 strings representing the vendor name, product name within the vendor namespace, and the serial number within the model namespace.</span></span> <span data-ttu-id="9639f-135">Las cadenas se delimitan con un ' + '.</span><span class="sxs-lookup"><span data-stu-id="9639f-135">Strings are delimited with a '+'.</span></span> <span data-ttu-id="9639f-136">Los espacios se pueden incluir y son significativos.</span><span class="sxs-lookup"><span data-stu-id="9639f-136">Spaces may be included and are significant.</span></span> <span data-ttu-id="9639f-137">El número de serie es la representación de texto del número de serie en mayúsculas hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="9639f-137">The serial number is the text representation of the serial number in hexadecimal upper case.</span></span> <span data-ttu-id="9639f-138">Representa el identificador del proveedor y del modelo de los datos de consulta de SCSI; el campo Vendor debe tener un ancho de 8 caracteres y el campo Product debe tener 16 caracteres de ancho.</span><span class="sxs-lookup"><span data-stu-id="9639f-138">This represents the vendor and model ID from SCSI Inquiry data; the vendor field MUST be 8 characters wide and the product field MUST be 16 characters wide.</span></span> <span data-ttu-id="9639f-139">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="9639f-139">For example,</span></span>

<span data-ttu-id="9639f-140">' Acme \_ \_ \_ \_ + Super Disk \_ \_ \_ \_ \_ \_ + 124437458 ' ( \_ es un carácter de espacio)</span><span class="sxs-lookup"><span data-stu-id="9639f-140">'ACME\_\_\_\_+SUPER DISK\_\_\_\_\_\_+124437458' (\_ is a space character)</span></span>

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="9639f-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span><span class="sxs-lookup"><span data-stu-id="9639f-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9639f-142">9 = NAA como formato genérico.</span><span class="sxs-lookup"><span data-stu-id="9639f-142">9 = NAA as a generic format.</span></span> <span data-ttu-id="9639f-143">Vea</span><span class="sxs-lookup"><span data-stu-id="9639f-143">See</span></span>

<span data-ttu-id="9639f-144"> https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span><span class="sxs-lookup"><span data-stu-id="9639f-144">https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span></span> <span data-ttu-id="9639f-145">Con formato de 16 o 32 caracteres hexadecimales en mayúsculas no separados (2 por byte binario).</span><span class="sxs-lookup"><span data-stu-id="9639f-145">Formatted as 16 or 32 unseparated uppercase hex characters (2 per binary byte).</span></span>

<span data-ttu-id="9639f-146">Por ejemplo, ' 21000020372D3C73 '</span><span class="sxs-lookup"><span data-stu-id="9639f-146">For example '21000020372D3C73'</span></span>

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="9639f-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="9639f-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>


</dt> <dd>

<span data-ttu-id="9639f-148">EUI como formato genérico (EUI64), vea</span><span class="sxs-lookup"><span data-stu-id="9639f-148">EUI as a generic format (EUI64) See</span></span>

<span data-ttu-id="9639f-149"> https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span><span class="sxs-lookup"><span data-stu-id="9639f-149">https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span></span>

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="9639f-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="9639f-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9639f-151">Formato de identificador del proveedor de T10 tal y como lo devolvió la página de VPD de consulta SCSI 83, identificador de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="9639f-151">T10 vendor identifier format as returned by SCSI Inquiry VPD page 83, identifier type 1.</span></span> <span data-ttu-id="9639f-152">Consulte la especificación de T10 SPC-3.</span><span class="sxs-lookup"><span data-stu-id="9639f-152">See T10 SPC-3 specification.</span></span> <span data-ttu-id="9639f-153">Es el ID. de proveedor ASCII de 8 bytes del registro T10 seguido de un identificador ASCII específico del proveedor. se permiten espacios.</span><span class="sxs-lookup"><span data-stu-id="9639f-153">This is the 8-byte ASCII vendor ID from the T10 registry followed by a vendor specific ASCII identifier; spaces are permitted.</span></span> <span data-ttu-id="9639f-154">En el caso de volúmenes no SCSI, "SNVM" puede ser la opción más adecuada.</span><span class="sxs-lookup"><span data-stu-id="9639f-154">For non SCSI volumes, 'SNVM' may be the most appropriate choice.</span></span>

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="9639f-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nombre del dispositivo de SO** (12)</span><span class="sxs-lookup"><span data-stu-id="9639f-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>


</dt> <dd>

<span data-ttu-id="9639f-156">Nombre del dispositivo de sistema operativo (para LogicalDisks).</span><span class="sxs-lookup"><span data-stu-id="9639f-156">OS Device Name (for LogicalDisks).</span></span> <span data-ttu-id="9639f-157">Consulte Descripción del nombre de LogicalDisk para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9639f-157">See LogicalDisk Name description for details.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9639f-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9639f-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9639f-159">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="9639f-159">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-160">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9639f-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-162">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**\_ StorageAllocationSettingData CIM**.**OtherHostExtentNameNamespace**","**\_ StorageAllocationSettingData CIM**.**HostExtentNameFormat**","[**\_ StorageExtent CIM**](cim-storageextent.md).**Espacio de nombres**")</span><span class="sxs-lookup"><span data-stu-id="9639f-162">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Namespace**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-163">El formato de nombre de la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="9639f-163">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9639f-164">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9639f-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9639f-165">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9639f-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="9639f-166">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="9639f-166">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="9639f-167">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="9639f-167">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="9639f-168">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="9639f-168">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="9639f-169">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="9639f-169">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="9639f-170">**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="9639f-170">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="9639f-171">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="9639f-171">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="9639f-172">**Espacio de nombres de dispositivo de SO** (8)</span><span class="sxs-lookup"><span data-stu-id="9639f-172">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9639f-173">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9639f-173">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9639f-174">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="9639f-174">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-175">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9639f-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-177">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**","[**CIM \_ BasedOn**](cim-basedon.md).**StartingAddress**")</span><span class="sxs-lookup"><span data-stu-id="9639f-177">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**", "[**CIM\_BasedOn**](cim-basedon.md).**StartingAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-178">Dirección inicial de la extensión de almacenamiento del host.</span><span class="sxs-lookup"><span data-stu-id="9639f-178">The starting address on the host storage extent.</span></span> <span data-ttu-id="9639f-179">Un valor NULL Val; UE indica que no hay ninguna asignación directa entre la extensión de almacenamiento virtual y la extensión de almacenamiento del host.</span><span class="sxs-lookup"><span data-stu-id="9639f-179">A NULL val;ue indicates that there is no direct mapping between the virtual storage extent and the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="9639f-180">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="9639f-180">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-181">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9639f-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-183">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **punitivo** (" byte ")</span><span class="sxs-lookup"><span data-stu-id="9639f-183">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-184">Tamaño, en bytes, de los bloques que se asignan en el host para la asignación de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9639f-184">The size, in bytes, of the blocks that are allocated on the host for the storage allocation.</span></span> <span data-ttu-id="9639f-185">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque en bytes.</span><span class="sxs-lookup"><span data-stu-id="9639f-185">If the block size is variable, then the maximum block size in bytes should be specified.</span></span> <span data-ttu-id="9639f-186">Si el tamaño de bloque es desconocido o si no se aplica un concepto de bloque, se debe usar el valor "1" (desconocido).</span><span class="sxs-lookup"><span data-stu-id="9639f-186">If the block size is unknown or if a block concept does not apply, then the value "1" (unknown) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="9639f-187">**Límite**</span><span class="sxs-lookup"><span data-stu-id="9639f-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-188">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9639f-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-190">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")</span><span class="sxs-lookup"><span data-stu-id="9639f-190">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-191">La cantidad máxima de bloques que se concederán para la asignación de recursos de almacenamiento en el host.</span><span class="sxs-lookup"><span data-stu-id="9639f-191">The maximum amount of blocks that will be granted for the storage resource allocation on the host.</span></span> <span data-ttu-id="9639f-192">El tamaño de bloque se especifica mediante la propiedad **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="9639f-192">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="9639f-193">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="9639f-193">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9639f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-196">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="9639f-196">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-197">El formato de la propiedad **HostExtentName** si la propiedad se establece en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="9639f-197">The format of the **HostExtentName** property if the property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="9639f-198">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="9639f-198">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9639f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-201">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="9639f-201">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-202">Una cadena que describe el espacio de nombres de la propiedad **HostExtentName** si el valor de la propiedad **HostExtentNameNamespace** es "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="9639f-202">A string that describes the namespace of the **HostExtentName** property if the value of the **HostExtentNameNamespace** property is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="9639f-203">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="9639f-203">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-204">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9639f-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-206">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("reserva"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")</span><span class="sxs-lookup"><span data-stu-id="9639f-206">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-207">La cantidad de bloques que se garantiza que estarán disponibles para la asignación de recursos de almacenamiento en el host.</span><span class="sxs-lookup"><span data-stu-id="9639f-207">The amount of blocks that are guaranteed to be available for the storage resource allocation on the host.</span></span> <span data-ttu-id="9639f-208">El tamaño de bloque se especifica mediante la propiedad **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="9639f-208">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="9639f-209">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="9639f-209">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-210">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9639f-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-212">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**NumberOfBlocks**","**\_ StorageAllocationSettingData CIM**.**VirtualQuantityUnits**")</span><span class="sxs-lookup"><span data-stu-id="9639f-212">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**NumberOfBlocks**", "**CIM\_StorageAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-213">El número de bloques que la asignación de almacenamiento presenta al consumidor.</span><span class="sxs-lookup"><span data-stu-id="9639f-213">The number of blocks that the storage allocation presents to the consumer.</span></span>

> [!Note]  
> <span data-ttu-id="9639f-214">La propiedad **VirtualQuantity** puede especificar un tamaño de bloque de "1", incluso si se desconoce **VirtualResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="9639f-214">The **VirtualQuantity** property can specify a block size of "1", even if **VirtualResourceBlockSize** is unknown.</span></span>

 

</dd> <dt>

<span data-ttu-id="9639f-215">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="9639f-215">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9639f-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-218">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="9639f-218">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="9639f-219">Unidades utilizadas por la propiedad **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="9639f-219">The units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="9639f-220">Este valor debe establecerse en "recuento (bloque de tamaño fijo)" o "byte".</span><span class="sxs-lookup"><span data-stu-id="9639f-220">This value shall should be set to "count(fixed size block)" or "byte".</span></span> <span data-ttu-id="9639f-221">El valor predeterminado, "Count (bloque de tamaño fijo)", debe usarse para un tamaño de bloque fijo y "byte" se debe usar para un tamaño de bloque desconocido o variable.</span><span class="sxs-lookup"><span data-stu-id="9639f-221">The default value, "count(fixed size block)" should be used for a fixed block size, and "byte" should be used for an unknown or variable block size.</span></span>

</dd> <dt>

<span data-ttu-id="9639f-222">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="9639f-222">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9639f-223">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9639f-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9639f-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9639f-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9639f-225">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **punitivo** (" byte ")</span><span class="sxs-lookup"><span data-stu-id="9639f-225">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="9639f-226">Tamaño, en bytes, de los bloques que forman la solicitud de asignación de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9639f-226">The size, in bytes, of the blocks that form the storage allocation request.</span></span> <span data-ttu-id="9639f-227">Si el tamaño del bloque es variable, se debe especificar el tamaño máximo del bloque.</span><span class="sxs-lookup"><span data-stu-id="9639f-227">If the block size is variable, then the maximum block size should be specified.</span></span> <span data-ttu-id="9639f-228">Si el tamaño de bloque es desconocido o si no se aplica un concepto de bloque, el tamaño de bloque debe ser "1" (desconocido).</span><span class="sxs-lookup"><span data-stu-id="9639f-228">If the block size is unknown or if a block concept does not apply, then the block size should be "1" (unknown).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9639f-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9639f-229">Requirements</span></span>



| <span data-ttu-id="9639f-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="9639f-230">Requirement</span></span> | <span data-ttu-id="9639f-231">Value</span><span class="sxs-lookup"><span data-stu-id="9639f-231">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9639f-232">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9639f-232">Minimum supported client</span></span><br/> | <span data-ttu-id="9639f-233">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9639f-233">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9639f-234">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9639f-234">Minimum supported server</span></span><br/> | <span data-ttu-id="9639f-235">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9639f-235">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9639f-236">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9639f-236">Namespace</span></span><br/>                | <span data-ttu-id="9639f-237">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9639f-237">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9639f-238">MOF</span><span class="sxs-lookup"><span data-stu-id="9639f-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9639f-239"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9639f-239"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9639f-240">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9639f-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9639f-241"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9639f-241"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9639f-242">Vea también</span><span class="sxs-lookup"><span data-stu-id="9639f-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9639f-243">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="9639f-243">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

