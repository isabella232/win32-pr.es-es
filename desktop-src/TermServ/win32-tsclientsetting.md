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
# <a name="win32_tsclientsetting-class"></a>\_Clase Win32 TSClientSetting

La clase WMI **\_ TSClientSetting de Win32** define los valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) relacionada con la Directiva de conexión.

La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético. Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La **clase \_ TSClientSetting de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TSClientSetting** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionSettings**](win32-tsclientsetting-connectionsettings.md)   | Establece las propiedades **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon** y **DefaultToClientPrinter** de esta clase.<br/>                      |
| [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md)                 | No se admite.<br/> **Windows 7 y Windows Server 2008 R2:** Establece la propiedad **AllowDwm** .<br/>                                               |
| [**SetClientProperty**](win32-tsclientsetting-setclientproperty.md)     | Establece la propiedad **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** o **WindowsPrinterMapping** .<br/> |
| [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md)             | Establece la propiedad **colorDepth** .<br/>                                                                                                                 |
| [**SetColorDepthPolicy**](win32-tsclientsetting-setcolordepthpolicy.md) | Establece la propiedad **ColorDepthPolicy** .<br/>                                                                                                           |
| [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md)           | Establece la propiedad **MaxMonitors** .<br/>                                                                                                                |
| [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md)     | Establece la propiedad **MaxXResolution** .<br/>                                                                                                             |
| [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md)     | Establece la propiedad **MaxYResolution** .<br/>                                                                                                             |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSClientSetting de Win32** tiene estas propiedades.

<dl> <dt>

**AdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se habilitan los gráficos RemoteFX avanzados para RemoteApp.

**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2012 R2 y Windows 8.1.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Los gráficos avanzados están deshabilitados.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Los gráficos avanzados están habilitados.

</dd> </dl>

</dd> <dt>

**AllowDwm**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad no está disponible.

* * Windows 7 y Windows Server 2008 R2: * *

Especifica si se debe habilitar o deshabilitar la composición de escritorio remoto. Cero deshabilitará la composición de escritorio remoto y un valor distinto de cero lo habilitará.

Use el método [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) para modificar esta propiedad.

</dd> <dt>

**AudioCaptureRedir**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se permite la redirección de captura de audio.

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**AudioMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la asignación de audio está deshabilitada o habilitada.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La asignación de audio está habilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La asignación de audio está deshabilitada.

</dd> </dl>

</dd> <dt>

**AVC444ModePreferred**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se prefiere el modo AVC444.

**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 10 o Windows Server 2016.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descripción breve (cadena de una línea) del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**ClipboardMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la asignación del Portapapeles está deshabilitada o habilitada.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La asignación del Portapapeles está habilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La asignación del Portapapeles está deshabilitada.

</dd> </dl>

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la profundidad de color. Para obtener los valores posibles, vea el método [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) .

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span id="8_bit"></span><span id="8_BIT"></span>**8 bits** (1)


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span id="15_bit"></span><span id="15_BIT"></span>**15 bits** (2)


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span id="16_bit"></span><span id="16_BIT"></span>**16 bits** (3)


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span id="24_bit"></span><span id="24_BIT"></span>**24 bits** (4)


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span id="32_bit"></span><span id="32_BIT"></span>**bit 32** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ColorDepthPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se va a invalidar la configuración de color máxima del usuario.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

No invalide la Directiva del usuario.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Invalide la Directiva del usuario.

</dd> </dl>

</dd> <dt>

**COMPortMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la asignación de puertos COM está deshabilitada o habilitada.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La asignación de puertos COM está habilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La asignación de puertos COM está deshabilitada.

</dd> </dl>

</dd> <dt>

**ConnectClientDrivesAtLogon**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si las unidades del cliente se conectarán automáticamente durante el proceso de inicio de sesión.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Las unidades no se conectarán automáticamente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Las unidades se conectarán automáticamente.

</dd> </dl>

</dd> <dt>

**ConnectionPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La Directiva que el servidor utiliza para recuperar la configuración de conexión del usuario.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (0)


</dt> <dd>

La configuración de conexión del usuario está en vigor.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Invalidación de servidor** (1)


</dt> <dd>

El servidor invalida la configuración de conexión del usuario.

</dd> </dl>

</dd> <dt>

**ConnectPrinterAtLogon**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si todas las impresoras locales asignadas del cliente se conectarán automáticamente durante el proceso de inicio de sesión.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Las impresoras locales no se conectarán automáticamente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Las impresoras locales se conectarán automáticamente.

</dd> </dl>

</dd> <dt>

**DefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si los trabajos de impresión se enviarán automáticamente a la impresora local del cliente.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Los trabajos de impresión no se enviarán automáticamente a la impresora local del cliente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Los trabajos de impresión se enviarán automáticamente a la impresora local del cliente.

</dd> </dl>

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**DriveMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la asignación de unidad está deshabilitada o habilitada.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La asignación de unidades está habilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La asignación de unidades está deshabilitada.

</dd> </dl>

</dd> <dt>

**EncodeImageQuality**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica la calidad de la imagen para la experiencia de RDP.

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

sin **pérdida** de (1)


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

