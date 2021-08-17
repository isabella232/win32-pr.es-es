---
title: Método IVMHardDiskConnection SetBusLocation (VPCCOMInterfaces.h)
description: Establece la ubicación del bus a la que está conectado este disco duro.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- SetBusLocation, método Virtual PC
- Método SetBusLocation Virtual PC , interfaz IVMHardDiskConnection
- IVMHardDiskConnection interface Virtual PC , método SetBusLocation
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f2ff59b0318c321d1fb5ce75bac8c5604c5e96474c52565732ec3794b4aab0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974355"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a>IVMHardDiskConnection::SetBusLocation (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Establece la ubicación del bus a la que está conectado este disco duro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vmBusNumber* \[ En\]
</dt> <dd>

Número de bus que se va a usar.

</dd> <dt>

*vmDeviceNumber* \[ En\]
</dt> <dd>

Número de dispositivo que se va a usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                               | Descripción                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                     | La operación se realizó correctamente.<br/>                                                                    |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>                    | La ubicación del bus especificada no es válida.<br/>                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O GUARDADA \_ \_ \_ 0XA004020B**</dt> <dt></dt> </dl>    | No se pudo establecer la ubicación del bus porque la máquina virtual está en estado en ejecución o guardado.<br/>    |
| <dl> <dt>**Máquina virtual \_ E \_ DRIVE \_ BUS \_ LOC IN \_ \_ USE**</dt> <dt>0xA00400503</dt> </dl> | No se pudo establecer la ubicación del bus porque otro dispositivo está conectado actualmente a esta ubicación.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA**</dt> <dt>0xA0040502</dt> </dl>            | La unidad actual no es válida.<br/>                                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>               | La máquina virtual actual no es válida.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>               | Se produjo un error inesperado.<br/>                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDiskconnection se define como \_ aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

