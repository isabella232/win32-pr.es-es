---
description: Representa las características de color de la Comisión Internacional de iluminación (CIE) de un monitor del equipo.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Clase WmiMonitorColorCharacteristics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360900"
---
# <a name="wmimonitorcolorcharacteristics-class"></a>Clase WmiMonitorColorCharacteristics

La clase **WmiMonitorColorCharacteristics** representa las características de color de la Comisión Internacional en iluminación (CIE) de un monitor del equipo. Los datos corresponden a los datos del bloque de características del color de la estructura de vídeo electrónica estándar (VESA) de la asociación mejorada de la visualización de datos (E-EDID).

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a>Miembros

La clase **WmiMonitorColorCharacteristics** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **WmiMonitorColorCharacteristics** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el monitor activo.

</dd> <dt>

**Azul**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenadas CIE para Blue, representadas por una instancia de la clase [**XYZinCIE**](xyzincie.md) .

</dd> <dt>

**DefaultWhite**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenadas de CIE blancas predeterminadas.

</dd> <dt>

**Verde**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenadas CIE para verde, representadas por una instancia de la clase [**XYZinCIE**](xyzincie.md) .

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

**Rojo**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenadas CIE para rojo, representadas por una instancia de la clase [**XYZinCIE**](xyzincie.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de cromaticidad y de punto blanco se expresan como números fraccionarios con un formato de codificación. Este formato es preciso en la milésima ubicación, que tiene una longitud de 10 bits. El bit más significativo (MSB) representa 2 ^-1 y el bit menos significativo (LSB) representa los coeficientes de 2 ^-10, respectivamente. La precisión de los valores almacenados en la estructura E-EDID v1. x debe ser precisa de +/-0,005 del valor real.

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

 

 




