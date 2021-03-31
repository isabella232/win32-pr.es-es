---
title: Método IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces. h)
description: Conecta un dispositivo USB a una máquina virtual.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Método AttachUSBDevice Virtual PC
- Método AttachUSBDevice Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método AttachUSBDevice
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
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079502"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>IVMVirtualMachine:: AttachUSBDevice (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Conecta un dispositivo USB a una máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inUSBDevice* \[ de\]
</dt> <dd>

Un puntero [**IVMUSBDevice**](ivmusbdevice.md) que representa el dispositivo USB conectado al host.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                             | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                   | La operación se realizó correctamente.<br/>                                           |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                     | El parámetro es **null**.<br/>                                              |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>                        | La máquina virtual no se está ejecutando.<br/>                                                  |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>                             | La configuración es desconocida.<br/>                                           |
| <dl> <dt>**Máquina virtual \_ E/s \_ \_ no \_ DISP**</dt> <dt>0xA0040504</dt> </dl>                   | Los componentes de integración no están disponibles en el sistema operativo invitado.<br/> |
| <dl> <dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt> </dl>          | La característica USB no está disponible.<br/>                                       |
| <dl> <dt>**Máquina virtual \_ \_Error del \_ \_ controlador \_ del conector de E USB**</dt> <dt>0xA00400925</dt> </dl>          | Error en el controlador del conector USB.<br/>                                 |
| <dl> <dt>**Máquina virtual \_ E \_ conexión USB con \_ \_ errores \_ más \_ dispositivos**</dt> <dt>0xA00400931</dt> </dl>     | No se pueden conectar más dispositivos a la máquina virtual.<br/>                                   |
| <dl> <dt>**Máquina virtual \_ E \_ \_ \_ \_ \_ error de directiva**</dt> de <dt>0xA00400932</dt> de conexión USB </dl>         | Una configuración de directiva de grupo impide el redireccionamiento USB.<br/>               |
| <dl> <dt>**Máquina virtual \_ \_ \_ \_ \_ \_ Error al adjuntar USB**</dt> <dt>0xA00400933</dt> </dl> | Otro cliente ya ha conectado un dispositivo USB.<br/>            |
| <dl> <dt>**Máquina virtual \_ E \_ \_ \_ no se pudo adjuntar USB**</dt> <dt>0xA00400926</dt> </dl>                    | Error en la operación de adjuntar.<br/>                                            |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                             | Se produjo un error inesperado.<br/>                                       |



 

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

 

