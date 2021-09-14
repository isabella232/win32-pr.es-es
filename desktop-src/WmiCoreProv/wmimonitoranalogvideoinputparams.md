---
description: Representa los parámetros de entrada de vídeo análogos de un monitor de equipo.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: Clase WmiMonitorAnalogVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073092"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a>Clase WmiMonitorAnalogVideoInputParams

La **clase WMI WmiMonitorAnalogVideoInputParams representa** los parámetros de entrada de vídeo análogos de un monitor de equipo. Los datos de esta clase corresponden a los datos del estándar E-EDID (Definición de entrada de vídeo de Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID). Una instancia de esta clase solo está disponible cuando el valor de la propiedad **VideoInputType** de la [**clase WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) es "Analog".

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a>Members

La **clase WmiMonitorAnalogVideoInputParams** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WmiMonitorAnalogVideoInputParams** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el monitor activo.

</dd> <dt>

**CompositeSyncSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se admite la sincronización compuesta.



| Value                                                                              | Significado                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Se admite la sincronización compuesta en la línea de sincronización horizontal.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | No se admite la sincronización compuesta en la línea de sincronización horizontal.<br/> |



 

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

**SeparateSyncsSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se admiten sincronizaciones independientes.



| Value                                                                              | Significado                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Se admiten sincronizaciones independientes.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | No se admiten sincronizaciones independientes.<br/> |



 

</dd> <dt>

**SerrationOfVsyncRequired**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se requiere la elevación del pulso de sincronización vertical.



| Value                                                                              | Significado                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Se requiere la elevación del pulso de sincronización vertical cuando se usa la sincronización compuesta o el vídeo de sincronización en verde.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | No se requiere la elevación del pulso de sincronización vertical cuando se usa la sincronización compuesta o el vídeo de sincronización en verde.<br/> |



 

</dd> <dt>

**SetupExpected**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se espera la instalación.



| Value                                                                              | Significado                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Monitor espera una configuración de cero a cero o un espacio en blanco según el estándar de nivel de señal adecuado.<br/>                      |
| <dl> <dt>1 (0x1)</dt> </dl> | El monitor no espera una configuración de cero a cero o un espacio en blanco según el estándar de nivel de señal adecuado.<br/> |



 

</dd> <dt>

**SignalLevelStandard**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estándar de nivel de señal para conexiones de conector de vídeo mejorado (EVC).



| Value                                                                              | Significado                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | 0.7,0.3 \[ V\]<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | 0.714,0.286 \[ V\]<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | 1.0,0.4 \[ V\]<br/>     |
| <dl> <dt>3 (0x3)</dt> </dl> | 0.7,0.0 \[ V\]<br/>     |



 

</dd> <dt>

**SyncOnGreenVideoSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se admite la sincronización en verde.



| Value                                                                              | Significado                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Se admite la sincronización en vídeo verde.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | No se admite la sincronización en vídeo verde.<br/> |



 

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

 

 




