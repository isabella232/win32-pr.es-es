---
title: Win32_TSClientSetting (clase)
description: Define la configuración para la \_ clase de terminal Win32 relacionada con la Directiva de conexión.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Win32_TSClientSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSClientSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204f38570e1e023ca070ed1845e4574d9570b8ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151004"
---
# <a name="win32_tsclientsetting-class"></a><span data-ttu-id="8f828-105">\_Clase Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="8f828-105">Win32\_TSClientSetting class</span></span>

<span data-ttu-id="8f828-106">La clase WMI **\_ TSClientSetting de Win32** define los valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) relacionada con la Directiva de conexión.</span><span class="sxs-lookup"><span data-stu-id="8f828-106">The **Win32\_TSClientSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

<span data-ttu-id="8f828-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="8f828-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="8f828-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="8f828-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f828-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f828-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a><span data-ttu-id="8f828-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f828-110">Members</span></span>

<span data-ttu-id="8f828-111">La **clase \_ TSClientSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8f828-111">The **Win32\_TSClientSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8f828-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8f828-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f828-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f828-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f828-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="8f828-114">Methods</span></span>

<span data-ttu-id="8f828-115">La clase **Win32 \_ TSClientSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8f828-115">The **Win32\_TSClientSetting** class has these methods.</span></span>



| <span data-ttu-id="8f828-116">Método</span><span class="sxs-lookup"><span data-stu-id="8f828-116">Method</span></span>                                                                   | <span data-ttu-id="8f828-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f828-117">Description</span></span>                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f828-118">**ConnectionSettings**</span><span class="sxs-lookup"><span data-stu-id="8f828-118">**ConnectionSettings**</span></span>](win32-tsclientsetting-connectionsettings.md)   | <span data-ttu-id="8f828-119">Establece las propiedades **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon** y **DefaultToClientPrinter** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8f828-119">Sets the **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon**, and **DefaultToClientPrinter** properties of this class.</span></span><br/>                      |
| [<span data-ttu-id="8f828-120">**SetAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="8f828-120">**SetAllowDwm**</span></span>](setallowdwm-win32-tsclientsetting.md)                 | <span data-ttu-id="8f828-121">No se admite.</span><span class="sxs-lookup"><span data-stu-id="8f828-121">Not supported.</span></span><br/> <span data-ttu-id="8f828-122">**Windows 7 y Windows Server 2008 R2:** Establece la propiedad **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="8f828-122">**Windows 7 and Windows Server 2008 R2:** Sets the **AllowDwm** property.</span></span><br/>                                               |
| [<span data-ttu-id="8f828-123">**SetClientProperty**</span><span class="sxs-lookup"><span data-stu-id="8f828-123">**SetClientProperty**</span></span>](win32-tsclientsetting-setclientproperty.md)     | <span data-ttu-id="8f828-124">Establece la propiedad **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** o **WindowsPrinterMapping** .</span><span class="sxs-lookup"><span data-stu-id="8f828-124">Sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property.</span></span><br/> |
| [<span data-ttu-id="8f828-125">**SetColorDepth**</span><span class="sxs-lookup"><span data-stu-id="8f828-125">**SetColorDepth**</span></span>](win32-tsclientsetting-setcolordepth.md)             | <span data-ttu-id="8f828-126">Establece la propiedad **colorDepth** .</span><span class="sxs-lookup"><span data-stu-id="8f828-126">Sets the **ColorDepth** property.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="8f828-127">**SetColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="8f828-127">**SetColorDepthPolicy**</span></span>](win32-tsclientsetting-setcolordepthpolicy.md) | <span data-ttu-id="8f828-128">Establece la propiedad **ColorDepthPolicy** .</span><span class="sxs-lookup"><span data-stu-id="8f828-128">Sets the **ColorDepthPolicy** property.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="8f828-129">**SetMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="8f828-129">**SetMaxMonitors**</span></span>](setmaxmonitors-win32-tsclientsetting.md)           | <span data-ttu-id="8f828-130">Establece la propiedad **MaxMonitors** .</span><span class="sxs-lookup"><span data-stu-id="8f828-130">Sets the **MaxMonitors** property.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="8f828-131">**SetMaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="8f828-131">**SetMaxXResolution**</span></span>](setmaxxresolution-win32-tsclientsetting.md)     | <span data-ttu-id="8f828-132">Establece la propiedad **MaxXResolution** .</span><span class="sxs-lookup"><span data-stu-id="8f828-132">Sets the **MaxXResolution** property.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="8f828-133">**SetMaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="8f828-133">**SetMaxYResolution**</span></span>](setmaxyresolution-win32-tsclientsetting.md)     | <span data-ttu-id="8f828-134">Establece la propiedad **MaxYResolution** .</span><span class="sxs-lookup"><span data-stu-id="8f828-134">Sets the **MaxYResolution** property.</span></span><br/>                                                                                                             |



 

