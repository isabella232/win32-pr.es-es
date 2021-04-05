---
description: El método SetUrgency establece el nivel de urgencia deseado para una alarma.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Método SetUrgency de la clase CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000598"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a>Método SetUrgency de la \_ clase AlarmDevice de CIM

El método **SetUrgency** establece el nivel de urgencia deseado para una alarma.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestedUrgency* \[ de\]
</dt> <dd>

Frecuencia relativa con la que la alarma parpadea, vibra o emite tonos sonoros. Los siguientes valores proceden de la propiedad **urgencia** de [**CIM \_ AlarmDevice**](cim-alarmdevice.md).

<dt>

0
</dt> <dd>

Desconocido.

</dd> <dt>

1
</dt> <dd>

Otros.

</dd> <dt>

2
</dt> <dd>

No se admite.

</dd> <dt>

3
</dt> <dd>

Informativo.

</dd> <dt>

4
</dt> <dd>

No crítico.

</dd> <dt>

5
</dt> <dd>

Crítico.

</dd> <dt>

6
</dt> <dd>

Irrecuperable.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite el nivel de urgencia solicitado y cualquier otro número para indicar un error.

## <a name="remarks"></a>Observaciones

Este método no está implementado actualmente por WMI. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[\_ALARMDEVICE CIM](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**\_ALARMDEVICE CIM**](cim-alarmdevice.md)
</dt> </dl>

 

