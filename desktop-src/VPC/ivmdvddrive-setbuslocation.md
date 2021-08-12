---
title: Método IVMDVDDrive SetBusLocation (VPCCOMInterfaces.h)
description: Adjunta la unidad de DVD a la ubicación de bus especificada en la máquina virtual.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- SetBusLocation, método Virtual PC
- Método SetBusLocation Virtual PC , interfaz IVMDVDDrive
- IVMDVDDrive interface Virtual PC , método SetBusLocation
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 593a42c21d1ed688185a7fe7123e972998859c010775a2cf4efd5f3bbbbaa98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595848"
---
# <a name="ivmdvddrivesetbuslocation-method"></a>IVMDVDDrive::SetBusLocation (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Adjunta la unidad de DVD a la ubicación de bus especificada en la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*busNumber* \[ En\]
</dt> <dd>

Número de bus al que se va a conectar esta unidad. Por ejemplo, en un bus IDE, este número representaría si se debe usar el número de bus principal o secundario.

</dd> <dt>

*deviceNumber* \[ En\]
</dt> <dd>

Número de dispositivo al que se va a conectar esta unidad. Por ejemplo, en un bus IDE, este número representaría si se debe usar la ubicación principal o secundaria del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                 | La ubicación del bus especificada no es válida.<br/>                                                                                     |
| <dl> <dt>**E \_ ERROR**</dt> <dt>0x80004005</dt> </dl>                       | Se produjo un error inesperado.<br/>                                                                                            |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O \_ \_ \_ GUARDADA**</dt> <dt>0XA004020B</dt> </dl> | No se puede establecer la ubicación del bus mientras la máquina virtual se está ejecutando o en un estado guardado.<br/>                                     |
| <dl> <dt>**VM \_ E \_ BUS \_ LOC EN \_ \_ USO**</dt> </dl>                                                                      | Otro dispositivo ya está conectado a la ubicación de bus especificada.<br/>                                                            |
| <dl> <dt>**Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA**</dt> <dt>0xA0040502</dt> </dl>         | No se pudo inicializar la unidad actual.<br/>                                                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | No se pudieron escribir los cambios en el archivo de preferencias porque no se pudo determinar la máquina virtual de esta unidad.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDVDDrive se define como \_ b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

