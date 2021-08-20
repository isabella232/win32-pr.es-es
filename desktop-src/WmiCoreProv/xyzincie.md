---
description: Contiene las coordenadas de la presentación en el espacio de colores XYZ de la Comisión Internacional de Iluminación (CIE).
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: XYZinCIE (clase)
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
ms.openlocfilehash: bc84f1550d2ba20daa0fb92dd3ce6f8d934207cff09de6d8b3e8b961bd341b6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110786"
---
# <a name="xyzincie-class"></a>XYZinCIE (clase)

La clase WMI **XYZinCIE** contiene las coordenadas de la presentación en el espacio de colores XYZ de la Comisión Internacional de Iluminación (CIE).

## <a name="syntax"></a>Sintaxis

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a>Miembros

La **clase XYZinCIE** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase XYZinCIE** tiene estas propiedades.

<dl> <dt>

**X**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenada X.

</dd> <dt>

**S**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Coordenada Y.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [**clase WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contiene instancias incrustadas de la **clase XYZinCIE** para describir las características de color de un monitor.

Para calcular la coordenada z, en función de los valores x e y, use la relación \| \| (x,y,z) \| \| = 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




