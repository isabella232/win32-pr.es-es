---
title: Método IVMGuestOS GetOsVersionInfo (VPCCOMInterfaces. h)
description: Recupera información de versión del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Método GetOsVersionInfo Virtual PC
- Método GetOsVersionInfo Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método GetOsVersionInfo
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
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676951"
---
# <a name="ivmguestosgetosversioninfo-method"></a>IVMGuestOS:: GetOsVersionInfo (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera información de versión del sistema operativo invitado que se ejecuta en la máquina virtual (VM).

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

Puntero a una estructura [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                       | Descripción                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                             | La operación se realizó correctamente.<br/>                                  |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                               | El parámetro es **null**.<br/>                                     |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl> | No hay suficiente memoria disponible para completar esta solicitud.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                       | Se produjo un error inesperado.<br/>                              |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>                  | La máquina virtual no se está ejecutando.<br/>                                         |
| <dl> <dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt> </dl>    | Los componentes de integración no están instalados en esta máquina virtual.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

