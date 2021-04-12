---
title: Win32_TSNetworkAdapterSetting (clase)
description: Define diversos valores de configuración para la \_ clase de terminal Win32, incluidas las propiedades relacionadas con el adaptador de red y el número máximo de conexiones permitidas.
ms.assetid: b8a757e6-801b-4349-902e-76596b06df1f
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSNetworkAdapterSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting.Caption
- Win32_TSNetworkAdapterSetting.Description
- Win32_TSNetworkAdapterSetting.InstallDate
- Win32_TSNetworkAdapterSetting.Name
- Win32_TSNetworkAdapterSetting.Status
- Win32_TSNetworkAdapterSetting.TerminalName
- Win32_TSNetworkAdapterSetting.DeviceIDList
- Win32_TSNetworkAdapterSetting.MaximumConnections
- Win32_TSNetworkAdapterSetting.NetworkAdapterID
- Win32_TSNetworkAdapterSetting.NetworkAdapterLanaID
- Win32_TSNetworkAdapterSetting.NetworkAdapterList
- Win32_TSNetworkAdapterSetting.NetworkAdapterName
- Win32_TSNetworkAdapterSetting.PolicySourceMaximumConnections
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f2f2f1ac7d6bf4b1fd3fb5f5a92fc4fd5260a92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491591"
---
# <a name="win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="86dbe-105">\_Clase Win32 TSNetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="86dbe-105">Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="86dbe-106">La clase WMI **\_ TSNetworkAdapterSetting de Win32** define varios valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) , incluidas las propiedades relacionadas con el adaptador de red y el número máximo de conexiones permitidas.</span><span class="sxs-lookup"><span data-stu-id="86dbe-106">The **Win32\_TSNetworkAdapterSetting** WMI class defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