### <a name="properties"></a><span data-ttu-id="8f828-135">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f828-135">Properties</span></span>

<span data-ttu-id="8f828-136">La **clase \_ TSClientSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8f828-136">The **Win32\_TSClientSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f828-137">**AdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="8f828-137">**AdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f828-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f828-140">Especifica si se habilitan los gráficos RemoteFX avanzados para RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f828-140">Specifies whether to enable advanced RemoteFX graphics for RemoteApp.</span></span>

<span data-ttu-id="8f828-141">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2012 R2 y Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="8f828-141">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-142"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-142"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-143">Los gráficos avanzados están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="8f828-143">Advanced graphics are disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-144"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-144"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-145">Los gráficos avanzados están habilitados.</span><span class="sxs-lookup"><span data-stu-id="8f828-145">Advanced graphics are enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-146">**AllowDwm**</span><span class="sxs-lookup"><span data-stu-id="8f828-146">**AllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-149">Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8f828-149">This property is not available.</span></span>

<span data-ttu-id="8f828-150">\* \* Windows 7 y Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="8f828-150">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="8f828-151">Especifica si se debe habilitar o deshabilitar la composición de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="8f828-151">Specifies whether to enable or disable remote desktop composition.</span></span> <span data-ttu-id="8f828-152">Cero deshabilitará la composición de escritorio remoto y un valor distinto de cero lo habilitará.</span><span class="sxs-lookup"><span data-stu-id="8f828-152">Zero will disable remote desktop composition and a nonzero value will enable it.</span></span>

<span data-ttu-id="8f828-153">Use el método [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) para modificar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f828-153">Use the [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) method to modify this property.</span></span>

</dd> <dt>

<span data-ttu-id="8f828-154">**AudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="8f828-154">**AudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-155">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-157">Especifica si se permite la redirección de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="8f828-157">Specifies whether to allow audio capture redirection.</span></span>

<span data-ttu-id="8f828-158">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f828-158">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-159">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-159">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-160">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-160">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-161">**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-161">**AudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-164">Especifica si la asignación de audio está deshabilitada o habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-164">Specifies whether audio mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-165"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-165"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-166">La asignación de audio está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-166">Audio mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-167"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-167"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-168">La asignación de audio está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-168">Audio mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-169">**AVC444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="8f828-169">**AVC444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-171">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f828-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f828-172">Especifica si se prefiere el modo AVC444.</span><span class="sxs-lookup"><span data-stu-id="8f828-172">Specifies whether AVC444 mode is preferred.</span></span>

