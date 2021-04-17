---
description: Representa los parámetros de entrada para el vídeo digital.
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
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716624"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a>Clase WmiMonitorDigitalVideoInputParams

**WmiMonitorDigitalVideoInputParams** representa los parámetros de entrada de vídeo digital. Los datos de esta clase se corresponden con los datos de la definición de entrada de vídeo de vídeo electrónica estándar (VESA) estándar de identificación de la visualización extendida mejorada (E-EDID). Una instancia de esta clase solo está disponible cuando el valor de la propiedad **VideoInputType** de la clase [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) es "digital".

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

La clase **WmiMonitorDigitalVideoInputParams** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **WmiMonitorDigitalVideoInputParams** tiene estas propiedades.

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

Calificadores: **clave**
</dt> </dl>

Nombre de la instancia de monitor específica.

</dd> <dt>

**IsDFP1xCompatible**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

VESA DFP 1. x o compatible. Si se establece, la interfaz es compatible con el panel plano digital VESA (DFP) 1. x transición minimizada de señalización diferencial (TMDS) CRGB, 1 píxel/reloj, hasta 8 bits/color más significativo (MSB) alineado, DE activo alto.

</dd> </dl>

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

 

 




