---
description: Configura los valores ip de los adaptadores de red que se aplicarán a una máquina virtual después de una conmutación por error.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Método SetFailoverNetworkAdapterSettings de la Msvm_ReplicationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 744c1b2e56fb50e5a0c16db7d03d7558b1ed69360de98f69a4aac795f9f7db63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147768"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a>Método SetFailoverNetworkAdapterSettings de la clase ReplicationService de Msvm \_

Configura las opciones de IP del adaptador de red que se aplicarán a una máquina virtual después de una conmutación por error. Estos parámetros de configuración se aplican después de una operación de conmutación por error, inmediatamente después de establecer la comunicación con el componente de integración Exchange KVP que se ejecuta en el sistema operativo invitado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia [**\_ de ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual cuyos adaptadores de red se van a configurar.

</dd> <dt>

*NetworkSettings* \[ En\]
</dt> <dd>

Matriz de instancias incrustadas de objetos [**\_ FailoverNetworkAdapterSettingData de Msvm.**](msvm-failovernetworkadaptersettingdata.md) Cada instancia describe los parámetros de configuración de uno de los adaptadores de red dentro de la máquina virtual. Las **propiedades IPAddresses** **y DHCPEnabled** deben especificarse en cada instancia.

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

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
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

[**InitiateFailover**](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[**ReplicationService de Msvm \_**](msvm-replicationservice.md)
</dt> <dt>

[**RevertFailover**](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

