---
description: La clase VideoConfiguration de Win32 \_ no está activa. No devolverá ninguna instancia, ya que no hay ningún proveedor que la resalte.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Win32_VideoConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d951a8927458fa12398682ce63963dd71949d70e4db3a426dfc93ad14c78bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922625"
---
# <a name="win32_videoconfiguration-class"></a>Clase VideoConfiguration de Win32 \_

La **clase \_ VideoConfiguration de Win32** no está activa. No devolverá ninguna instancia, ya que no hay ningún proveedor que la resalte.

La **clase \_ VideoConfiguration de Win32** representa una configuración de un subsistema de vídeo. Esta clase ha quedado en desuso en favor de las propiedades contenidas en las clases [**\_ VideoController de Win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)y [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a>Miembros

La **clase \_ VideoConfiguration de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VideoConfiguration de Win32** tiene estas propiedades.

<dl> <dt>

**ActualColorResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per pixel")
</dt> </dl>

Indica la profundidad de color actual de la presentación del vídeo.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterChipType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ Info \| ChipType")
</dt> </dl>

Contiene el nombre del chip del adaptador.

Ejemplo: s3

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterCompatibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Especifica el nombre del fabricante del adaptador. Este nombre se puede usar para comparar la compatibilidad de este dispositivo con las necesidades del sistema informático.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterDACType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ Info \| DACType")
</dt> </dl>

Indica el nombre del chip digital a analógico (DAC) utilizado en el adaptador.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Contiene una descripción o un nombre descriptivo del adaptador de vídeo.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ Info \| VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Indica el tamaño de memoria del adaptador de vídeo.

Ejemplo: 16777216

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HARDWARE Description System \\ \\ \\ \\ \\ \\ DisplayController \\ \\ 0 \\ \\ Identifier")
</dt> </dl>

Indica el tipo de adaptador de vídeo.

Juego de caracteres: alfanumérico

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")
</dt> </dl>

Indica el número real de bits por píxel que representa la pantalla. Esto se puede escalar a la configuración de vídeo actual (representada por la propiedad ActualColorResolution) del usuario.

Ejemplo: 8

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**ColorPlanes**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| PLANES")
</dt> </dl>

Indica el número actual de planos de color usados en la presentación del vídeo. Un plano de color es otra manera de representar los colores de los píxeles. en lugar de asignar un único valor RGB a cada uno de los píxeles, los planos de color separan el gráfico en cada uno de los componentes de color primario (azul verde rojo) y los almacenan en sus propios planos. Esto permite mayores profundidades de color en sistemas de vídeo de 8 y 16 bits. Los sistemas gráficos presentes tienen el bitwidth lo suficientemente grande como para almacenar información de profundidad de color, lo que hace que solo sea necesario un plano de color.

Ejemplo: 1

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**ColorTableEntries**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")
</dt> </dl>

Indica el número de índices de color de una tabla de colores para una presentación de vídeo. Esta propiedad se usa si el dispositivo tiene una profundidad de color de no más de 8 bits por píxel. En el caso de los dispositivos con mayor profundidad de color, se devuelve -1.

Ejemplo: 256

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")
</dt> </dl>

Indica el número actual de lápices específicos del dispositivo. Un valor de 0xFFFFFFFF significa que el dispositivo no admite lápices. Los lápices se usan para dibujar líneas y los límites de objetos poligonales.

Ejemplo: 3

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**DriverDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ AdapterDescription \| DriverDate")
</dt> </dl>

Indica la fecha y hora en que se instaló el controlador de vídeo actual.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES")
</dt> </dl>

Indica el número actual de píxeles en la dirección horizontal (eje X) de la pantalla.

Ejemplo: 1024

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**InfFilename**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \| InfPath")
</dt> </dl>

Especifica la ruta de acceso al archivo .inf del controlador de vídeo.

Ejemplo: C: \\ controladores Windows \\ System32 \\

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**InfSection**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \| InfSection")
</dt> </dl>

Indica la sección del archivo .inf donde reside la información de vídeo de Win32.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**InstalledDisplayDrivers**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ Defaule \| drv")
</dt> </dl>

Indica el nombre del controlador de vídeo instalado.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**MonitorManufacturer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Indica el nombre del fabricante del dispositivo para mostrar.

Ejemplo: NEC

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**MonitorType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HARDWARE Description System \\ \\ \\ \\ \\ \\ MonitorPeripheral \\ \\ 0 \| Identifier")
</dt> </dl>

Indica el nombre del modelo del dispositivo para mostrar.

Ejemplo: NEC 5FGp

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Contiene un nombre de identificación para la clase de configuración de vídeo.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**PixelsPerXLogicalInch**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX")
</dt> </dl>

Indica el número de píxeles por pulgada lógica a lo largo del eje X (dirección horizontal) de la pantalla.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**PixelsPeryLogicalInch**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY")
</dt> </dl>

Indica el número de píxeles por pulgada lógica a lo largo del eje Y (dirección vertical) de la pantalla.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| DEVICEFRESH")
</dt> </dl>

Indica la frecuencia de actualización de la configuración del vídeo. Un valor de 0 o 1 indica que se usa una velocidad predeterminada.

Ejemplo: 72

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings.Interlaced")
</dt> </dl>

Indica si el dispositivo de pantalla está entrelazado.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

**No entrelazado** ("no entrelazado")


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

**Entrelazado** ("entrelazado")


</dt> <dd></dd> </dl>

</dd> <dt>

**ScreenHeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("mmmms")
</dt> </dl>

Especifica el alto de la pantalla física.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**ScreenWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de contexto de dispositivo Win32API \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milímetros")
</dt> </dl>

Especifica el ancho de la pantalla física.

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")
</dt> </dl>

Representa el número actual de entradas de índice de color reservadas para el uso del sistema. Este valor solo es válido para la configuración de presentación que usa una paleta indizada . Las paletas indizadas no se usan para profundidades de color superiores a 8 bits por píxel. Si la profundidad de color es superior a 8 bits por píxel, este valor se establece en **NULL.**

Ejemplo: 20

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES")
</dt> </dl>

Indica el número actual de píxeles en la dirección vertical (eje Y) de la pantalla.

Ejemplo: 768

Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> </dl>

 

 
