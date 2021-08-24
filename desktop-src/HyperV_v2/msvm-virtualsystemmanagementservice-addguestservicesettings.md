---
description: Agrega la configuración del servicio de invitado a una configuración del sistema virtual.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Método AddGuestServiceSettings de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f011a0bce545bbde57cbcc9c22861f492cbc27e71ddc717a379d82cbd27bc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681145"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método AddGuestServiceSettings de la clase Msvm \_ VirtualSystemManagementService

Agrega la configuración del servicio de invitado a una configuración del sistema virtual.

Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden modificar los servicios invitados del sistema virtual activo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedConfiguration* \[ En\]
</dt> <dd>

Referencia a [**cim \_ virtualSystemSettingData**](cim-virtualsystemsettingdata.md) que describe la configuración afectada.

</dd> <dt>

*GuestServiceSettings* \[ En\]
</dt> <dd>

Matriz que contiene la configuración del servicio invitado.

</dd> <dt>

*ResultingGuestServiceSettings* \[ out\]
</dt> <dd>

Si se ejecuta correctamente, contiene una referencia a [**un \_ valor settingData de CIM**](cim-settingdata.md) que describe la configuración del servicio invitado resultante.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