<span data-ttu-id="86dbe-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="86dbe-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="86dbe-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="86dbe-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="86dbe-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86dbe-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSNETWORKADAPTERSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   DeviceIDList[];
  uint32   MaximumConnections;
  string   NetworkAdapterID;
  uint32   NetworkAdapterLanaID;
  string   NetworkAdapterList[];
  string   NetworkAdapterName;
  uint32   PolicySourceMaximumConnections;
};
```

## <a name="members"></a><span data-ttu-id="86dbe-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="86dbe-110">Members</span></span>

<span data-ttu-id="86dbe-111">La **clase \_ TSNetworkAdapterSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="86dbe-111">The **Win32\_TSNetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="86dbe-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="86dbe-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="86dbe-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86dbe-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="86dbe-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="86dbe-114">Methods</span></span>

<span data-ttu-id="86dbe-115">La clase **Win32 \_ TSNetworkAdapterSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="86dbe-115">The **Win32\_TSNetworkAdapterSetting** class has these methods.</span></span>



| <span data-ttu-id="86dbe-116">Método</span><span class="sxs-lookup"><span data-stu-id="86dbe-116">Method</span></span>                                                                                     | <span data-ttu-id="86dbe-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="86dbe-117">Description</span></span>                                                                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86dbe-118">**SelectAllNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="86dbe-118">**SelectAllNetworkAdapters**</span></span>](win32-tsnetworkadaptersetting-selectallnetworkadapters.md) | <span data-ttu-id="86dbe-119">Selecciona todos los adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="86dbe-119">Selects all network adapters.</span></span><br/>                                                                 |
| [<span data-ttu-id="86dbe-120">**SelectNetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="86dbe-120">**SelectNetworkAdapterIP**</span></span>](win32-tsnetworkadaptersetting-selectnetworkadapterip.md)     | <span data-ttu-id="86dbe-121">Selecciona un adaptador de red basado en la dirección IP del adaptador.</span><span class="sxs-lookup"><span data-stu-id="86dbe-121">Selects a network adapter based on the adapter's IP address.</span></span><br/>                                  |
| [<span data-ttu-id="86dbe-122">**SetNetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="86dbe-122">**SetNetworkAdapterLanaID**</span></span>](setnetworkadapterlanaid-win32-tsnetworkadaptersetting.md)   | <span data-ttu-id="86dbe-123">Especifica el número de adaptador de red de área local (LANA) de NetBIOS del adaptador de red que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="86dbe-123">Specifies the NetBIOS Local Area Network Adapter (LANA) number of the network adapter to set.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="86dbe-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86dbe-124">Properties</span></span>

<span data-ttu-id="86dbe-125">La **clase \_ TSNetworkAdapterSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="86dbe-125">The **Win32\_TSNetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86dbe-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="86dbe-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86dbe-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-129">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="86dbe-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-130">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="86dbe-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="86dbe-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86dbe-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86dbe-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86dbe-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-135">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="86dbe-135">Description of the object.</span></span>

<span data-ttu-id="86dbe-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86dbe-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-137">**DeviceIDList**</span><span class="sxs-lookup"><span data-stu-id="86dbe-137">**DeviceIDList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-138">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="86dbe-138">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-140">Matriz de cadenas de los identificadores de dispositivo disponibles devueltos en el orden de los adaptadores de red físicos devueltos en la matriz de propiedades **NetworkAdapterList** .</span><span class="sxs-lookup"><span data-stu-id="86dbe-140">String array of available device IDs returned in the order of physical network adapters returned in the **NetworkAdapterList** property array.</span></span> <span data-ttu-id="86dbe-141">El valor del identificador de dispositivo es la propiedad **DeviceID** en el [**\_ adaptador de Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter) .</span><span class="sxs-lookup"><span data-stu-id="86dbe-141">The device ID value is the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="86dbe-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-143">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="86dbe-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-145">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="86dbe-145">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-146">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="86dbe-146">The date the object was installed.</span></span> <span data-ttu-id="86dbe-147">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="86dbe-147">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="86dbe-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86dbe-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-149">**MaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="86dbe-149">**MaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86dbe-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="86dbe-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-152">Número máximo de conexiones permitidas.</span><span class="sxs-lookup"><span data-stu-id="86dbe-152">The maximum number of connections allowed.</span></span> <span data-ttu-id="86dbe-153">El valor **MAXINT** denota un número ilimitado de conexiones.</span><span class="sxs-lookup"><span data-stu-id="86dbe-153">The value **MAXINT** denotes an unlimited number of connections.</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-154">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="86dbe-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86dbe-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-157">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="86dbe-157">The name of the object.</span></span>

<span data-ttu-id="86dbe-158">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86dbe-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-159">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="86dbe-159">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86dbe-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-162">GUID que representa el identificador del adaptador de red que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="86dbe-162">The GUID that represents the ID of the network adapter to set.</span></span> <span data-ttu-id="86dbe-163">Un **GUID** que consta de todos los ceros denota todos los adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="86dbe-163">A **GUID** that consists of all zeros denotes all network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-164">**NetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="86dbe-164">**NetworkAdapterLanaID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86dbe-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-167">Número de adaptador de red de área local (LANA) de NetBIOS del adaptador de red que se usa para identificar el adaptador de red asignado al terminal.</span><span class="sxs-lookup"><span data-stu-id="86dbe-167">NetBIOS Local Area Network Adapter (LANA) number of the network adapter that is used to identify the network adapter assigned to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-168">**NetworkAdapterList**</span><span class="sxs-lookup"><span data-stu-id="86dbe-168">**NetworkAdapterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-169">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="86dbe-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-171">Matriz de cadenas de adaptadores de red físicos disponibles y los identificadores de dispositivo correspondientes.</span><span class="sxs-lookup"><span data-stu-id="86dbe-171">String array of available physical network adapters and the corresponding device IDs.</span></span> <span data-ttu-id="86dbe-172">Los identificadores de dispositivo son la propiedad **DeviceID** en el [**\_ adaptador de Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span><span class="sxs-lookup"><span data-stu-id="86dbe-172">The device IDs are the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-173">**NetworkAdapterName**</span><span class="sxs-lookup"><span data-stu-id="86dbe-173">**NetworkAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86dbe-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-176">Descripción del adaptador de red que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="86dbe-176">Description of the network adapter to set.</span></span> <span data-ttu-id="86dbe-177">Este valor se encuentra en [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span><span class="sxs-lookup"><span data-stu-id="86dbe-177">This value is in [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-178">**PolicySourceMaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="86dbe-178">**PolicySourceMaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-179">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86dbe-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-181">Indica si la propiedad **MaximumConnections** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86dbe-181">Indicates whether the **MaximumConnections** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="86dbe-182">0</span><span class="sxs-lookup"><span data-stu-id="86dbe-182">0</span></span>
</dt> <dd>

<span data-ttu-id="86dbe-183">Servidor</span><span class="sxs-lookup"><span data-stu-id="86dbe-183">Server</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-184">1</span><span class="sxs-lookup"><span data-stu-id="86dbe-184">1</span></span>
</dt> <dd>

<span data-ttu-id="86dbe-185">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="86dbe-185">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="86dbe-186">2</span><span class="sxs-lookup"><span data-stu-id="86dbe-186">2</span></span>
</dt> <dd>

<span data-ttu-id="86dbe-187">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="86dbe-187">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="86dbe-188">**Estado**</span><span class="sxs-lookup"><span data-stu-id="86dbe-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86dbe-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-191">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="86dbe-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-192">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="86dbe-192">Current status of the object.</span></span> <span data-ttu-id="86dbe-193">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="86dbe-193">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="86dbe-194">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="86dbe-194">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="86dbe-195">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="86dbe-195">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="86dbe-196">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="86dbe-196">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="86dbe-197">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="86dbe-197">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="86dbe-198">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="86dbe-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="86dbe-199">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="86dbe-199">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="86dbe-200">("Error")</span><span class="sxs-lookup"><span data-stu-id="86dbe-200">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="86dbe-201">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="86dbe-201">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="86dbe-202">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="86dbe-202">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="86dbe-203">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="86dbe-203">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="86dbe-204">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="86dbe-204">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="86dbe-205">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="86dbe-205">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="86dbe-206">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="86dbe-206">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86dbe-207">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="86dbe-207">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86dbe-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86dbe-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86dbe-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86dbe-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86dbe-210">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="86dbe-210">The name of the terminal.</span></span>

<span data-ttu-id="86dbe-211">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="86dbe-211">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86dbe-212">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86dbe-212">Remarks</span></span>

<span data-ttu-id="86dbe-213">Tenga en cuenta que Winstations asociado a la sesión de consola no puede tener acceso a los métodos y las propiedades de esta clase.</span><span class="sxs-lookup"><span data-stu-id="86dbe-213">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="86dbe-214">Si se realiza un intento de hacerlo especificando "Console" como el valor de la propiedad TerminalName, los métodos de este objeto devuelven **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="86dbe-214">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="86dbe-215">Este código de error también se devuelve si una estación de ventana intenta llamar a métodos de este objeto para agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="86dbe-215">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="86dbe-216">Para conectarse al espacio de nombres "root \\ cimv2 \\ TerminalServices", el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="86dbe-216">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="86dbe-217">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="86dbe-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="86dbe-218">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="86dbe-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="86dbe-219">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="86dbe-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="86dbe-220">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="86dbe-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="86dbe-221">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="86dbe-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="86dbe-222">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="86dbe-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="86dbe-223">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="86dbe-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="86dbe-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86dbe-224">Requirements</span></span>



| <span data-ttu-id="86dbe-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="86dbe-225">Requirement</span></span> | <span data-ttu-id="86dbe-226">Value</span><span class="sxs-lookup"><span data-stu-id="86dbe-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86dbe-227">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86dbe-227">Minimum supported client</span></span><br/> | <span data-ttu-id="86dbe-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86dbe-228">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86dbe-229">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86dbe-229">Minimum supported server</span></span><br/> | <span data-ttu-id="86dbe-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86dbe-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86dbe-231">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="86dbe-231">Namespace</span></span><br/>                | <span data-ttu-id="86dbe-232">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="86dbe-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="86dbe-233">MOF</span><span class="sxs-lookup"><span data-stu-id="86dbe-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86dbe-234"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86dbe-234"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="86dbe-235">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86dbe-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86dbe-236"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86dbe-236"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86dbe-237">Vea también</span><span class="sxs-lookup"><span data-stu-id="86dbe-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86dbe-238">**Adaptador de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="86dbe-238">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)
</dt> <dt>

[<span data-ttu-id="86dbe-239">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="86dbe-239">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
</dt> <dt>

[<span data-ttu-id="86dbe-240">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="86dbe-240">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="86dbe-241">**Win32 \_ TSNetworkAdapterListSetting**</span><span class="sxs-lookup"><span data-stu-id="86dbe-241">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> </dl>

 

