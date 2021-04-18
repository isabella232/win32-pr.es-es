---
description: Representa la información de identificación de un monitor de vídeo, como el nombre del fabricante, el año de fabricación o el número de serie.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Clase WmiMonitorID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105718589"
---
# <a name="wmimonitorid-class"></a><span data-ttu-id="9390d-103">Clase WmiMonitorID</span><span class="sxs-lookup"><span data-stu-id="9390d-103">WmiMonitorID class</span></span>

<span data-ttu-id="9390d-104">La clase WMI **WmiMonitorID** representa la información de identificación de un monitor de vídeo, como el nombre del fabricante, el año de fabricación o el número de serie.</span><span class="sxs-lookup"><span data-stu-id="9390d-104">The **WmiMonitorID** WMI class represents the identifying information about a video monitor, such as manufacturer name, year of manufacture, or serial number.</span></span> <span data-ttu-id="9390d-105">Los datos de esta clase se corresponden con los datos del bloque de identificación de proveedor/producto de la definición de entrada de vídeo de la estándar de identificación extendida de vídeo (E-EDID) de la Asociación estándar de vídeo electrónica (VESA).</span><span class="sxs-lookup"><span data-stu-id="9390d-105">The data in this class correspond to data in the Vendor/Product Identification block of Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="9390d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9390d-106">Syntax</span></span>

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a><span data-ttu-id="9390d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9390d-107">Members</span></span>

<span data-ttu-id="9390d-108">La clase **WmiMonitorID** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9390d-108">The **WmiMonitorID** class has these types of members:</span></span>

-   [<span data-ttu-id="9390d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9390d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9390d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9390d-110">Properties</span></span>

<span data-ttu-id="9390d-111">La clase **WmiMonitorID** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9390d-111">The **WmiMonitorID** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9390d-112">**Activo**</span><span class="sxs-lookup"><span data-stu-id="9390d-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9390d-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9390d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9390d-115">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="9390d-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="9390d-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="9390d-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9390d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9390d-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9390d-119">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="9390d-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9390d-120">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="9390d-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="9390d-121">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="9390d-121">**ManufacturerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-122">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9390d-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9390d-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9390d-124">Nombre del fabricante.</span><span class="sxs-lookup"><span data-stu-id="9390d-124">Name of manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="9390d-125">**ManufacturerNameLength**</span><span class="sxs-lookup"><span data-stu-id="9390d-125">**ManufacturerNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9390d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9390d-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9390d-128">Longitud del nombre del fabricante ubicada en la propiedad **ManufacturerName** .</span><span class="sxs-lookup"><span data-stu-id="9390d-128">Length of manufacturer name located in the **ManufacturerName** property.</span></span>

</dd> <dt>

<span data-ttu-id="9390d-129">**ProductCodeID**</span><span class="sxs-lookup"><span data-stu-id="9390d-129">**ProductCodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-130">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9390d-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9390d-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9390d-132">IDENTIFICADOR de código de producto asignado por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="9390d-132">Vendor assigned product code ID.</span></span>

</dd> <dt>

<span data-ttu-id="9390d-133">**SerialNumberID**</span><span class="sxs-lookup"><span data-stu-id="9390d-133">**SerialNumberID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-134">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9390d-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9390d-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9390d-136">Número de serie.</span><span class="sxs-lookup"><span data-stu-id="9390d-136">Serial number.</span></span>

</dd> <dt>

<span data-ttu-id="9390d-137">UserFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9390d-137">UserFriendlyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-138">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9390d-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9390d-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9390d-140">Nombre descriptivo del monitor.</span><span class="sxs-lookup"><span data-stu-id="9390d-140">The friendly name of the monitor.</span></span> <span data-ttu-id="9390d-141">El tamaño del nombre es la longitud especificada por la propiedad UserFriendlyNameLength.</span><span class="sxs-lookup"><span data-stu-id="9390d-141">The size of the name is the length specified by the UserFriendlyNameLength property.</span></span>

</dd> <dt>

<span data-ttu-id="9390d-142">UserFriendlyNameLength</span><span class="sxs-lookup"><span data-stu-id="9390d-142">UserFriendlyNameLength</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-143">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9390d-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9390d-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9390d-145">Número de caracteres del nombre que se encuentra en la propiedad UserFriendlyName.</span><span class="sxs-lookup"><span data-stu-id="9390d-145">Number of characters in the name located in the UserFriendlyName property.</span></span>

</dd> <dt>

<span data-ttu-id="9390d-146">**WeekOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="9390d-146">**WeekOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-147">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9390d-147">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9390d-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9390d-149">Semana de fabricación por número de semana.</span><span class="sxs-lookup"><span data-stu-id="9390d-149">Week of manufacture by week number.</span></span> <span data-ttu-id="9390d-150">El intervalo está comprendido entre 1 y 53.</span><span class="sxs-lookup"><span data-stu-id="9390d-150">The range is from 1 through 53.</span></span> <span data-ttu-id="9390d-151">Cero (0) no está definido.</span><span class="sxs-lookup"><span data-stu-id="9390d-151">Zero (0) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="9390d-152">**YearOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="9390d-152">**YearOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9390d-153">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9390d-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9390d-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9390d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9390d-155">Año de fabricación.</span><span class="sxs-lookup"><span data-stu-id="9390d-155">Year of manufacture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9390d-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9390d-156">Remarks</span></span>

<span data-ttu-id="9390d-157">Para obtener una explicación sobre cómo traducir las matrices que almacenan los IDENTIFICADOres de número de serie, consulte el artículo [información del monitor de informes con Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog.</span><span class="sxs-lookup"><span data-stu-id="9390d-157">For a discussion on how to translate the arrays that store serial number ID's, see the [Reporting Monitor information with Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog article.</span></span>

## <a name="examples"></a><span data-ttu-id="9390d-158">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9390d-158">Examples</span></span>

<span data-ttu-id="9390d-159">En el siguiente ejemplo de PowerShell se recupera el número de serie de varios monitores.</span><span class="sxs-lookup"><span data-stu-id="9390d-159">The following PowerShell example retrieves the serial number of multiple monitors.</span></span>


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



<span data-ttu-id="9390d-160">El siguiente código de VBScript también recupera información del ID. de monitor de un sistema.</span><span class="sxs-lookup"><span data-stu-id="9390d-160">The following VBScript code also retrieves monitor ID information from a system.</span></span>


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a><span data-ttu-id="9390d-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9390d-161">Requirements</span></span>



| <span data-ttu-id="9390d-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="9390d-162">Requirement</span></span> | <span data-ttu-id="9390d-163">Value</span><span class="sxs-lookup"><span data-stu-id="9390d-163">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9390d-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9390d-164">Minimum supported client</span></span><br/> | <span data-ttu-id="9390d-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9390d-165">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9390d-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9390d-166">Minimum supported server</span></span><br/> | <span data-ttu-id="9390d-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9390d-167">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9390d-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9390d-168">Namespace</span></span><br/>                | <span data-ttu-id="9390d-169">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="9390d-169">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9390d-170">MOF</span><span class="sxs-lookup"><span data-stu-id="9390d-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9390d-171"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9390d-171"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9390d-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9390d-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9390d-173"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9390d-173"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9390d-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="9390d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9390d-175">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="9390d-175">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

