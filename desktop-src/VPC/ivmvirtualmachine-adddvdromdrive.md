---
title: Método IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces.h)
description: Agrega una nueva unidad de CD o DVD a la máquina virtual.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- AddDVDROMDrive, método Virtual PC
- Método AddDVDROMDrive Para PC virtual, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , Método AddDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a875af50d38270b898c17f2848a4e4b33fe79a4b17d9ab7b6be58cdcfcf92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123235"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a>IVMVirtualMachine::AddDVDROMDrive (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Agrega una nueva unidad de CD o DVD a la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*busNumber* \[ En\]
</dt> <dd>

Bus al que se conectará la unidad.



| Valor                                                                        | Significado                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La unidad se conectará al primer bus.<br/>  |
| <dl> <dt>1</dt> </dl> | La unidad se conectará al segundo bus.<br/> |



 

</dd> <dt>

*deviceNumber* \[ En\]
</dt> <dd>

Dispositivo al que se conectará la unidad.



| Valor                                                                        | Significado                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La unidad se conectará al primer dispositivo del bus.<br/>  |
| <dl> <dt>1</dt> </dl> | La unidad se conectará al segundo dispositivo del bus.<br/> |



 

</dd> <dt>

*dvdDrive* \[ out, retval\]
</dt> <dd>

Objeto [**IVMDVDDrive.**](ivmdvddrive.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                               | Descripción                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                     | La operación se realizó correctamente.<br/>                       |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                       | El *parámetro dvdDrive* es **NULL.**<br/>               |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>                    | Un parámetro no es válido.<br/>                           |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>               | La configuración es desconocida.<br/>                       |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O \_ \_ \_ GUARDADA**</dt> <dt>0XA004020B</dt> </dl>    | La máquina virtual está en estado en ejecución o guardado.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ DRIVE \_ BUS \_ LOC IN \_ \_ USE**</dt> <dt>0xA00400503</dt> </dl> | La ubicación de bus especificada está en uso.<br/>               |
| <dl> <dt>**Máquina virtual \_ E \_ UNIDAD \_ NO VÁLIDA**</dt> <dt>0xA0040502</dt> </dl>            | La unidad especificada no es válida.<br/>                   |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>               | Se produjo un error inesperado.<br/>                   |



 

## <a name="remarks"></a>Comentarios

Solo puede agregar una nueva unidad de CD o DVD a una máquina virtual detenida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

