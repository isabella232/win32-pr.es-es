---
description: Representa los parámetros de entrada del vídeo digital.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Clase WmiMonitorDigitalVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: fa86add32d77a5b2838fc78eaf097c11b8a15db3f0fde9186f93046691ebc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926571"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a>Clase WmiMonitorDigitalVideoInputParams

**WmiMonitorDigitalVideoInputParams representa** los parámetros de entrada del vídeo digital. Los datos de esta clase corresponden a los datos del estándar E-EDID (Definición de entrada de vídeo de Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID). Una instancia de esta clase solo está disponible cuando el valor de la **propiedad VideoInputType** de la [**clase WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) es "Digital".

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a>Miembros

La **clase WmiMonitorDigitalVideoInputParams** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WmiMonitorDigitalVideoInputParams** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el monitor activo.

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

**IsDFP1xCompatible**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

VESA DFP 1.x o compatible. Si se establece, la interfaz es compatible con la señal compatible con el CRGB de señalización diferencial minimizada (TMDS) de transición de VESA Digital Flat Panel (DFP) 1.x, 1 píxel/reloj, hasta 8 bits/bit más significativo (MSB) alineado, DE activo alto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




