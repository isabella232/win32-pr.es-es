---
title: Método de cierre de sesión IVMGuestOS (VPCCOMInterfaces. h)
description: Cierra la sesión de todos los usuarios del sistema operativo invitado.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Logoff (método, equipo virtual PC)
- Logoff Method Virtual PC, IVMGuestOS (interfaz)
- Interfaz IVMGuestOS Virtual PC, método Logoff
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079731"
---
# <a name="ivmguestoslogoff-method"></a>IVMGuestOS:: Logoff (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Cierra la sesión de todos los usuarios del sistema operativo invitado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*outLogoffTask* \[ out, retval\]
</dt> <dd>

Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de finalización de la secuencia de cierre de sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                | La operación se realizó correctamente.<br/>                                                |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                          | Se produjo un error inesperado.<br/>                                            |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                  | El parámetro es **null**.<br/>                                                   |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt> </dl> | El autor de la llamada debe tener permisos de acceso de ejecución para esta máquina virtual.<br/>                 |
| <dl> <dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt> </dl>                           | La operación no se completó de manera oportuna.<br/>                           |
| <dl> <dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt> </dl>       | La característica componentes de integración no está instalada en esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>                     | La máquina virtual (VM) debe estar en ejecución para esta operación.<br/>                 |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>                          | La configuración es desconocida.<br/>                                                |



 

## <a name="remarks"></a>Observaciones

`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) se devuelve a través de la propiedad [**error**](ivmtask-error.md) del objeto [**IVMTask**](ivmtask.md) devuelto. no hay sesiones de inicio de sesión en el sistema operativo invitado.

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

 

