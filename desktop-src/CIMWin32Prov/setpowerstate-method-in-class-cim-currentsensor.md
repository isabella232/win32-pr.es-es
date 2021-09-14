---
description: 'Método SetPowerState de la clase CIM_CurrentSensor: el método SetPowerState establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo en ese estado.'
ms.assetid: 8dd54a71-152a-4668-bdb6-c0968d8ff094
ms.tgt_platform: multiple
title: Método SetPowerState de la CIM_CurrentSensor clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CurrentSensor.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1a5f546ea13cf085b09315abe56369d5ba0e152
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062605"
---
# <a name="setpowerstate-method-of-the-cim_currentsensor-class"></a>Método SetPowerState de la clase \_ CurrentSensor de CIM

El **método SetPowerState** establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo en ese estado. En una subclase, el conjunto de códigos de retorno posibles debe especificarse mediante un **calificador ValueMap** en el método . Las cadenas a las que se traduce el contenido de **ValueMap** también deben especificarse en la subclase como calificador de **matriz Values.** Este método se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

Potencia completa.

</dd> <dt>

2
</dt> <dd>

Modo de bajo consumo de energía de Ahorro de energía.

</dd> <dt>

3
</dt> <dd>

Ahorro de energía en espera.

</dd> <dt>

4
</dt> <dd>

Otro ahorro de energía.

</dd> <dt>

5
</dt> <dd>

Ciclo de energía.

</dd> <dt>

6
</dt> <dd>

Apagar.

</dd> </dl> </dd> <dt>

*Hora* \[ En\]
</dt> <dd>

Especifica cuándo se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método). Cuando el *parámetro PowerState* es igual a 5 ("Ciclo de energía"), el parámetro *Time* indica cuándo se debe volver a encender el dispositivo. El apagado es inmediato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificadas y otro valor si se produjo cualquier otro error.

## <a name="remarks"></a>Observaciones

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CIM \_ CurrentSensor](setpowerstate-method-in-class-cim-currentsensor.md)
</dt> <dt>

[**CIM \_ CurrentSensor**](cim-currentsensor.md)
</dt> </dl>

 

 




