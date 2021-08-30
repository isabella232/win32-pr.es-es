---
description: La clase WMI PrinterConfiguration de Win32 \_ representa la configuración de un dispositivo de impresora. Esto incluye funcionalidades como la resolución, el color, las fuentes y la orientación.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Win32_PrinterConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6fccf35ec4cfc075d91daee4c2db6b6f23617d1cd2b8b4b6b249df6bfa5dec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971885"
---
# <a name="win32_printerconfiguration-class"></a>Clase PrinterConfiguration de Win32 \_

La **clase \_ WMI PrinterConfiguration** [de](../wmisdk/retrieving-a-class.md) Win32 representa la configuración de un dispositivo de impresora. Esto incluye funcionalidades como la resolución, el color, las fuentes y la orientación.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a>Miembros

La **clase \_ PrinterConfiguration de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PrinterConfiguration de Win32** tiene estas propiedades.

<dl> <dt>

**BitsPerPel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **En desuso**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Número de bits usados para representar el color en esta configuración (los bits por píxel). Esta propiedad ha quedado obsoleta. En su lugar, use las propiedades de las clases [**\_ VideoController de Win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) para determinar cómo se representa el color.

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

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**Intercalar**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** se deben intercalar las páginas que se imprimen. Intercalar es imprimir todo el documento antes de imprimir la siguiente copia, en lugar de imprimir cada página del documento el número necesario de veces.

Esta propiedad se omite a menos que el controlador de impresora indique compatibilidad con la intercalación.

</dd> <dt>

**Color**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Color del documento. Algunas impresoras de color tienen la capacidad de imprimir con un color negro verdadero en lugar de una combinación de cian,rillón y amarillo (CMY). Esto suele crear texto más oscuro y más nítido para los documentos. Esta opción solo es útil para impresoras de color que admiten la impresión en negro verdadero.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Monocromo (verdadero negro)

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Color

</dd> </dl>

</dd> <dt>

**Copias**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de copias que se imprimirán. El controlador de impresora debe admitir la impresión de copias de varias páginas.

Ejemplo: 2

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**DeviceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre descriptivo de la impresora. Este nombre es único para el tipo de impresora y puede truncarse debido a las limitaciones de la cadena de la que se deriva.

Ejemplo: "PCL/HP PclJet"

</dd> <dt>

**DisplayFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el dispositivo de pantalla es de color o monocromo y si el tipo de examen no está entrelazado o entrelazado. Esta propiedad ha quedado obsoleta. En su lugar, use propiedades de presentación como **la propiedad DisplayType** de la **clase \_ DesktopMonitor de Win32.**

</dd> <dt>

**DisplayFrequency**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Muestra la frecuencia de actualización vertical. La frecuencia de actualización de un monitor es el número de veces que se vuelve a dibujar la pantalla por segundo (frecuencia). Esta propiedad ha quedado obsoleta. En su lugar, use las propiedades [**de la clase \_ VideoController Win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)o [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**DitherType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de dither de la impresora. Esta propiedad puede asumir valores predefinidos de 1 a 5, o valores definidos por el controlador de 6 a 256. El dithering de líneas es un método especial de dithering que produce bordes bien definidos entre las escalas de color negro, blanco y gris. No es adecuado para imágenes que incluyen continuos continuos en intensidad y matiz, como fotografías examinadas.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Sin dithering

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Pincel general

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Pincel fino

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Line Art

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

Escala de grises

</dd> </dl>

</dd> <dt>

**DriverVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de versión del controlador Windows impresora basado en datos. El fabricante del controlador crea y mantiene los números de versión.

</dd> <dt>

**Dúplex**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** la impresión se realiza en ambos lados. Si **es FALSE,** la impresión se realiza solo en un lado del medio.

</dd> <dt>

**FormName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No compatible.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (puntos por pulgada)
</dt> </dl>

Resolución de impresión en puntos por pulgada a lo largo del eje X (ancho) del trabajo de impresión (similar a la propiedad **XResolution** obsoleta). Este valor solo se establece cuando la **propiedad PrintQuality** de esta clase es positiva.

</dd> <dt>

**ICMIntent**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor específico de uno de los tres métodos posibles de coincidencia de colores (denominados intenciones) que se deben usar de forma predeterminada. ICM aplicaciones establecen intenciones mediante el uso de las ICM funciones. Esta propiedad puede suponer valores predefinidos de 1 a 3, o valores definidos por el controlador de 4 a 256. Las aplicaciones no ICM pueden usar este valor para determinar cómo la impresora controla los trabajos de impresión de color.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Saturación

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Compare

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Color exacto

</dd> </dl>

</dd> <dt>

**ICMMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cómo ICM se controla. Para una aplicación que no ICM, esta propiedad determina si ICM está habilitado o deshabilitado. Para ICM, el sistema examina esta propiedad para determinar qué parte del sistema del equipo controla ICM compatibilidad.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Disabled

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Windows

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Controlador de dispositivo

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Dispositivo

</dd> </dl>

</dd> <dt>

**LogPixels**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **En desuso**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Número de píxeles por pulgada lógica. Esta propiedad obsoleta solo es válida con dispositivos que funcionan con píxeles, lo que excluye dispositivos como impresoras. No hay ningún valor de reemplazo que se aplique a las impresoras.

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de medio en el que se imprime la impresora. La propiedad se puede establecer en un valor predefinido o un valor definido por el controlador mayor o igual que 256.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Estándar

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Transparencia

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Brillante

</dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre de la impresora a la que está asociada esta configuración. Este valor coincide con la **propiedad Name** de la instancia de [**Impresora Win32 \_**](win32-printer.md) asociada.

</dd> <dt>

**Orientación**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Orientación de impresión del papel.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Vertical

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Horizontal

</dd> </dl>

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimas de milímetro)
</dt> </dl>

