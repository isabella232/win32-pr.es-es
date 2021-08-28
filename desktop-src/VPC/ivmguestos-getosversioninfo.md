---
title: Método IVMGuestOS GetOsVersionInfo (VPCCOMInterfaces.h)
description: Recupera la información de versión del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Método GetOsVersionInfo de Virtual PC
- Método GetOsVersionInfo para PC virtual, interfaz IVMGuestOS
- IVMGuestOS interface Virtual PC , Método GetOsVersionInfo
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef39259b429d096246bbdbe5cb23e6021f498b2d9d47cd14fb12409eca814c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653475"
---
# <a name="ivmguestosgetosversioninfo-method"></a>IVMGuestOS::GetOsVersionInfo (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la información de versión del sistema operativo invitado que se ejecuta en la máquina virtual .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*guestOsVersionInfo* \[ out, retval\]
</dt> <dd>

Puntero a una [**estructura GUESTOSVERSIONINFOEX.**](guestosversioninfoex.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                       | Descripción                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                             | La operación se realizó correctamente.<br/>                                  |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                               | El parámetro es **NULL.**<br/>                                     |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl> | No hay suficiente memoria disponible para completar esta solicitud.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                       | Se produjo un error inesperado.<br/>                              |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>                  | La máquina virtual no se está ejecutando.<br/>                                         |
| <dl> <dt>**Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl>    | Los componentes de integración no están instalados en esta máquina virtual.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS se define como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

