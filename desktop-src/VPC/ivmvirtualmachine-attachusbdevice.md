---
title: Método IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces.h)
description: Conecta un dispositivo USB a una máquina virtual.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- AttachUSBDevice method Virtual PC
- AttachUSBDevice method Virtual PC , IVMVirtualMachine interface
- IVMVirtualMachine interface Virtual PC , método AttachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c62f3e6862e14a7faa70719d1238500ab5dfe1de10801e7aea390e24a07210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006905"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>IVMVirtualMachine::AttachUSBDevice (Método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Conecta un dispositivo USB a una máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inUSBDevice* \[ En\]
</dt> <dd>

Puntero [**IVMUSBDevice**](ivmusbdevice.md) que representa el dispositivo USB conectado al host.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                             | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                   | La operación se realizó correctamente.<br/>                                           |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                     | El parámetro es **NULL.**<br/>                                              |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>                        | La máquina virtual no se está ejecutando.<br/>                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                             | La configuración es desconocida.<br/>                                           |
| <dl> <dt>**Máquina virtual \_ E \_ LAS \_ ADICIONES NO ESTÁN \_ DISPONIBLES**</dt> <dt>0xA0040504</dt> </dl>                   | Los componentes de integración no están disponibles en el sistema operativo invitado.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl>          | La característica USB no está disponible.<br/>                                       |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR DEL CONTROLADOR DEL CONECTOR \_ \_ \_ USB**</dt> <dt>0xA00400925</dt> </dl>          | Se produjo un error en el controlador del conector USB.<br/>                                 |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR DE CONEXIÓN USB MÁS \_ \_ \_ \_ DISPOSITIVOS**</dt> <dt>0XA00400931</dt> </dl>     | No se pueden conectar más dispositivos a la máquina virtual.<br/>                                   |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR DE CONEXIÓN USB DE GP \_ \_ \_ \_ 0XA00400932**</dt> <dt></dt> </dl>         | Una configuración de directiva de grupo impide el redireccionamiento USB.<br/>               |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR DE CONEXIÓN USB \_ \_ \_ YA \_**</dt> ASIGNADA <dt>0xA00400933</dt> </dl> | Otro cliente ya ha conectado un dispositivo USB.<br/>            |
| <dl> <dt>**Máquina virtual \_ E \_ ERROR DE CONEXIÓN USB \_ \_ 0xA00400926**</dt> <dt></dt> </dl>                    | Error en la operación de asociación.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                             | Se produjo un error inesperado.<br/>                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