Longitud del papel. Para determinar el tamaño del papel en pulgadas, divida este valor entre 254.

Ejemplo: 2794

</dd> <dt>

**PaperSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño del papel. Los tamaños posibles se encuentran en la **propiedad PaperSizesSupported** de la clase [**\_ Printer de Win32**](win32-printer.md) asociada.

Ejemplo: "A4 o Letra".

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimas de milímetro)
</dt> </dl>

Ancho del papel. Para determinar el tamaño del papel en pulgadas, divida este valor entre 254.

Ejemplo: 2159

</dd> <dt>

**SussHeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **En desuso**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propiedad no es compatible.

</dd> <dt>

**SussWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **En desuso**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propiedad no es compatible.

</dd> <dt>

**PrintQuality**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Uno de los cuatro niveles de calidad del trabajo de impresión. Si se especifica un valor positivo, la calidad se mide en puntos por pulgada.

<dt>

<span id="-1"></span>

<span id="-1"></span>**-1**


</dt> <dd>

Borrador

</dd> <dt>

<span id="-2"></span>

<span id="-2"></span>**-2**


</dt> <dd>

Bajo

</dd> <dt>

<span id="-3"></span>

<span id="-3"></span>**-3**


</dt> <dd>

Media

</dd> <dt>

<span id="-4"></span>

<span id="-4"></span>**-4**


</dt> <dd>

Alto

</dd> </dl>

</dd> <dt>

**Escala**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (porcentaje)
</dt> </dl>

Factor por el que se va a escalar la salida impresa. Por ejemplo, una escala de 75 reduce la salida de impresión a 3/4 su alto y ancho originales.

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

**SpecificationVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de versión de los datos de inicialización para el dispositivo asociado a la Windows basada en datos.

</dd> <dt>

**TTOption**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se deben imprimir las fuentes TrueType.

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Mapa de** bits (1)


</dt> <dd>

Imprime fuentes TrueType como gráficos. Esta es la acción predeterminada para las impresoras de matriz de puntos.

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Descargar** (2)


</dt> <dd>

Descarga fuentes TrueType como fuentes flexibles. Esta es la acción predeterminada para las impresoras que usan el lenguaje de control de impresoras (PCL).

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Sustituto** (3)


</dt> <dd>

Sustituye las fuentes de dispositivo por fuentes TrueType. Esta es la acción predeterminada para PostScript impresoras.

</dd> </dl>

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (puntos por pulgada)
</dt> </dl>

Resolución de impresión a lo largo del eje Y (alto) del trabajo de impresión (similar a la **propiedad YResolution** obsoleta). Este valor solo se establece cuando la **propiedad PrintQuality** de esta clase es positiva.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **En desuso**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propiedad ha quedado obsoleta. Use la **propiedad HorizontalResolution** en su lugar.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **En desuso**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propiedad ha quedado obsoleta. Use la **propiedad VerticalResolution** en su lugar.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ PrinterConfiguration de Win32** se deriva de [**cim \_ setting**](cim-setting.md).

**Información general**

Para poder determinar cómo distribuir y usar mejor los recursos de impresión, debe tener un conocimiento detallado de esos recursos. Por ejemplo, el Departamento A podría tener solo tres impresoras en comparación con cinco impresoras del Departamento B. Sin embargo, si las impresoras del Departamento A pueden imprimir 20 páginas por minuto y las impresoras del Departamento B solo pueden imprimir 5 páginas por minuto, los usuarios del Departamento A tienen realmente más capacidad de impresión. Sin conocer las funcionalidades detalladas de estas impresoras, podría concluir erróneamente que el Departamento A tiene poca capacidad de impresión y, por tanto, comprar impresoras adicionales que terminan sin usarse.

WMI incluye dos clases, [**Impresora \_ Win32**](win32-printer.md) e **Impresora Win32Configuración, \_** que se pueden usar para devolver información detallada sobre todas las impresoras instaladas en un equipo.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se recupera la información de la impresora.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](./cim-setting.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
