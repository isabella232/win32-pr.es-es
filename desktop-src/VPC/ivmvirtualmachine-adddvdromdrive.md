---
title: Método IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces. h)
description: Agrega una nueva unidad de CD o DVD a la máquina virtual.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- Método AddDVDROMDrive Virtual PC
- Método AddDVDROMDrive Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método AddDVDROMDrive
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
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695954"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a>IVMVirtualMachine:: AddDVDROMDrive (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*busNumber* \[ de\]
</dt> <dd>

El bus al que se conectará la unidad.



| Value                                                                        | Significado                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La unidad se conectará al primer bus.<br/>  |
| <dl> <dt>1</dt> </dl> | La unidad se conectará al segundo bus.<br/> |



 

</dd> <dt>

*deviceNumber* \[ de\]
</dt> <dd>

El dispositivo al que se conectará la unidad.



| Value                                                                        | Significado                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La unidad se conectará al primer dispositivo del bus.<br/>  |
| <dl> <dt>1</dt> </dl> | La unidad se conectará al segundo dispositivo del bus.<br/> |



 

</dd> <dt>

*dvdDrive* \[ out, retval\]
</dt> <dd>

Objeto [**IVMDVDDrive**](ivmdvddrive.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                               | Descripción                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                     | La operación se realizó correctamente.<br/>                       |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                       | El parámetro *dvdDrive* es **null**.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                    | Un parámetro no es válido.<br/>                           |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>               | La configuración es desconocida.<br/>                       |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt> </dl>    | La máquina virtual está en estado en ejecución o guardada.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ unidad \_ \_ de bus \_ de disco en \_ uso**</dt> <dt>0xA00400503</dt> </dl> | La ubicación de bus especificada está en uso.<br/>               |
| <dl> <dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt> </dl>            | La unidad especificada no es válida.<br/>                   |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>               | Se produjo un error inesperado.<br/>                   |



 

## <a name="remarks"></a>Observaciones

Solo puede Agregar una nueva unidad de CD o DVD a una máquina virtual detenida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

