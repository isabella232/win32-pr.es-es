---
description: Contiene las coordenadas de la presentación en el espacio de color de la Comisión Internacional de iluminación (CIE) XYZ.
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Clase XYZinCIE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716770"
---
# <a name="xyzincie-class"></a>Clase XYZinCIE

La clase WMI **XYZinCIE** contiene las coordenadas de la presentación en el espacio de color de la Comisión Internacional en la iluminación (CIE) XYZ.

## <a name="syntax"></a>Sintaxis

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a>Miembros

La clase **XYZinCIE** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **XYZinCIE** tiene estas propiedades.

<dl> <dt>

**X**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenada X.

</dd> <dt>

**S**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenada Y.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contiene las instancias incrustadas de la clase **XYZinCIE** para describir las características de color de un monitor.

Para calcular la coordenada z, en función de los valores x e y, use la relación \| \| (x, y, z) \| \| = 1.

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

 

 




