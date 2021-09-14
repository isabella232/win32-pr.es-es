---
description: Contiene elementos descriptores de modo para la matriz MonitorSourceModes de la clase WmiMonitorListedSupportedSourceModes.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: VideoModeDescriptor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073103"
---
# <a name="videomodedescriptor-class"></a>VideoModeDescriptor (clase)

La clase WMI **VideoModeDescriptorVideo** contiene elementos descriptores de modo para la matriz **MonitorSourceModes** de la [**clase WmiMonitorListedSupportedSourceModes.**](wmimonitorlistedsupportedsourcemodes.md) Estos elementos incluyen características de supervisión, como la frecuencia de actualización, las características de píxeles o el tamaño de la imagen. La **clase VideoModeDescriptorVideo** contiene información que es un superconjunto de los datos disponibles de los bloques de control de tiempo establecidos, estándares y detallados.

## <a name="syntax"></a>Sintaxis

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a>Members

La **clase VideoModeDescriptor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase VideoModeDescriptor** tiene estas propiedades.

<dl> <dt>

**CompositePolarityType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de polaridad compuesta. Se trata de la polaridad de los pulsos de sincronización horizontal fuera de la sincronización vertical.



| Value                                                                              | Significado                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La polaridad compuesta es positiva.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | La polaridad compuesta es negativa.<br/>                                 |
| <dl> <dt>2 (0x2)</dt> </dl> | No aplicable. El tipo de sincronización de señal debe ser compuesto digitalmente.<br/> |



 

</dd> <dt>

**HorizontalActivePixels**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de píxeles activos horizontalmente.

</dd> <dt>

**HorizontalBlankingPixels**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de píxeles de espacio en blanco horizontal

</dd> <dt>

**HorizontalBorder**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Borde horizontal.

</dd> <dt>

**HorizontalImageSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño de imagen horizontal en milímetros (mm).

</dd> <dt>

**HorizontalPolarityType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de polaridad horizontal.



| Value                                                                              | Significado                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La polaridad horizontal es positiva.<br/>                               |
| <dl> <dt>1 (0x1)</dt> </dl> | La polaridad horizontal es negativa.<br/>                               |
| <dl> <dt>2 (0x2)</dt> </dl> | No aplicable. El tipo de sincronización de señal debe ser independiente digitalmente.<br/> |



 

</dd> <dt>

**HorizontalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Denominador de frecuencia de actualización horizontal.

</dd> <dt>

**HorizontalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Numerador de frecuencia de actualización horizontal en Hertz (Hz).

</dd> <dt>

**HorizontalSyncOffset**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Desplazamiento de sincronización horizontal.

</dd> <dt>

**HorizontalSyncPulseWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho del pulso de sincronización horizontal.

</dd> <dt>

**IsInterlaced**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el modo de presentación está entrelazado.

</dd> <dt>

**IsSerrationRequired**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica qué tipo de serranía es necesario, si procede.



| Value                                                                              | Significado                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | El controlador debe proporcionar sincronización horizontal durante la sincronización vertical.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | El controlador no debe proporcionar sincronización horizontal durante la sincronización vertical.<br/>                             |
| <dl> <dt>2 (0x2)</dt> </dl> | No aplicable. El tipo de sincronización de señales debe ser así, compuesto análogo o compuesto digital.<br/> |



 

</dd> <dt>

**IsSyncOnRGB**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica qué líneas de señal de vídeo se deben sincronizar, si procede.



| Value                                                                              | Significado                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | El pulso de sincronización debe aparecer en las tres líneas de señal de vídeo.<br/>                  |
| <dl> <dt>1 (0x1)</dt> </dl> | El pulso de sincronización solo debe aparecer en la línea de señal de vídeo verde.<br/>          |
| <dl> <dt>2 (0x2)</dt> </dl> | No aplicable. El tipo de sincronización de señal debe ser compuesto análogo de toba.<br/> |



 

</dd> <dt>

**PixelClockRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Velocidad del reloj de píxeles en Hertz (Hz).

</dd> <dt>

**StereoModeType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de modo estéreo. En la tabla siguiente se enumeran los valores posibles.



| Value                                                                              | Significado                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Sin estéreo.<br/>                                               |
| <dl> <dt>1 (0x1)</dt> </dl> | Estéreo secuencial de campo con imagen derecha en sincronización estéreo.<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Estéreo secuencial de campo con imagen izquierda en sincronización estéreo.<br/>  |
| <dl> <dt>3 (0x3)</dt> </dl> | Estéreo intercalado de 2 vías con imagen derecha en líneas uniformes.<br/> |
| <dl> <dt>4 (0x4)</dt> </dl> | Estéreo intercalado de 2 vías con imagen izquierda en líneas uniformes.<br/>  |
| <dl> <dt>5 (0x5)</dt> </dl> | Estéreo intercalado de 4 vías.<br/>                                |
| <dl> <dt>6 (0x6)</dt> </dl> | Estéreo intercalado en paralelo.<br/>                         |



 

