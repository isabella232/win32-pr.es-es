---
description: Solicita que se cambie el estado del elemento.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: Método RequestStateChange de la clase Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3358c6c9907717e536466466dd074faf3a038a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001250"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a>Método RequestStateChange de la \_ clase de teclado MSVM

Solicita que se cambie el estado del elemento.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestedState* \[ de\]
</dt> <dd>

Nuevo estado solicitado para el elemento. Esta información se colocará en la propiedad **RequestedState** de la instancia si el código de retorno es 0 (' completado sin error '), 3 (' timeout ') o 4096 (0x1000) (' Job Started '). Para obtener explicaciones detalladas de los valores de *RequestedState* , consulte la descripción de las propiedades **EnabledState** y **RequestedState** .

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Apagar** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Sin conexión** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Prueba** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Diferir** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

Modo **inactivo** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Reinicio** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Restablecer** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (32768... 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia al trabajo. Este parámetro puede ser **null** si la tarea se ha completado.

</dd> <dt>

*TimeoutPeriod* \[ de\]
</dt> <dd>

Cantidad máxima de tiempo que el cliente espera que se lleve a cabo la transición al nuevo estado. El formato de intervalo debe usarse para especificar este período de tiempo de espera. Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición. Si esta propiedad no contiene 0 o **null**, y la implementación no admite este parámetro, se devuelve un código de retorno de 4098 ("se ha utilizado el parámetro de tiempo de espera no compatible").

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error desconocido o no especificado** (2)
</dt> <dt>

**No se puede completar en el período de tiempo de espera** (3)
</dt> <dt>

**Error** (4)
</dt> <dt>

**Parámetro no válido** (5)
</dt> <dt>

**En uso** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Transición de estado no válida** (4097)
</dt> <dt>

**No se admite el uso de parámetros de tiempo de espera** (4098)
</dt> <dt>

**Ocupado** (4099)
</dt> <dt>

**Método reservado** (4100.. 32767)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Teclado MSVM**](msvm-keyboard.md)
</dt> </dl>

 

 




