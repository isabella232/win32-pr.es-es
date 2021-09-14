---
description: Representa las características de color de la Comisión Internacional de Iluminación (CIE) de un monitor de equipo.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073080"
---
# <a name="wmimonitorcolorcharacteristics-class"></a>Clase WmiMonitorColorCharacteristics

La **clase WmiMonitorColorCharacteristics** representa las características de color de la Comisión Internacional de Iluminación (CIE) de un monitor de equipo. Los datos corresponden a los datos del bloque Características de color de la estructura Enhanced Extended Display Identification Data (E-EDID) de Video Electronics Standard Association (VESA).

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

## <a name="members"></a>Members

La **clase WmiMonitorColorCharacteristics** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WmiMonitorColorCharacteristics** tiene estas propiedades.

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

Coordenadas CIE para azul, representadas por una instancia de la [**clase XYZinCIE.**](xyzincie.md)

</dd> <dt>

**DefaultWhite**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenadas CIE blancas predeterminadas.

</dd> <dt>

**Verde**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenadas de CIE para verde, representadas por una instancia de la [**clase XYZinCIE.**](xyzincie.md)

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

**Rojo**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenadas CIE para rojo, representadas por una instancia de la [**clase XYZinCIE.**](xyzincie.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de punto blanco y de siticidad se expresan como números fraccionales mediante un formato de codificación. Este formato es preciso en la milésima posición, que tiene una longitud de 10 bits. El bit más significativo (MSB) representa 2^-1 y el bit menos significativo (LSB) representa 2^-10 coeficientes, respectivamente. La precisión de los valores almacenados en la estructura E-EDID v1.x debe ser precisa con +/- 0,005 del valor real.

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

 

 