</dd> <dt>

**SyncSignalType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de sincronización de señal. En la tabla siguiente se enumeran los valores posibles.



| Value                                                                              | Significado                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Compuesto análogo<br/>         |
| <dl> <dt>1 (0x1)</dt> </dl> | Compuesto análogo de Fuente<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Compuesto digital<br/>        |
| <dl> <dt>3 (0x3)</dt> </dl> | Digital Separate<br/>         |



 

</dd> <dt>

**VerticalActivePixels**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de píxeles activos verticalmente.

</dd> <dt>

**VerticalBlankingPixels**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de píxeles de espacio en blanco vertical.

</dd> <dt>

**VerticalBorder**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Borde vertical.

</dd> <dt>

**VerticalImageSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño de imagen vertical en milímetros (mm).

</dd> <dt>

**VerticalPolarityType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de polaridad vertical.



| Value                                                                              | Significado                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La polaridad vertical es positiva.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | La polaridad vertical es negativa<br/>                                  |
| <dl> <dt>2 (0x2)</dt> </dl> | No aplicable. El tipo de sincronización de señal debe ser independiente digitalmente.<br/> |



 

</dd> <dt>

**VerticalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Denominador de frecuencia de actualización vertical.

</dd> <dt>

**VerticalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Numerador de frecuencia de actualización vertical en Hertz (Hz).

</dd> <dt>

**VerticalSyncOffset**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Desplazamiento de sincronización vertical.

</dd> <dt>

**VerticalSyncPulseWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho de pulso de sincronización vertical.

</dd> <dt>

VideoStandardType
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo estándar de vídeo.



| Value                                                                                | Significado                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Otros<br/>                                                                                               |
| <dl> <dt>1 (0x1)</dt> </dl>   | VESA DMT. En video electronics standard association (VESA) display monitor timings specification (Especificación de control de tiempo del monitor de pantalla de Video Electronics Standard Association [VESA]).<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>   | VESA GTF. Del estándar fórmula de control de tiempo generalizado de VESA.<br/>                                            |
| <dl> <dt>3 (0x3)</dt> </dl>   | VESA CVT/From VESA Coordinated Video Timings standard( VeSA CVT/From VESA Coordinated Video Timings standard).<br/>                                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | IBM<br/>                                                                                                 |
| <dl> <dt>5 (0x5)</dt> </dl>   | MANZANA<br/>                                                                                               |
| <dl> <dt>6 (0x6)</dt> </dl>   | HAN M<br/>                                                                                              |
| <dl> <dt>7 (0x7)</dt> </dl>   | JJ J<br/>                                                                                              |
| <dl> <dt>8 (0x8)</dt> </dl>   | HAN 433<br/>                                                                                            |
| <dl> <dt>9 (0x9)</dt> </dl>   | PAL B<br/>                                                                                               |
| <dl> <dt>10 (0xA)</dt> </dl>  | PAL B1<br/>                                                                                              |
| <dl> <dt>11 (0xB)</dt> </dl>  | PAL G<br/>                                                                                               |
| <dl> <dt>12 (0xC)</dt> </dl>  | PAL H<br/>                                                                                               |
| <dl> <dt>13 (0xD)</dt> </dl>  | PAL I<br/>                                                                                               |
| <dl> <dt>14 (0xE)</dt> </dl>  | PAL D<br/>                                                                                               |
| <dl> <dt>15 (0xF)</dt> </dl>  | PAL N<br/>                                                                                               |
| <dl> <dt>16 (0x10)</dt> </dl> | PAL NC<br/>                                                                                              |
| <dl> <dt>17 (0x11)</dt> </dl> | SECAM B<br/>                                                                                             |
| <dl> <dt>18 (0x12)</dt> </dl> | SECAM D<br/>                                                                                             |
| <dl> <dt>19 (0x13)</dt> </dl> | SECAM G<br/>                                                                                             |
| <dl> <dt>20 (0x14)</dt> </dl> | SECAM H<br/>                                                                                             |
| <dl> <dt>21 (0x15)</dt> </dl> | SECAM K<br/>                                                                                             |
| <dl> <dt>22 (0x16)</dt> </dl> | SECAM K1<br/>                                                                                            |
| <dl> <dt>23 (0x17)</dt> </dl> | SECAM L<br/>                                                                                             |
| <dl> <dt>24 (0x18)</dt> </dl> | SECAM L1<br/>                                                                                            |
| <dl> <dt>25 (0x19)</dt> </dl> | EIA861<br/>                                                                                              |
| <dl> <dt>26 (0x1A)</dt> </dl> | EIA861A<br/>                                                                                             |
| <dl> <dt>27 (0x1B)</dt> </dl> | EIA861B<br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




