---
title: Método IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces. h)
description: Agrega una nueva conexión de disco duro a la máquina virtual.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- Método AddHardDiskConnection Virtual PC
- Método AddHardDiskConnection Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método AddHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651400"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a>IVMVirtualMachine:: AddHardDiskConnection (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Agrega una nueva conexión de disco duro a la máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hardDiskPath* \[ de\]
</dt> <dd>

La ruta de acceso completa del archivo de disco duro virtual (VHD) que se va a conectar.

</dd> <dt>

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

*hardDiskConnection* \[ out, retval\]
</dt> <dd>

Objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                                  |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                      | El parámetro *hardDiskConnection* es **null**.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | Un parámetro *hardDiskPath* es **null** o el parámetro *busNumber* o *deviceNumber* no es válido.<br/>                                            |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt> </dl>   | El sistema no encuentra el archivo especificado por el parámetro *hardDiskPath* .<br/>                                                                     |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt> </dl>   | El sistema no puede encontrar la ruta de acceso especificada por el parámetro *hardDiskPath* .<br/>                                                                     |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt> </dl>      | El parámetro *hardDiskPath* contiene un carácter no válido (uno de " \* ? <>/ \| ": ").<br/>                                                        |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt> </dl>      | El parámetro *hardDiskPath* especifica una ruta de acceso relativa o vacía. Se requiere una ruta de acceso absoluta.<br/>                                                |
| <dl> <dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt> </dl>   | La ruta de acceso especificada por el parámetro *hardDiskPath* es demasiado larga. La ruta de acceso debe tener menos de 260 caracteres.<br/>                                     |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>                              | La configuración es desconocida.<br/>                                                                                                                  |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt> </dl>                   | La máquina virtual está en estado en ejecución o guardada.<br/>                                                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ unidad \_ \_ de bus \_ de disco en \_ uso**</dt> <dt>0xA00400503</dt> </dl>                | La ubicación de bus especificada está en uso.<br/>                                                                                                          |
| <dl> <dt>**Máquina virtual \_ E 0xA0040682 de \_ \_ \_ archivo HD no válido**</dt> <dt></dt> </dl>                        | El VHD es superior a 127 GB y no se puede conectar al bus IDE.<br/>                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ no compatible con \_ el \_ \_ tipo de disco HD**</dt> <dt>0xA00400686</dt> </dl>             | El parámetro *hardDiskPath* hace referencia a un VHD vinculado o a un disco duro virtual de diferenciación en un VHD vinculado. Los VHD vinculados no se pueden conectar a las máquinas virtuales.<br/> |
| <dl> <dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt> </dl> | El disco duro virtual especificado ya está conectado a otra ubicación de bus para esta máquina virtual.<br/>                                                                    |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                              |



 

## <a name="remarks"></a>Observaciones

Solo puede Agregar una nueva conexión de disco duro a una máquina virtual detenida.

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

 

