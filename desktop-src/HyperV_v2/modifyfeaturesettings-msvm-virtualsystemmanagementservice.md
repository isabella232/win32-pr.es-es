---
description: Modifica la configuración actual de las características de una conexión Ethernet de máquina virtual.
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: Método ModifyFeatureSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c376158008c5ad0e611d3a05c7e73d2e7d1b44cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360812"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ModifyFeatureSettings de la \_ clase VirtualSystemManagementService de MSVM

Modifica la configuración actual de las características de una conexión Ethernet de máquina virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FeatureSettings* \[ de\]
</dt> <dd>

Una matriz de cadenas que contienen una instancia incrustada de una clase derivada de la clase [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) , que describe las modificaciones realizadas a la configuración actual de las características de una conexión Ethernet existente. La propiedad **InstanceID** de cada una de estas instancias identifica la configuración de características que se va a modificar.

</dd> <dt>

*ResultingFeatureSettings* \[ enuncia\]
</dt> <dd>

Una matriz de referencias a las instancias de la clase [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representan la configuración de características modificada.

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

**Estado no válido** (5)
</dt> <dt>

**Parámetros incompatibles** (6)
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

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

