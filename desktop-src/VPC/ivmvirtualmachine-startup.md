---
title: Método de inicio IVMVirtualMachine (VPCCOMInterfaces. h)
description: Inicia la máquina virtual desde el estado no inicializado o guardado.
ms.assetid: 82f9b6f1-99b1-4402-93f5-b4aa3520a505
keywords:
- Método de inicio Virtual PC
- Método de inicio Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método de inicio
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a45e0952fc1a17fc6ba2ea639f2ee87f7b9ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996879"
---
# <a name="ivmvirtualmachinestartup-method"></a>IVMVirtualMachine:: Startup (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Inicia la máquina virtual desde el estado no inicializado o guardado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Startup(
  [out, retval] IVMTask **startupTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*startupTask* \[ out, retval\]
</dt> <dd>

Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de la ejecución de la secuencia de inicio de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                | La operación se realizó correctamente.<br/>                                                  |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                  | El parámetro es **null**.<br/>                                                     |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt> </dl> | El autor de la llamada debe tener permisos de acceso de ejecución para iniciar esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt> </dl>                           | La operación no se completó de manera oportuna.<br/>                             |
| <dl> <dt>**Máquina virtual \_ E \_ fuera \_ del \_ recurso**</dt> <dt>0xA0040203</dt> </dl>                    | No hay suficientes recursos de host.<br/>                                           |
| <dl> <dt>**Máquina virtual \_ E \_ demasiadas \_ \_ máquinas virtuales**</dt> <dt>0xA0040204</dt> </dl>                       | Hay demasiadas máquinas virtuales activas.<br/>                                    |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt> </dl>                          | La máquina virtual ya se está ejecutando.<br/>                                        |
| <dl> <dt>**Máquina virtual \_ E \_ primario \_ modificado**</dt> <dt>0xA00400687</dt> </dl>                    | No se puede iniciar la máquina virtual porque se ha modificado el VHD primario.<br/>     |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                          | Se produjo un error inesperado.<br/>                                              |



 

## <a name="remarks"></a>Observaciones

Si la máquina virtual está guardada, se restaurará desde el estado guardado.

Los valores siguientes se pueden devolver a través de la propiedad [**error**](ivmtask-error.md) del objeto [**IVMTask**](ivmtask.md) devuelto.



| Código de [**error**](ivmtask-error.md) /valor                                                                                                                                                                                                                                      | Descripción                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)<br/>                                                 | El hardware no admite la virtualización.<br/>              |
| <span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)<br/> | La virtualización de hardware está deshabilitada.<br/>                       |
| <span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)<br/>                             | Tanto Virtual PC 2007 como Windows Virtual PC están instalados.<br/> |
| <span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)<br/>             | Se instala otro software de virtualización.<br/>                |
| <span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)<br/>                                                                 | No hay suficientes recursos de host.<br/>                       |



 

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

 

