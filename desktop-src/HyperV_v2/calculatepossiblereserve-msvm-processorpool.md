---
description: Este método se usa para buscar la reserva real con el parámetro de entrada que es el número de procesadores de máquinas virtuales para los que se calcula la reserva.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Método CalculatePossibleReserve de la clase Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813854"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>Método CalculatePossibleReserve de la \_ clase ProcessorPool de MSVM

Este método se usa para buscar la reserva real con el parámetro de entrada que es el número de procesadores de máquinas virtuales para los que se calcula la reserva. Este método es necesario porque la reserva de recursos del procesador depende en gran medida del número de procesadores que se deben programar en paralelo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProcessorCount* \[ de\]
</dt> <dd>

Tipo: **UInt16**

El número de procesadores de máquinas virtuales para los que se calcula la reserva. El valor máximo de esta propiedad es el número de procesadores lógicos para el equipo host.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

La cantidad de recursos de CPU que se pueden reservar para una máquina virtual.

## <a name="remarks"></a>Observaciones

El acceso a la clase [**MSVM \_ ProcessorPool**](msvm-processorpool.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ ProcessorPool**](msvm-processorpool.md)
</dt> </dl>

 

