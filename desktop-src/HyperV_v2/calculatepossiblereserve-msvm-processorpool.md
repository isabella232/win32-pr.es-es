---
description: Este método se usa para buscar la reserva real, siendo el parámetro de entrada el número de procesadores de máquina virtual para los que se calcula la reserva.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Método CalculatePossibleReserve de la Msvm_ProcessorPool clase
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
ms.openlocfilehash: 06cfa01dd89392c05f460462d8bda5898b47d90b6e027fa885bf039f62488cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042075"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>Método CalculatePossibleReserve de la clase \_ Msvm ProcessorPool

Este método se usa para buscar la reserva real, siendo el parámetro de entrada el número de procesadores de máquina virtual para los que se calcula la reserva. Este método es necesario porque la reserva de recursos de procesador depende en gran medida del número de procesadores que se deben programar en paralelo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProcessorCount* \[ En\]
</dt> <dd>

Tipo: **uint16**

Número de procesadores de máquina virtual para los que se calcula la reserva. El valor máximo de esta propiedad es el número de procesadores lógicos para el equipo host.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Cantidad de recursos de CPU que se pueden reservar para una máquina virtual.

## <a name="remarks"></a>Comentarios

El acceso a [**la clase \_ Msvm ProcessorPool**](msvm-processorpool.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Msvm \_ ProcessorPool**](msvm-processorpool.md)
</dt> </dl>

 

