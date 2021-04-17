---
description: Representa las características básicas de pantalla de un monitor de equipo.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: Clase WmiMonitorBasicDisplayParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706820"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>Clase WmiMonitorBasicDisplayParams

La clase WMI **WmiMonitorBasicDisplayParams** representa las características básicas de pantalla de un monitor de equipo. El valor de la propiedad **VideoInputType** indica si el monitor es analógico o digital. Los datos de esta clase se corresponden con los datos del bloque básico de parámetros de presentación/características de la Asociación de vídeo electrónica estándar (VESA) estándar mejorado de identificación de visualización extendida (E-EDID).

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a>Miembros

La clase **WmiMonitorBasicDisplayParams** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **WmiMonitorBasicDisplayParams** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el monitor activo.

</dd> <dt>

**DisplayTransferCharacteristic**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Visualización de la característica de transferencia (100 \* gamma-100).

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Nombre de la instancia de monitor específica.

</dd> <dt>

**MaxHorizontalImageSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño máximo de imagen horizontal en centímetros. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**MaxVerticalImageSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño máximo de imagen vertical en centímetros. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**SupportedDisplayFeatures**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mostrar las características admitidas por el monitor.

</dd> <dt>

**VideoInputType**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de entrada de vídeo.



| Value                                                                              | Significado            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>0 (0X0)</dt> </dl> | Analógico<br/>  |
| <dl> <dt>1 (0x1)</dt> </dl> | Digital<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

**MaxHorizontalImageSize** y **MaxVerticalImageSize** representan las dimensiones de imagen máximas que el monitor puede mostrar correctamente para todo el conjunto de combinaciones de control de tiempo y formato admitidas. La dimensión de imagen máxima se define mediante el estándar de definición de área de imagen de vídeo (VIAD) de VESA y se redondea al centímetro más cercano. El sistema del equipo host puede usar estos datos para seleccionar el tamaño y la relación de aspecto de la imagen que permitirá el texto escalado correctamente. Tenga en cuenta que, si uno o ambos de estos campos son cero, el sistema no realiza suposiciones sobre el tamaño de presentación. Por ejemplo, puede que el tamaño de una pantalla de proyección no esté determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




