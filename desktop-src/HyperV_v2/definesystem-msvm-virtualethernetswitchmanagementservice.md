---
description: Crea un nuevo conmutador virtual.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Método DefineSystem de la clase Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911694"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Método DefineSystem de la \_ clase VirtualEthernetSwitchManagementService de MSVM

Crea un nuevo conmutador virtual. Las propiedades que no se especifican se rellenarán con los valores predeterminados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Configuración* \[ de\]
</dt> <dd>

Instancia insertada de la clase [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) que se usa para definir los atributos del conmutador virtual que se va a crear. Este parámetro es necesario.

</dd> <dt>

*ResourceSettings* \[ de\]
</dt> <dd>

Una matriz de instancias incrustadas de la clase [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que describe la configuración de los puertos de conmutador que se van a crear en el ámbito del nuevo conmutador virtual. Si se especifica **null** , se creará el conmutador virtual sin recursos (es decir, sin puertos de conmutador).

</dd> <dt>

*ReferenceConfiguration* \[ de\]
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*ResultingSystem* \[ enuncia\]
</dt> <dd>

Si un conmutador virtual se crea correctamente, una referencia a una instancia de la clase [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa el conmutador virtual recién definido.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

