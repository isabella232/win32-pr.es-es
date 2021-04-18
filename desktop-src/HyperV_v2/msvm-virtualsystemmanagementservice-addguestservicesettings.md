---
description: Agrega la configuración del servicio de invitado a una configuración de sistema virtual.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Método AddGuestServiceSettings de la clase Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: 5bcdfd8c159e92efe633c04e22af5bceb9d003e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540302"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método AddGuestServiceSettings de la \_ clase VirtualSystemManagementService de MSVM

Agrega la configuración del servicio de invitado a una configuración de sistema virtual.

Cuando se aplica a partes de una configuración de sistema virtual "actual", se puede modificar como un efecto secundario en los servicios invitados del sistema virtual activo.

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

*AffectedConfiguration* \[ de\]
</dt> <dd>

Referencia a un [**\_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) que describe la configuración afectada.

</dd> <dt>

*GuestServiceSettings* \[ de\]
</dt> <dd>

Una matriz que contiene la configuración del servicio de invitado.

</dd> <dt>

*ResultingGuestServiceSettings* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, contiene una referencia a un [**\_ SettingData de CIM**](cim-settingdata.md) que describe la configuración del servicio invitado resultante.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

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

**Tiempo de espera** (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (de no.. 32767)
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

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

