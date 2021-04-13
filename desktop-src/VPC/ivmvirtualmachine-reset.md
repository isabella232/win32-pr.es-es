---
title: Método de restablecimiento de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Restablece la máquina virtual.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Restablecer método virtual PC
- Método Reset Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método Reset
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492238"
---
# <a name="ivmvirtualmachinereset-method"></a>IVMVirtualMachine:: RESET (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Restablece la máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resetTask* \[ out, retval\]
</dt> <dd>

Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de finalización de la secuencia de restablecimiento de la máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                | La operación se realizó correctamente.<br/>                                     |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                  | El parámetro es **null**.<br/>                                        |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt> </dl> | El autor de la llamada debe tener permisos de acceso Execute para restablecer esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>                     | La máquina virtual no se está ejecutando.<br/>                                            |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>                          | La configuración es desconocida.<br/>                                     |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                          | Se produjo un error inesperado.<br/>                                 |



 

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

 

