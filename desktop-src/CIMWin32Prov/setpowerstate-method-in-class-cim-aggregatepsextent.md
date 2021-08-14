---
description: El método SetPowerState define el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo en ese estado.
ms.assetid: 3808b75d-229e-44c0-a1bc-aa260590cd36
ms.tgt_platform: multiple
title: Método SetPowerState de la CIM_AggregatePSExtent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a979ad1a61e907bcc1d14b402b72999590909001e5214dca83e5920dceeac1bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439825"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepsextent-class"></a>Método SetPowerState de la clase \_ AggregatePSExtent de CIM

El **método SetPowerState** define el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo en ese estado. En una subclase, se debe especificar el conjunto de códigos de retorno posibles, mediante un **calificador ValueMap** en el método . Las cadenas a las que se traduce el contenido de **ValueMap** también se deben especificar en la subclase como calificador de **matriz Values.** Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PowerState* \[ En\]
</dt> <dd>

Valor **valueMap** que especifica el estado de energía deseado para este dispositivo lógico.

<dt>

1
</dt> <dd>

Potencia completa

</dd> <dt>

2
</dt> <dd>

Modo de bajo consumo de energía con ahorro de energía

</dd> <dt>

3
</dt> <dd>

Espera de ahorro de energía

</dd> <dt>

4
</dt> <dd>

Power-save other

</dd> <dt>

5
</dt> <dd>

Ciclo de energía

</dd> <dt>

6
</dt> <dd>

Apagado

</dd> </dl> </dd> <dt>

*Hora* \[ En\]
</dt> <dd>

Cuando se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método). Cuando el *parámetro PowerState* es igual a 5(ciclo de energía), el parámetro *Time* indica cuándo se debe volver a encender el dispositivo. El apagado es inmediato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificadas y otro valor si se produjo cualquier otro error.

## <a name="remarks"></a>Observaciones

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Agregado \_ DE CIMPSExtent](setpowerstate-method-in-class-cim-aggregatepsextent.md)
</dt> <dt>

[**Agregado \_ DE CIMPSExtent**](cim-aggregatepsextent.md)
</dt> </dl>

 

 




