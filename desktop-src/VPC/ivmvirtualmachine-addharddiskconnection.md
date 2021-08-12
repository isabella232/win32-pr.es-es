---
title: Método IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces.h)
description: Agrega una nueva conexión de disco duro a la máquina virtual.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- Equipo virtual del método AddHardDiskConnection
- Método AddHardDiskConnection Para PC virtual, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , Método AddHardDiskConnection
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
ms.openlocfilehash: d67bbeb5cdb347327a807b19ec16c901c211cdddb72ce88a8b5b00804b195f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592763"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a>IVMVirtualMachine::AddHardDiskConnection (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*hardDiskPath* \[ En\]
</dt> <dd>

Ruta de acceso completa del archivo de disco duro virtual (VHD) que se conectará.

</dd> <dt>

*busNumber* \[ En\]
</dt> <dd>

Bus al que se conectará la unidad.



| Value                                                                        | Significado                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La unidad se conectará al primer bus.<br/>  |
| <dl> <dt>1</dt> </dl> | La unidad se conectará al segundo bus.<br/> |



 

</dd> <dt>

*deviceNumber* \[ En\]
</dt> <dd>

Dispositivo al que se conectará la unidad.



| Value                                                                        | Significado                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La unidad se conectará al primer dispositivo del bus.<br/>  |
| <dl> <dt>1</dt> </dl> | La unidad se conectará al segundo dispositivo del bus.<br/> |



 

</dd> <dt>

*hardDiskConnection* \[ out, retval\]
</dt> <dd>

Objeto [**IVMHardDiskConnection.**](ivmharddiskconnection.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                    | La operación se realizó correctamente.<br/>                                                                                                                  |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                      | El *parámetro hardDiskConnection* es **NULL.**<br/>                                                                                                |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                                   | Un *parámetro hardDiskPath* es **NULL** o el *parámetro busNumber* o *deviceNumber* no es válido.<br/>                                            |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)**</dt> <dt>0X80070002</dt> </dl>   | El sistema no puede encontrar el archivo especificado por el *parámetro hardDiskPath.*<br/>                                                                     |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)**</dt> <dt>0X80070003</dt> </dl>   | El sistema no puede encontrar la ruta de acceso especificada por el *parámetro hardDiskPath.*<br/>                                                                     |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ NOMBRE NO \_ VÁLIDO)**</dt> <dt>0x8007007b</dt> </dl>      | El *parámetro hardDiskPath* contiene un carácter no válido (uno de " \* ?<>/ \| ":").<br/>                                                        |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | El *parámetro hardDiskPath* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                                                |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl>   | La ruta de acceso especificada por el *parámetro hardDiskPath* es demasiado larga. La ruta de acceso debe tener menos de 260 caracteres.<br/>                                     |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                              | La configuración es desconocida.<br/>                                                                                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O \_ \_ \_ GUARDADA**</dt> <dt>0XA004020B</dt> </dl>                   | La máquina virtual está en estado en ejecución o guardado.<br/>                                                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ UNIDAD DE BUS \_ \_ LOC EN \_ \_ USO**</dt> <dt>0xA00400503</dt> </dl>                | La ubicación de bus especificada está en uso.<br/>                                                                                                          |
| <dl> <dt>**Máquina virtual \_ E \_ ARCHIVOS HD NO \_ \_ VÁLIDOs**</dt> <dt>0xA0040682</dt> </dl>                        | El DISCO duro virtual es mayor que 127 GB y no se puede conectar al bus IDE.<br/>                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ TIPO DE DISCO HD \_ \_ \_ NO**</dt> COMPATIBLE <dt>0xA00400686</dt> </dl>             | El *parámetro hardDiskPath* hace referencia a un VHD vinculado o a un VHD de diferenciación a un VHD vinculado. Los discos duros virtuales vinculados no se pueden conectar a máquinas virtuales.<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(INFRACCIÓN \_ DE USO COMPARTIDO DE \_ ERRORES)**</dt> <dt>0x80070020</dt> </dl> | El VHD especificado ya está conectado a otra ubicación de bus para esta máquina virtual.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Se produjo un error inesperado.<br/>                                                                                                              |



 

## <a name="remarks"></a>Observaciones

Solo puede agregar una nueva conexión de disco duro a una máquina virtual detenida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

