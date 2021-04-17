---
description: Representa una propiedad de dispositivo PnP que consta de una matriz de elementos Uint16.
ms.assetid: A86C68BB-9CC6-4D0E-B2C9-91E3BF00077E
ms.tgt_platform: multiple
title: Win32_PnPDevicePropertyUint16Array (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevicePropertyUint16Array
- Win32_PnPDevicePropertyUint16Array.Key
- Win32_PnPDevicePropertyUint16Array.KeyName
- Win32_PnPDevicePropertyUint16Array.Type
- Win32_PnPDevicePropertyUint16Array.DeviceID
- Win32_PnPDevicePropertyUint16Array.Data
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0affb7a3fc08c964b2aecd9e43e410c4175b9c97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659738"
---
# <a name="win32_pnpdevicepropertyuint16array-class"></a><span data-ttu-id="8058c-103">\_Clase Win32 PnPDevicePropertyUint16Array</span><span class="sxs-lookup"><span data-stu-id="8058c-103">Win32\_PnPDevicePropertyUint16Array class</span></span>

<span data-ttu-id="8058c-104">Representa una propiedad de dispositivo PnP que consta de una matriz de elementos **Uint16** .</span><span class="sxs-lookup"><span data-stu-id="8058c-104">Represents a PnP device property consisting of an array of **Uint16** elements.</span></span>

<span data-ttu-id="8058c-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8058c-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8058c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8058c-106">Syntax</span></span>

``` syntax
class Win32_PnPDevicePropertyUint16Array : Win32_PnPDeviceProperty
{
  string Key;
  string KeyName;
  Uint32 Type;
  string DeviceID;
  Uint16 Data[];
};
```

## <a name="members"></a><span data-ttu-id="8058c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8058c-107">Members</span></span>

<span data-ttu-id="8058c-108">La **clase \_ PnPDevicePropertyUint16Array de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8058c-108">The **Win32\_PnPDevicePropertyUint16Array** class has these types of members:</span></span>

-   [<span data-ttu-id="8058c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8058c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8058c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8058c-110">Properties</span></span>

<span data-ttu-id="8058c-111">La **clase \_ PnPDevicePropertyUint16Array de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8058c-111">The **Win32\_PnPDevicePropertyUint16Array** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8058c-112">**Data**</span><span class="sxs-lookup"><span data-stu-id="8058c-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8058c-113">Tipo de datos: matriz **Uint16**</span><span class="sxs-lookup"><span data-stu-id="8058c-113">Data type: **Uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8058c-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8058c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8058c-115">Valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8058c-115">The property value.</span></span>

</dd> <dt>

<span data-ttu-id="8058c-116">**ID**</span><span class="sxs-lookup"><span data-stu-id="8058c-116">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8058c-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8058c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8058c-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8058c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8058c-119">Identifica el dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="8058c-119">Identifies the PnP device.</span></span>

<span data-ttu-id="8058c-120">Esta propiedad se hereda de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8058c-120">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="8058c-121">**Clave**</span><span class="sxs-lookup"><span data-stu-id="8058c-121">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8058c-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8058c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8058c-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8058c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8058c-124">Valor del par de Name-Value de claves que identifica la propiedad de **datos** .</span><span class="sxs-lookup"><span data-stu-id="8058c-124">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="8058c-125">Esta propiedad se hereda de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8058c-125">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="8058c-126">**Clave**</span><span class="sxs-lookup"><span data-stu-id="8058c-126">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8058c-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8058c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8058c-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8058c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8058c-129">Nombre del par de Name-Value de claves que identifica la propiedad de **datos** .</span><span class="sxs-lookup"><span data-stu-id="8058c-129">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="8058c-130">Esta propiedad se hereda de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8058c-130">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="8058c-131">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8058c-131">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8058c-132">Tipo de datos: **Uint32**</span><span class="sxs-lookup"><span data-stu-id="8058c-132">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8058c-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8058c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8058c-134">Tipo de la propiedad de **datos** .</span><span class="sxs-lookup"><span data-stu-id="8058c-134">The type of the **Data** property.</span></span>

<span data-ttu-id="8058c-135">Esta propiedad se hereda de [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8058c-135">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

<span data-ttu-id="8058c-136">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="8058c-136">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="8058c-137">**Vacío** (0)</span><span class="sxs-lookup"><span data-stu-id="8058c-137">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="8058c-138">**Null** (1)</span><span class="sxs-lookup"><span data-stu-id="8058c-138">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="8058c-139">**SByte** (2)</span><span class="sxs-lookup"><span data-stu-id="8058c-139">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="8058c-140">**Byte** (3)</span><span class="sxs-lookup"><span data-stu-id="8058c-140">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="8058c-141">**Int16** (4)</span><span class="sxs-lookup"><span data-stu-id="8058c-141">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="8058c-142">**UInt16** (5)</span><span class="sxs-lookup"><span data-stu-id="8058c-142">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="8058c-143">**Int32** (6)</span><span class="sxs-lookup"><span data-stu-id="8058c-143">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="8058c-144">**Uint32** (7)</span><span class="sxs-lookup"><span data-stu-id="8058c-144">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="8058c-145">**Int64** (8)</span><span class="sxs-lookup"><span data-stu-id="8058c-145">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="8058c-146">**UInt64** (9)</span><span class="sxs-lookup"><span data-stu-id="8058c-146">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="8058c-147">**Float** (10)</span><span class="sxs-lookup"><span data-stu-id="8058c-147">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="8058c-148">**Double** (11)</span><span class="sxs-lookup"><span data-stu-id="8058c-148">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="8058c-149">**Decimal** (12)</span><span class="sxs-lookup"><span data-stu-id="8058c-149">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="8058c-150">**GUID** (13)</span><span class="sxs-lookup"><span data-stu-id="8058c-150">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="8058c-151">**Moneda** (14)</span><span class="sxs-lookup"><span data-stu-id="8058c-151">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="8058c-152">**Fecha** (15)</span><span class="sxs-lookup"><span data-stu-id="8058c-152">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="8058c-153">**FileTime** (16)</span><span class="sxs-lookup"><span data-stu-id="8058c-153">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="8058c-154">**Booleano** (17)</span><span class="sxs-lookup"><span data-stu-id="8058c-154">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="8058c-155">**Cadena** (18)</span><span class="sxs-lookup"><span data-stu-id="8058c-155">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="8058c-156">**SecurityDescriptor** (19)</span><span class="sxs-lookup"><span data-stu-id="8058c-156">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="8058c-157">**SecurityDescriptorString** (20)</span><span class="sxs-lookup"><span data-stu-id="8058c-157">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="8058c-158">**DEVPROPKEY** (21)</span><span class="sxs-lookup"><span data-stu-id="8058c-158">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="8058c-159">**DEVPROPTYPE** (22)</span><span class="sxs-lookup"><span data-stu-id="8058c-159">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8058c-160">**Error** (23)</span><span class="sxs-lookup"><span data-stu-id="8058c-160">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="8058c-161">**NTStatus** (24)</span><span class="sxs-lookup"><span data-stu-id="8058c-161">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="8058c-162">**StringIndirect** (25)</span><span class="sxs-lookup"><span data-stu-id="8058c-162">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="8058c-163">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="8058c-163">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="8058c-164">26 –</span><span class="sxs-lookup"><span data-stu-id="8058c-164">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="8058c-165">**SByteArray** (4098)</span><span class="sxs-lookup"><span data-stu-id="8058c-165">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="8058c-166">**Binario** (4099)</span><span class="sxs-lookup"><span data-stu-id="8058c-166">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="8058c-167">**, Int16array** (4100)</span><span class="sxs-lookup"><span data-stu-id="8058c-167">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="8058c-168">**, Uint16array** (4101)</span><span class="sxs-lookup"><span data-stu-id="8058c-168">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="8058c-169">**Int64Array** (4102)</span><span class="sxs-lookup"><span data-stu-id="8058c-169">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="8058c-170">**UInt64Array** (4103)</span><span class="sxs-lookup"><span data-stu-id="8058c-170">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="8058c-171">**FloatArray** (4104)</span><span class="sxs-lookup"><span data-stu-id="8058c-171">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="8058c-172">**DoubleArray** (4105)</span><span class="sxs-lookup"><span data-stu-id="8058c-172">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="8058c-173">**DecimalArray** (4106)</span><span class="sxs-lookup"><span data-stu-id="8058c-173">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="8058c-174">**GuidArray** (4107)</span><span class="sxs-lookup"><span data-stu-id="8058c-174">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="8058c-175">**CurrencyArray** (4108)</span><span class="sxs-lookup"><span data-stu-id="8058c-175">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="8058c-176">**DateArray** (4109)</span><span class="sxs-lookup"><span data-stu-id="8058c-176">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="8058c-177">**FileTimeArray** (4110)</span><span class="sxs-lookup"><span data-stu-id="8058c-177">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="8058c-178">**BooleanArray** (4111)</span><span class="sxs-lookup"><span data-stu-id="8058c-178">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="8058c-179">**StringList** (4112)</span><span class="sxs-lookup"><span data-stu-id="8058c-179">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="8058c-180">**SecurityDescriptorList** (4113)</span><span class="sxs-lookup"><span data-stu-id="8058c-180">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="8058c-181">**SecurityDescriptorStringList** (8210)</span><span class="sxs-lookup"><span data-stu-id="8058c-181">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="8058c-182">**DEVPROPKEYArray** (8211)</span><span class="sxs-lookup"><span data-stu-id="8058c-182">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="8058c-183">**DEVPROPTYPEArray** (8212)</span><span class="sxs-lookup"><span data-stu-id="8058c-183">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="8058c-184">**ErrorArray** (4117)</span><span class="sxs-lookup"><span data-stu-id="8058c-184">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="8058c-185">**NTStatusArray** (4118)</span><span class="sxs-lookup"><span data-stu-id="8058c-185">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="8058c-186">**StringIndirectList** (4119)</span><span class="sxs-lookup"><span data-stu-id="8058c-186">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="8058c-187">**Unknown-check en devpropdef. h** (4120)</span><span class="sxs-lookup"><span data-stu-id="8058c-187">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="8058c-188">**TBD** (8217)</span><span class="sxs-lookup"><span data-stu-id="8058c-188">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="8058c-189">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="8058c-189">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="8058c-190">8218:4294967295</span><span class="sxs-lookup"><span data-stu-id="8058c-190">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8058c-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8058c-191">Requirements</span></span>



| <span data-ttu-id="8058c-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="8058c-192">Requirement</span></span> | <span data-ttu-id="8058c-193">Value</span><span class="sxs-lookup"><span data-stu-id="8058c-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8058c-194">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8058c-194">Minimum supported client</span></span><br/> | <span data-ttu-id="8058c-195">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8058c-195">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8058c-196">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8058c-196">Minimum supported server</span></span><br/> | <span data-ttu-id="8058c-197">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8058c-197">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="8058c-198">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8058c-198">Namespace</span></span><br/>                | <span data-ttu-id="8058c-199">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8058c-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8058c-200">MOF</span><span class="sxs-lookup"><span data-stu-id="8058c-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8058c-201"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8058c-201"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8058c-202">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8058c-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8058c-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8058c-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8058c-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="8058c-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8058c-205">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="8058c-205">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8058c-206">**Win32 \_ PnPDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="8058c-206">**Win32\_PnPDeviceProperty**</span></span>](win32-pnpdeviceproperty.md)
</dt> <dt>

[<span data-ttu-id="8058c-207">**GetDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="8058c-207">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md)
</dt> </dl>

 

 




