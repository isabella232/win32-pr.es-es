---
description: Agrega la configuración de características Ethernet a la configuración de una conexión Ethernet de máquina virtual.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Método AddFeatureSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360711"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método AddFeatureSettings de la \_ clase VirtualSystemManagementService de MSVM

Agrega la configuración de características Ethernet a la configuración de una conexión Ethernet de máquina virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedConfiguration* \[ de\]
</dt> <dd>

Referencia a una instancia de la clase [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que representa la conexión Ethernet afectada.

</dd> <dt>

*FeatureSettings* \[ de\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) que describe la configuración de características que se va a agregar a la configuración de conexión.

</dd> <dt>

*ResultingFeatureSettings* \[ enuncia\]
</dt> <dd>

Una matriz de referencias a las instancias de la clase [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representa la configuración de características agregada.

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

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

