---
title: Método IVMVirtualMachine Pause (VPCCOMInterfaces.h)
description: Pausa la máquina virtual.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Pausa del método Virtual PC
- Pause method Virtual PC , IVMVirtualMachine interface
- IVMVirtualMachine interface Virtual PC , Método Pause
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bbab3da710a66c1e737e02693cb2002452ec11154b1be3da0e3568fea38e59f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471485"
---
# <a name="ivmvirtualmachinepause-method"></a>IVMVirtualMachine::P ause (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Pausa la máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                | La operación se realizó correctamente.<br/>                                     |
| <dl> <dt>**E \_ ERROR**</dt> <dt>0x80004005</dt> </dl>                                     | La máquina virtual ya está en pausa.<br/>                                         |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (ACCESO DE ERROR \_ \_ DENEGADO)**</dt> <dt>0x80070005</dt> </dl> | El autor de la llamada debe tener permisos de acceso de ejecución para pausar esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ TIEMPO DE \_ ESPERA**</dt> <dt>0XA0040202</dt> </dl>                           | La operación no se ha completado a tiempo.<br/>                |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>                     | La máquina virtual no se está ejecutando.<br/>                               |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | La configuración es desconocida.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Se produjo un error inesperado.<br/>                                 |



 

## <a name="remarks"></a>Observaciones

**La** pausa no guarda el estado actual de la máquina virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

