---
description: Representa las características de visualización básicas de un monitor de equipo.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073091"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>Clase WmiMonitorBasicDisplayParams

La clase WMI **WmiMonitorBasicDisplayParams** representa las características de presentación básicas de un monitor de equipo. El valor de la **propiedad VideoInputType** indica si el monitor es análogo o digital. Los datos de esta clase corresponden a los datos del bloque Basic Display Parameters/Features del estándar E-EDID (Enhanced Extended Display Identification Data, E-EDID) de Video Electronics Standard Association (VESA).

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

## <a name="members"></a>Members

La **clase WmiMonitorBasicDisplayParams** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WmiMonitorBasicDisplayParams** tiene estas propiedades.

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

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Muestra la característica de transferencia (100 \* Gamma-100).

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Nombre de la instancia de monitor específica.

</dd> <dt>

**MaxHorizontalImageSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño máximo de la imagen horizontal en centímetros. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**MaxVerticalImageSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño máximo de la imagen vertical en centímetros. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**SupportedDisplayFeatures**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mostrar características compatibles con el monitor.

</dd> <dt>

**VideoInputType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de entrada de vídeo.



| Value                                                                              | Significado            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Analógico<br/>  |
| <dl> <dt>1 (0x1)</dt> </dl> | Digital<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

**MaxHorizontalImageSize** y **MaxVerticalImageSize** representan las dimensiones de imagen máximas que el monitor puede mostrar correctamente para todo el conjunto de combinaciones de formato y tiempo admitidas. La dimensión de imagen máxima se define mediante el estándar de definición de área de imagen de vídeo (VIAD) de VESA y se redondea al centímetros más cercano. El sistema del equipo host puede usar estos datos para seleccionar el tamaño de la imagen y la relación de aspecto que permitirán escalar correctamente el texto. Tenga en cuenta que, si alguno de estos campos o ambos son cero, el sistema no hace ninguna suposición sobre el tamaño de presentación. Por ejemplo, el tamaño de una presentación de proyección puede ser indeterminado.

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

 

 




