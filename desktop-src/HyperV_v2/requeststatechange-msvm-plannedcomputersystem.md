---
description: Solicita que el estado del sistema planeado cambie al valor especificado.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Método RequestStateChange de la clase Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687471"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a>Método RequestStateChange de la \_ clase PlannedComputerSystem de MSVM

Solicita que el estado del sistema planeado cambie al valor especificado.

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

Estado solicitado para el sistema planeado.

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

Este parámetro no se utiliza y debe ser **null**.

</dd> <dt>

*TimeoutPeriod* \[ de\]
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.



| Código o valor devuelto                                                                                                                      | Descripción                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>0</dt> </dl>     | Correcto<br/>                                                                 |
| <dl> <dt></dt><dt>4096</dt> </dl>  |                                                                                    |
| <dl> <dt></dt><dt>32768</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32769</dt> </dl> | Acceso denegado.<br/>                                                          |
| <dl> <dt></dt><dt>32770</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32771</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32772</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32773</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32774</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32775</dt> </dl> | No se admite el valor especificado en el parámetro *RequestedState* .<br/> |
| <dl> <dt></dt><dt>32776</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32777</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32778</dt> </dl> |                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




