---
title: Método IVMVirtualMachine RemoveHardDiskConnection (VPCCOMInterfaces. h)
description: Quita la conexión de disco duro especificada de la máquina virtual.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- Método RemoveHardDiskConnection Virtual PC
- Método RemoveHardDiskConnection Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método RemoveHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422355"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a>IVMVirtualMachine:: RemoveHardDiskConnection (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Quita la conexión de disco duro especificada de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hardDiskConnection* \[ de\]
</dt> <dd>

Un objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) que representa la conexión del disco duro que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                              |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                    | El parámetro es **null**.<br/>                                 |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>            | La configuración es desconocida.<br/>                              |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt> </dl> | La máquina virtual está en estado en ejecución o guardada.<br/>        |
| <dl> <dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt> </dl>         | La unidad especificada no está conectada a esta ubicación de bus.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                          |



 

## <a name="remarks"></a>Observaciones

Solo puede quitar una conexión de disco duro existente de una máquina virtual detenida. Se obtiene una lista de las conexiones actualmente asociadas a la máquina virtual mediante la enumeración de la propiedad [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

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

 

