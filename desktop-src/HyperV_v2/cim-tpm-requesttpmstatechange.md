---
description: Solicita que el estado del TPM cambie al valor especificado en el parámetro RequestedTPMState.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Método RequestTPMStateChange de la clase CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001620"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a>Método RequestTPMStateChange de la \_ clase TPM CIM

Solicita que el estado del TPM cambie al valor especificado en el parámetro *RequestedTPMState* . Si la invocación del método se completa correctamente, la propiedad **TPMState** debe ser igual al parámetro **RequestedTPMState** . Invocar varias veces al método **RequestTPMStateChange** podría provocar que se sobrescriban o se pierdan solicitudes anteriores.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestedTPMState* \[ de\]
</dt> <dd>

Estados de TPM solicitados.

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**S1 habilitada: propiedad activa** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 deshabilitado-propiedad activa** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**S3 habilitado: inactivo-propiedad** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**S4 deshabilitado-inactivo-propiedad** (5)


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**S5 habilitado-activo-no propietario** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 deshabilitado-activo-no propietario** (7)


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 habilitado: inactivo:** no tiene propiedad (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 deshabilitado-inactivo:** no tiene propiedad (9)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (32768... 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*AuthorizationToken* \[ de\]
</dt> <dd>

Token de autorización que puede ser necesario para que la acción surta efecto. El parámetro *AuthorizationToken* puede ser necesario para establecer la presencia física o para pasar OwnerAuth, la contraseña de autorización de propietario definida por TCG. En el caso de OwnerAuth, \_ es posible que se requiera el SharedCredential de CIM con un valor que no sea NULL de CIM \_ SharedCredential. Secret. La \_ propiedad CIM SharedCredential. algorithm también se puede especificar en función de la propiedad CIM \_ TPMCapabilities. SupportedPasswordAlgorithms.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Puede contener una referencia al [**\_ ConcreteJob de CIM**](cim-concretejob.md) creado para realizar el seguimiento de la transición de estado iniciada por la invocación del método.

</dd> <dt>

*TimeoutPeriod* \[ de\]
</dt> <dd>

Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado. El formato de intervalo debe usarse para especificar el *TimeoutPeriod*. Un valor de 0 o un parámetro null indica que el cliente no tiene ningún requisito de tiempo para la transición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM de CIM \_**](cim-tpm.md)
</dt> </dl>

 

 




