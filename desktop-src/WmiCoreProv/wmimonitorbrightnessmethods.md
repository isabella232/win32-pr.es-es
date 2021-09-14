---
description: Contiene métodos que administran el brillo del monitor.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Clase WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073082"
---
# <a name="wmimonitorbrightnessmethods-class"></a>Clase WmiMonitorBrightnessMethods

La clase WMI **WmiMonitorBrightnessMethods** contiene métodos que administran el brillo del monitor.

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Members

La **clase WmiMonitorBrightnessMethods** tiene estos tipos de miembros:

-   [Métodos](#wmimonitorbrightnessmethods-class)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase WmiMonitorBrightnessMethods** tiene estos métodos.



| Método                                                                                                         | Descripción                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | Establece el brillo de nuevo en la configuración de directiva.<br/>     |
| [**WmiSetALSBrightness**](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | Establece el valor de brillo del sensor de luz ambiente.<br/>     |
| [**WmiSetALSBrightnessState**](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | Controla el estado de brillo del sensor de luz ambiente.<br/> |
| [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | Establece el brillo del monitor.<br/>                        |



 

### <a name="properties"></a>Propiedades

La **clase WmiMonitorBrightnessMethods** tiene estas propiedades.

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

 

 




