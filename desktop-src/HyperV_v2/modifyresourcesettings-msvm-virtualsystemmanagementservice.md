---
description: 'Método ModifyResourceSettings de la clase Msvm_VirtualSystemManagementService: modifica la configuración de recursos virtuales.'
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Método ModifyResourceSettings de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 09ca0bb9fea02b6acc5599d9f907b1e60fdbd9ec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119343"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ModifyResourceSettings de la clase Msvm \_ VirtualSystemManagementService

Modifica la configuración de recursos virtuales. Cuando se aplica a partes de una configuración de máquina virtual actual, como efecto secundario, se pueden modificar los recursos de la máquina virtual activa.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ResourceSettings* \[ En\]
</dt> <dd>

Matriz de cadenas que contienen una instancia incrustada de una clase derivada de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), que contienen los aspectos modificados de los recursos virtuales existentes. La **propiedad InstanceID** de cada instancia identifica la configuración del recurso virtual que se va a modificar.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Matriz de referencias a instancias de objetos derivados de [**\_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representan aspectos virtuales de los recursos virtuales modificados.

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

**Estado no válido** (5)
</dt> <dt>

**Parámetros incompatibles** (6)
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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 solo \[ aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ModifyVirtualSystemResources (V1)**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

