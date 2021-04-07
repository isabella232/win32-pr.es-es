---
description: Establece el estado de energía del dispositivo. El uso de este método está en desuso. En su lugar, use el método SetPowerState en la clase PowerManagementService asociada.
ms.assetid: 2f53a8bd-18a8-45aa-92ad-68a33b6a42ab
title: Método SetPowerState de la clase CIM_LogicalDevice (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a29f71806747e6d63f53618acd09d472ac8bdea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002489"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-hyper-v-management"></a>Método SetPowerState de la clase CIM_LogicalDevice (administración de Hyper-V)

Establece el estado de energía del dispositivo. El uso de este método está en desuso. En su lugar, use el método **SetPowerState** en la clase **PowerManagementService** asociada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PowerState* \[ de\]
</dt> <dd>

El estado de energía que se va a establecer.

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

**Potencia completa** (1)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

Ahorro **de energía: modo de baja energía** (2)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

Ahorro **de energía: en espera** (3)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

Ahorro **de energía: otros** (4)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Ciclo de energía** (5)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Desconectar (6** )


</dt> <dd></dd> </dl> </dd> <dt>

*Hora* \[ de de\]
</dt> <dd>

Time indica cuándo debe establecerse el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDevice de CIM \_**](cim-logicaldevice.md)
</dt> </dl>

 

 




