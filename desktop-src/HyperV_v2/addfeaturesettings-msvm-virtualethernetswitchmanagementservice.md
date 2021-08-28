---
description: Agrega la configuración de características a la configuración de un puerto de conmutador Ethernet.
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: Método AddFeatureSettings de la Msvm_VirtualEthernetSwitchManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 679e4dbba4b8d3e90691955a0642f9a22692d73824059419f5faceacc85abaf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829665"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Método AddFeatureSettings de la clase \_ VirtualEthernetSwitchManagementService de Msvm

Agrega la configuración de características a la configuración de un puerto de conmutador Ethernet.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedConfiguration* \[ En\]
</dt> <dd>

Referencia a una clase [**derivada \_ CIM SettingData**](/previous-versions//cc136911(v=vs.85)) que representa el puerto de conmutador Ethernet afectado o la configuración del conmutador Ethernet.

</dd> <dt>

*FeatureSettings* \[ En\]
</dt> <dd>

Matriz de cadenas que contienen una instancia incrustada de una clase derivada de la clase [**\_ FeatureSettingData de Msvm,**](msvm-featuresettingdata.md) que describe la configuración de características que se va a agregar a la configuración del puerto del conmutador.

</dd> <dt>

*ResultingFeatureSettings* \[ out\]
</dt> <dd>

Matriz de referencias a instancias de la clase [**\_ FeatureSettingData de Msvm**](msvm-featuresettingdata.md) que representan la configuración de características agregada.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

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
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