<span data-ttu-id="8f828-173">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 10 o Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8f828-173">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-174">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-174">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-175">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-175">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8f828-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8f828-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f828-179">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f828-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f828-180">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="8f828-180">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8f828-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f828-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f828-182">**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-182">**ClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-183">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-185">Especifica si la asignación del Portapapeles está deshabilitada o habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-185">Specifies whether clipboard mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-186"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-186"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-187">La asignación del Portapapeles está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-187">Clipboard mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-188"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-188"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-189">La asignación del Portapapeles está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-189">Clipboard mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-190">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="8f828-190">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-191">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-193">Especifica la profundidad de color.</span><span class="sxs-lookup"><span data-stu-id="8f828-193">Specifies the color depth.</span></span> <span data-ttu-id="8f828-194">Para obtener los valores posibles, vea el método [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) .</span><span class="sxs-lookup"><span data-stu-id="8f828-194">For possible values, see the [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) method.</span></span>

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span data-ttu-id="8f828-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bits** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span data-ttu-id="8f828-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bits** (2)</span><span class="sxs-lookup"><span data-stu-id="8f828-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span data-ttu-id="8f828-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bits** (3)</span><span class="sxs-lookup"><span data-stu-id="8f828-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span data-ttu-id="8f828-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bits** (4)</span><span class="sxs-lookup"><span data-stu-id="8f828-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bit** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span data-ttu-id="8f828-199"><span id="32_bit"></span><span id="32_BIT"></span>**bit 32** (5)</span><span class="sxs-lookup"><span data-stu-id="8f828-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 bit** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-200">**ColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="8f828-200">**ColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-201">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-203">Especifica si se va a invalidar la configuración de color máxima del usuario.</span><span class="sxs-lookup"><span data-stu-id="8f828-203">Specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-204"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-204"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-205">No invalide la Directiva del usuario.</span><span class="sxs-lookup"><span data-stu-id="8f828-205">Do not override the user's policy.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-206"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-206"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-207">Invalide la Directiva del usuario.</span><span class="sxs-lookup"><span data-stu-id="8f828-207">Override the user's policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-208">**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-208">**COMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-209">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-211">Especifica si la asignación de puertos COM está deshabilitada o habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-211">Specifies whether COM port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-212"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-212"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-213">La asignación de puertos COM está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-213">COM port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-214"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-214"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-215">La asignación de puertos COM está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-215">COM port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-216">**ConnectClientDrivesAtLogon**</span><span class="sxs-lookup"><span data-stu-id="8f828-216">**ConnectClientDrivesAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-217">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-219">Especifica si las unidades del cliente se conectarán automáticamente durante el proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8f828-219">Specifies whether the client's drives will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-220"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-220"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-221">Las unidades no se conectarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8f828-221">Drives will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-222"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-222"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-223">Las unidades se conectarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8f828-223">Drives will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-224">**ConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="8f828-224">**ConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-225">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f828-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f828-227">La Directiva que el servidor utiliza para recuperar la configuración de conexión del usuario.</span><span class="sxs-lookup"><span data-stu-id="8f828-227">The policy the server uses to retrieve the user connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="8f828-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-229">La configuración de conexión del usuario está en vigor.</span><span class="sxs-lookup"><span data-stu-id="8f828-229">The user's connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="8f828-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Invalidación de servidor** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-231">El servidor invalida la configuración de conexión del usuario.</span><span class="sxs-lookup"><span data-stu-id="8f828-231">The user's connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-232">**ConnectPrinterAtLogon**</span><span class="sxs-lookup"><span data-stu-id="8f828-232">**ConnectPrinterAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-233">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-235">Especifica si todas las impresoras locales asignadas del cliente se conectarán automáticamente durante el proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8f828-235">Specifies whether all mapped local printers of the client will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-236"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-236"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-237">Las impresoras locales no se conectarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8f828-237">Local printers will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-238"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-238"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-239">Las impresoras locales se conectarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8f828-239">Local printers will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-240">**DefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="8f828-240">**DefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-241">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-243">Especifica si los trabajos de impresión se enviarán automáticamente a la impresora local del cliente.</span><span class="sxs-lookup"><span data-stu-id="8f828-243">Specifies whether print jobs will be automatically sent to the client's local printer.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-244"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-244"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-245">Los trabajos de impresión no se enviarán automáticamente a la impresora local del cliente.</span><span class="sxs-lookup"><span data-stu-id="8f828-245">Print jobs are not to be automatically sent to the client's local printer.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-246"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-246"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-247">Los trabajos de impresión se enviarán automáticamente a la impresora local del cliente.</span><span class="sxs-lookup"><span data-stu-id="8f828-247">Print jobs are to be automatically sent to the client's local printer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-248">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f828-248">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8f828-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-251">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8f828-251">Description of the object.</span></span>

<span data-ttu-id="8f828-252">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f828-252">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f828-253">**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-253">**DriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-254">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-256">Especifica si la asignación de unidad está deshabilitada o habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-256">Specifies whether drive mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-257"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-257"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-258">La asignación de unidades está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-258">Drive mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-259"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-259"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-260">La asignación de unidades está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-260">Drive mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-261">**EncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="8f828-261">**EncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-262">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-263">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f828-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f828-264">Especifica la calidad de la imagen para la experiencia de RDP.</span><span class="sxs-lookup"><span data-stu-id="8f828-264">Specifies the image quality for RDP experience.</span></span>