**alto** (2)


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

**medio** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si el servidor host de sesión de escritorio remoto usa el procesador de gráficos de hardware como adaptador predeterminado.

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Fecha en que se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**LPTPortMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la asignación de puerto LPT está deshabilitada o habilitada.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La asignación de puertos LPT está habilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La asignación de puerto LPT está deshabilitada.

</dd> </dl>

</dd> <dt>

**MaxMonitors**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número máximo de monitores admitidos por el servidor. Use el método [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) para modificar esta propiedad.

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.

</dd> <dt>

**MaxXResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La resolución X máxima admitida por el servidor. Use el método [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) para modificar esta propiedad.

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.

</dd> <dt>

**MaxYResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Resolución máxima Y admitida por el servidor. Use el método [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) para modificar esta propiedad.

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**PNPRedirection**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se va a permitir el redireccionamiento Plug and Play.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Permite el redireccionamiento de Plug and Play.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

No permita el redireccionamiento Plug and Play.

</dd> </dl>

</dd> <dt>

**PolicyAdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **AdvancedRemoteAppGraphics** está configurada por el servidor o la Directiva de grupo.

**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2012 R2 y Windows 8.1.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceAllowDwm**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad no está disponible.

* * Windows 7 y Windows Server 2008 R2: * *

Indica si la propiedad **AllowDwm** está configurada por el servidor o la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceAudioCaptureRedir**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **AudioCaptureRedir** está configurada por el servidor o la Directiva de grupo.

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceAudioMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **AudioMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceAvc444ModePreferred**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se configura la propiedad **AVC444ModePreferredis** .

**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 10 o Windows Server 2016.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceClipboardMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **ClipboardMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepth**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **colorDepth** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepthPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **ColorDepthPolicy** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceCOMPortMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **COMPortMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceDefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **DefaultToClientPrinter** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceDriveMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **DriveMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceEncodeImageQuality**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se configura el **EncodeImageQualityi** .

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceHardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se configura el **HardwareGraphicsAdapter** .

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceLPTPortMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **LPTPortMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceMaxMonitors**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **MaxMonitors** está configurada por el servidor, la Directiva de grupo o el valor predeterminado.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.

</dd> <dt>

**PolicySourceMaxResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si las propiedades **MaxXResolution** y **MaxYResolution** están configuradas por el servidor, la Directiva de grupo o el valor predeterminado.

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourcePNPRedirection**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **PNPRedirection** está configurada por el servidor o por la Directiva de grupo.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceRemoteSessionProfile**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se configura el **RemoteSessionProfile** .

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceSelectNetworkDetect**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se configura la propiedad **SelectNetworkDetect** .

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceSelectTransport**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se configura la propiedad **SelectTransport** .

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceVideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **VideoPlaybackRedir** está configurada por el servidor o la Directiva de grupo.

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceWindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **WindowsPrinterMapping** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**RemoteSessionProfile**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica el perfil para la experiencia de RDP.

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

<span id="scale"></span><span id="SCALE"></span>

**escala** (1)


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

**experiencia** (2)


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

**ancho de banda** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**SelectNetworkDetect**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se utiliza la detección de redes.

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

se usa en tiempo de conexión y en estado estable.

</dd> <dt>

1
</dt> <dd>

deshabilitado en tiempo de conexión

</dd> <dt>

2
</dt> <dd>

deshabilitado en estado estable

</dd> <dt>

3
</dt> <dd>

deshabilitado en tiempo de conexión y en estado estable.

</dd> </dl>

</dd> <dt>

**SelectTransport**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica qué protocolos de transporte se pueden usar para el acceso RDP al servidor.

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible antes de Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Use UDP y TCP.

</dd> <dt>

1
</dt> <dd>

Usar solo TCP.

</dd> <dt>

2
</dt> <dd>

Use UDP o TCP.

</dd> </dl>

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Estado actual del objeto. Se pueden definir varios Estados operativos y no operativos. Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo). Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio". El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

<dt>



 ("Correcto")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconocido")


</dt> <dd></dd> <dt>



 ("Pred FAIL")


</dt> <dd></dd> <dt>



 ("Iniciando")


</dt> <dd></dd> <dt>



 ("Deteniéndose")


</dt> <dd></dd> <dt>



 ("Servicio")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del terminal.

Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> <dt>

**VideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se permite la redirección de reproducción de vídeo.

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible antes de Windows Server 2008 R2 y Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**WindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la asignación de impresora está deshabilitada o habilitada para la ventana del cliente.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La asignación de impresora está habilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La asignación de impresora está deshabilitada.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que una estación de ventana asociada a la sesión de consola no puede tener acceso a los métodos y las propiedades de esta clase. Si se realiza un intento de hacerlo especificando "Console" como el valor de la propiedad **TerminalName** , los métodos de este objeto devolverán **WBEM \_ E \_ no \_ compatible**. Este código de error también se devuelve si una estación de ventana intenta llamar a métodos de este objeto para agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.

Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes. En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C. En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de seis.

En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Terminal Win32**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dt>

[**Configuración de CIM \_**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