<span data-ttu-id="8f828-265">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-265">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

<span data-ttu-id="8f828-266">sin **pérdida** de (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-266">**lossless** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="8f828-267">**alto** (2)</span><span class="sxs-lookup"><span data-stu-id="8f828-267">**high** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="8f828-268">**medio** (3)</span><span class="sxs-lookup"><span data-stu-id="8f828-268">**medium** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-269">**HardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="8f828-269">**HardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-270">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-271">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f828-271">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f828-272">Especifica si el servidor host de sesión de escritorio remoto usa el procesador de gráficos de hardware como adaptador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8f828-272">Specifies whether the RD Session Host server uses the hardware graphics renderer as the default adapter.</span></span>

<span data-ttu-id="8f828-273">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-273">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-274">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-274">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-275">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-275">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f828-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-277">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f828-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f828-279">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="8f828-279">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8f828-280">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="8f828-280">The date the object was installed.</span></span> <span data-ttu-id="8f828-281">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="8f828-281">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8f828-282">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f828-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f828-283">**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-283">**LPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-284">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-286">Especifica si la asignación de puerto LPT está deshabilitada o habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-286">Specifies whether LPT port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-287"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-287"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-288">La asignación de puertos LPT está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-288">LPT port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-289"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-289"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-290">La asignación de puerto LPT está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-290">LPT port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-291">**MaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="8f828-291">**MaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-292">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-294">Número máximo de monitores admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="8f828-294">The maximum number of monitors supported by the server.</span></span> <span data-ttu-id="8f828-295">Use el método [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) para modificar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f828-295">Use the [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="8f828-296">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f828-296">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8f828-297">**MaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="8f828-297">**MaxXResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-298">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-298">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-300">La resolución X máxima admitida por el servidor.</span><span class="sxs-lookup"><span data-stu-id="8f828-300">The maximum X resolution supported by the server.</span></span> <span data-ttu-id="8f828-301">Use el método [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) para modificar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f828-301">Use the [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="8f828-302">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f828-302">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8f828-303">**MaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="8f828-303">**MaxYResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-304">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-304">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-306">Resolución máxima Y admitida por el servidor.</span><span class="sxs-lookup"><span data-stu-id="8f828-306">The maximum Y resolution supported by the server.</span></span> <span data-ttu-id="8f828-307">Use el método [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) para modificar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f828-307">Use the [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="8f828-308">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f828-308">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8f828-309">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8f828-309">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8f828-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-312">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="8f828-312">The name of the object.</span></span>

<span data-ttu-id="8f828-313">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f828-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f828-314">**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="8f828-314">**PNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-315">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-317">Especifica si se va a permitir el redireccionamiento Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="8f828-317">Specifies whether to allow Plug and Play redirection.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-318"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-318"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-319">Permite el redireccionamiento de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="8f828-319">Allow Plug and Play redirection.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-320"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-320"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-321">No permita el redireccionamiento Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="8f828-321">Do not allow Plug and Play redirection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-322">**PolicyAdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="8f828-322">**PolicyAdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-323">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-325">Indica si la propiedad **AdvancedRemoteAppGraphics** está configurada por el servidor o la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8f828-325">Indicates whether the **AdvancedRemoteAppGraphics** property is configured by the server or group policy.</span></span>

<span data-ttu-id="8f828-326">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2012 R2 y Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="8f828-326">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span data-ttu-id="8f828-327">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-327">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-328">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-328">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-329">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-329">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-330">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-330">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-331">**PolicySourceAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="8f828-331">**PolicySourceAllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-332">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-334">Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8f828-334">This property is not available.</span></span>

<span data-ttu-id="8f828-335">\* \* Windows 7 y Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="8f828-335">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="8f828-336">Indica si la propiedad **AllowDwm** está configurada por el servidor o la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8f828-336">Indicates whether the **AllowDwm** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="8f828-337">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-337">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-338">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-338">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-339">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-339">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-340">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-340">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-341">**PolicySourceAudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="8f828-341">**PolicySourceAudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-342">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-344">Indica si la propiedad **AudioCaptureRedir** está configurada por el servidor o la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8f828-344">Indicates whether the **AudioCaptureRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="8f828-345">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f828-345">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="8f828-346">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-346">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-347">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-347">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-348">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-348">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-349">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-349">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-350">**PolicySourceAudioMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-350">**PolicySourceAudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-351">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-353">Indica si la propiedad **AudioMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f828-353">Indicates whether the **AudioMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f828-354">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-354">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-355">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-355">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-356">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-356">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-357">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-357">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-358">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-358">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-359">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-359">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-360">**PolicySourceAvc444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="8f828-360">**PolicySourceAvc444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-361">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-363">Indica cómo se configura la propiedad **AVC444ModePreferredis** .</span><span class="sxs-lookup"><span data-stu-id="8f828-363">Indicates how the **AVC444ModePreferredis** property is configured.</span></span>

<span data-ttu-id="8f828-364">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 10 o Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8f828-364">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span data-ttu-id="8f828-365">0</span><span class="sxs-lookup"><span data-stu-id="8f828-365">0</span></span>
</dt> <dd>

<span data-ttu-id="8f828-366">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-366">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-367">1</span><span class="sxs-lookup"><span data-stu-id="8f828-367">1</span></span>
</dt> <dd>

<span data-ttu-id="8f828-368">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-368">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-369">**PolicySourceClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-369">**PolicySourceClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-370">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-372">Indica si la propiedad **ClipboardMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f828-372">Indicates whether the **ClipboardMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f828-373">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-373">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-374">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-374">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-375">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-375">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-376">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-376">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-377">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-377">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-378">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-378">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-379">**PolicySourceColorDepth**</span><span class="sxs-lookup"><span data-stu-id="8f828-379">**PolicySourceColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-380">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-382">Indica si la propiedad **colorDepth** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f828-382">Indicates whether the **ColorDepth** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f828-383">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-383">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-384">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-384">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-385">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-385">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-386">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-386">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-387">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-387">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-388">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-388">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-389">**PolicySourceColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="8f828-389">**PolicySourceColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-390">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-392">Indica si la propiedad **ColorDepthPolicy** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f828-392">Indicates whether the **ColorDepthPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f828-393">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-393">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-394">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-394">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-395">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-395">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-396">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-396">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-397">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-397">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-398">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-398">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-399">**PolicySourceCOMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-399">**PolicySourceCOMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-400">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-400">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-401">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-402">Indica si la propiedad **COMPortMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f828-402">Indicates whether the **COMPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f828-403">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-403">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-404">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-404">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-405">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-405">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-406">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-406">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-407">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-407">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-408">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-408">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-409">**PolicySourceDefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="8f828-409">**PolicySourceDefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-410">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-412">Indica si la propiedad **DefaultToClientPrinter** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f828-412">Indicates whether the **DefaultToClientPrinter** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f828-413">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-413">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-414">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-414">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-415">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-415">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-416">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-416">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-417">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-417">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-418">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-418">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-419">**PolicySourceDriveMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-419">**PolicySourceDriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-420">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-422">Indica si la propiedad **DriveMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f828-422">Indicates whether the **DriveMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f828-423">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-424">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-426">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-426">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-427">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-427">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-428">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-428">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-429">**PolicySourceEncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="8f828-429">**PolicySourceEncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-430">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-432">Indica cómo se configura el **EncodeImageQualityi** .</span><span class="sxs-lookup"><span data-stu-id="8f828-432">Indicates how the **EncodeImageQualityi** is configured.</span></span>

<span data-ttu-id="8f828-433">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-433">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f828-434">0</span><span class="sxs-lookup"><span data-stu-id="8f828-434">0</span></span>
</dt> <dd>

<span data-ttu-id="8f828-435">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-435">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-436">1</span><span class="sxs-lookup"><span data-stu-id="8f828-436">1</span></span>
</dt> <dd>

<span data-ttu-id="8f828-437">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-437">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-438">**PolicySourceHardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="8f828-438">**PolicySourceHardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-439">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-441">Indica cómo se configura el **HardwareGraphicsAdapter** .</span><span class="sxs-lookup"><span data-stu-id="8f828-441">Indicates how the **HardwareGraphicsAdapter** is configured.</span></span>

<span data-ttu-id="8f828-442">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-442">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f828-443">0</span><span class="sxs-lookup"><span data-stu-id="8f828-443">0</span></span>
</dt> <dd>

<span data-ttu-id="8f828-444">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-444">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-445">1</span><span class="sxs-lookup"><span data-stu-id="8f828-445">1</span></span>
</dt> <dd>

<span data-ttu-id="8f828-446">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-446">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-447">**PolicySourceLPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-447">**PolicySourceLPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-448">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-448">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-450">Indica si la propiedad **LPTPortMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f828-450">Indicates whether the **LPTPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f828-451">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-451">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-452">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-452">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-453">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-453">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-454">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-454">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-455">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-455">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-456">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-456">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-457">**PolicySourceMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="8f828-457">**PolicySourceMaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-458">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-458">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-459">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-460">Indica si la propiedad **MaxMonitors** está configurada por el servidor, la Directiva de grupo o el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8f828-460">Indicates whether the **MaxMonitors** property is configured by the server, group policy, or default.</span></span>

<dt>

<span data-ttu-id="8f828-461">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-461">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-462">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-462">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-463">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-463">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-464">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-464">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-465">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-465">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-466">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-466">Default</span></span>

</dd> </dl>

<span data-ttu-id="8f828-467">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f828-467">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8f828-468">**PolicySourceMaxResolution**</span><span class="sxs-lookup"><span data-stu-id="8f828-468">**PolicySourceMaxResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-469">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-469">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-471">Indica si las propiedades **MaxXResolution** y **MaxYResolution** están configuradas por el servidor, la Directiva de grupo o el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8f828-471">Indicates whether the **MaxXResolution** and **MaxYResolution** properties are configured by the server, group policy, or default.</span></span>

<span data-ttu-id="8f828-472">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f828-472">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="8f828-473">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-473">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-474">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-474">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-475">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-475">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-476">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-476">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-477">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-477">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-478">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-478">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-479">**PolicySourcePNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="8f828-479">**PolicySourcePNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-480">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-482">Indica si la propiedad **PNPRedirection** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8f828-482">Indicates whether the **PNPRedirection** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="8f828-483">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-483">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-484">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-484">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-485">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-485">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-486">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-486">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-487">**PolicySourceRemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="8f828-487">**PolicySourceRemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-488">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-489">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-490">Indica cómo se configura el **RemoteSessionProfile** .</span><span class="sxs-lookup"><span data-stu-id="8f828-490">Indicates how the **RemoteSessionProfile** is configured.</span></span>

<span data-ttu-id="8f828-491">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-491">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is unavailable prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f828-492">0</span><span class="sxs-lookup"><span data-stu-id="8f828-492">0</span></span>
</dt> <dd>

<span data-ttu-id="8f828-493">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-493">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-494">1</span><span class="sxs-lookup"><span data-stu-id="8f828-494">1</span></span>
</dt> <dd>

<span data-ttu-id="8f828-495">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-495">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-496">**PolicySourceSelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="8f828-496">**PolicySourceSelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-497">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-497">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-498">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-499">Indica cómo se configura la propiedad **SelectNetworkDetect** .</span><span class="sxs-lookup"><span data-stu-id="8f828-499">Indicates how the property **SelectNetworkDetect** is configured.</span></span>

<span data-ttu-id="8f828-500">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-500">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f828-501">0</span><span class="sxs-lookup"><span data-stu-id="8f828-501">0</span></span>
</dt> <dd>

<span data-ttu-id="8f828-502">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-502">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-503">1</span><span class="sxs-lookup"><span data-stu-id="8f828-503">1</span></span>
</dt> <dd>

<span data-ttu-id="8f828-504">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-504">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-505">**PolicySourceSelectTransport**</span><span class="sxs-lookup"><span data-stu-id="8f828-505">**PolicySourceSelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-506">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-508">Indica cómo se configura la propiedad **SelectTransport** .</span><span class="sxs-lookup"><span data-stu-id="8f828-508">Indicates how the property **SelectTransport** is configured.</span></span>

<span data-ttu-id="8f828-509">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-509">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f828-510">0</span><span class="sxs-lookup"><span data-stu-id="8f828-510">0</span></span>
</dt> <dd>

<span data-ttu-id="8f828-511">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-511">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-512">1</span><span class="sxs-lookup"><span data-stu-id="8f828-512">1</span></span>
</dt> <dd>

<span data-ttu-id="8f828-513">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-513">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-514">**PolicySourceVideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="8f828-514">**PolicySourceVideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-515">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-515">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-516">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-517">Indica si la propiedad **VideoPlaybackRedir** está configurada por el servidor o la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8f828-517">Indicates whether the **VideoPlaybackRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="8f828-518">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f828-518">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="8f828-519">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-519">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-520">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-520">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-521">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-521">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-522">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-522">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-523">**PolicySourceWindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-523">**PolicySourceWindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-524">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-525">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-526">Indica si la propiedad **WindowsPrinterMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f828-526">Indicates whether the **WindowsPrinterMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f828-527">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="8f828-527">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-528">Servidor</span><span class="sxs-lookup"><span data-stu-id="8f828-528">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f828-529">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f828-529">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-530">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="8f828-530">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f828-531">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f828-531">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f828-532">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="8f828-532">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-533">**RemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="8f828-533">**RemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-534">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-534">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-535">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f828-535">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f828-536">Especifica el perfil para la experiencia de RDP.</span><span class="sxs-lookup"><span data-stu-id="8f828-536">Specifies the profile for the RDP experience.</span></span>

<span data-ttu-id="8f828-537">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-537">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="scale"></span><span id="SCALE"></span>

<span data-ttu-id="8f828-538">**escala** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-538">**scale** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

<span data-ttu-id="8f828-539">**experiencia** (2)</span><span class="sxs-lookup"><span data-stu-id="8f828-539">**experience** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

<span data-ttu-id="8f828-540">**ancho de banda** (3)</span><span class="sxs-lookup"><span data-stu-id="8f828-540">**bandwidth** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-541">**SelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="8f828-541">**SelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-542">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-543">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f828-543">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f828-544">Especifica si se utiliza la detección de redes.</span><span class="sxs-lookup"><span data-stu-id="8f828-544">Specifies whether network detection is used.</span></span>

<span data-ttu-id="8f828-545">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-545">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f828-546">0</span><span class="sxs-lookup"><span data-stu-id="8f828-546">0</span></span>
</dt> <dd>

<span data-ttu-id="8f828-547">se usa en tiempo de conexión y en estado estable.</span><span class="sxs-lookup"><span data-stu-id="8f828-547">used at connect time and in steady state.</span></span>

</dd> <dt>

<span data-ttu-id="8f828-548">1</span><span class="sxs-lookup"><span data-stu-id="8f828-548">1</span></span>
</dt> <dd>

<span data-ttu-id="8f828-549">deshabilitado en tiempo de conexión</span><span class="sxs-lookup"><span data-stu-id="8f828-549">disabled at connect time</span></span>

</dd> <dt>

<span data-ttu-id="8f828-550">2</span><span class="sxs-lookup"><span data-stu-id="8f828-550">2</span></span>
</dt> <dd>

<span data-ttu-id="8f828-551">deshabilitado en estado estable</span><span class="sxs-lookup"><span data-stu-id="8f828-551">disabled in steady state</span></span>

</dd> <dt>

<span data-ttu-id="8f828-552">3</span><span class="sxs-lookup"><span data-stu-id="8f828-552">3</span></span>
</dt> <dd>

<span data-ttu-id="8f828-553">deshabilitado en tiempo de conexión y en estado estable.</span><span class="sxs-lookup"><span data-stu-id="8f828-553">disabled at connect time and in steady state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-554">**SelectTransport**</span><span class="sxs-lookup"><span data-stu-id="8f828-554">**SelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-555">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-555">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-556">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f828-556">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f828-557">Especifica qué protocolos de transporte se pueden usar para el acceso RDP al servidor.</span><span class="sxs-lookup"><span data-stu-id="8f828-557">Specifies which transport protocols can be used for RDP access to server.</span></span>

<span data-ttu-id="8f828-558">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f828-558">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f828-559">0</span><span class="sxs-lookup"><span data-stu-id="8f828-559">0</span></span>
</dt> <dd>

<span data-ttu-id="8f828-560">Use UDP y TCP.</span><span class="sxs-lookup"><span data-stu-id="8f828-560">Use both UDP and TCP.</span></span>

</dd> <dt>

<span data-ttu-id="8f828-561">1</span><span class="sxs-lookup"><span data-stu-id="8f828-561">1</span></span>
</dt> <dd>

<span data-ttu-id="8f828-562">Usar solo TCP.</span><span class="sxs-lookup"><span data-stu-id="8f828-562">Use only TCP.</span></span>

</dd> <dt>

<span data-ttu-id="8f828-563">2</span><span class="sxs-lookup"><span data-stu-id="8f828-563">2</span></span>
</dt> <dd>

<span data-ttu-id="8f828-564">Use UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="8f828-564">Use either UDP or TCP.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-565">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8f828-565">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-566">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8f828-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-567">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f828-568">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8f828-568">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8f828-569">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8f828-569">Current status of the object.</span></span> <span data-ttu-id="8f828-570">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="8f828-570">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8f828-571">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="8f828-571">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8f828-572">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="8f828-572">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8f828-573">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="8f828-573">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8f828-574">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="8f828-574">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8f828-575">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f828-575">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8f828-576">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="8f828-576">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f828-577">("Error")</span><span class="sxs-lookup"><span data-stu-id="8f828-577">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f828-578">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="8f828-578">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f828-579">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="8f828-579">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f828-580">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="8f828-580">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f828-581">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="8f828-581">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f828-582">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="8f828-582">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f828-583">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="8f828-583">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-584">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="8f828-584">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-585">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8f828-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-586">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-587">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="8f828-587">The name of the terminal.</span></span>

<span data-ttu-id="8f828-588">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="8f828-588">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f828-589">**VideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="8f828-589">**VideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-590">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-591">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-592">Especifica si se permite la redirección de reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8f828-592">Specifies whether to allow video playback redirection.</span></span>

<span data-ttu-id="8f828-593">**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f828-593">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-594">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-594">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-595">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-595">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f828-596">**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="8f828-596">**WindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f828-597">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f828-597">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f828-598">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f828-598">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f828-599">Especifica si la asignación de impresora está deshabilitada o habilitada para la ventana del cliente.</span><span class="sxs-lookup"><span data-stu-id="8f828-599">Specifies whether printer mapping is disabled or enabled for the client's window.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f828-600"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f828-600"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-601">La asignación de impresora está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-601">Printer mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f828-602"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f828-602"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f828-603">La asignación de impresora está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-603">Printer mapping is disabled.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f828-604">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f828-604">Remarks</span></span>

<span data-ttu-id="8f828-605">Tenga en cuenta que una estación de ventana asociada a la sesión de consola no puede tener acceso a los métodos y las propiedades de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8f828-605">Be aware that a window station associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="8f828-606">Si se realiza un intento de hacerlo especificando "Console" como el valor de la propiedad **TerminalName** , los métodos de este objeto devolverán **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="8f828-606">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="8f828-607">Este código de error también se devuelve si una estación de ventana intenta llamar a métodos de este objeto para agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="8f828-607">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="8f828-608">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="8f828-608">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="8f828-609">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="8f828-609">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="8f828-610">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de seis.</span><span class="sxs-lookup"><span data-stu-id="8f828-610">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="8f828-611">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="8f828-611">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="8f828-612">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8f828-612">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8f828-613">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8f828-613">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8f828-614">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="8f828-614">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8f828-615">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8f828-615">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f828-616">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f828-616">Requirements</span></span>



| <span data-ttu-id="8f828-617">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f828-617">Requirement</span></span> | <span data-ttu-id="8f828-618">Value</span><span class="sxs-lookup"><span data-stu-id="8f828-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f828-619">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f828-619">Minimum supported client</span></span><br/> | <span data-ttu-id="8f828-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f828-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f828-621">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f828-621">Minimum supported server</span></span><br/> | <span data-ttu-id="8f828-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f828-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f828-623">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8f828-623">Namespace</span></span><br/>                | <span data-ttu-id="8f828-624">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8f828-624">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8f828-625">MOF</span><span class="sxs-lookup"><span data-stu-id="8f828-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f828-626"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f828-626"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f828-627">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f828-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f828-628"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f828-628"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f828-629">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f828-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f828-630">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="8f828-630">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="8f828-631">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="8f828-631">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="8f828-632">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8f828-632">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

