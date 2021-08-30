---
title: Método IVMGuestOS Logoff (VPCCOMInterfaces.h)
description: Cierra la sesión de todos los usuarios del sistema operativo invitado.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Método de cierre de sesión Virtual PC
- Método de cierre de sesión Virtual PC, interfaz IVMGuestOS
- IVMGuestOS interface Virtual PC , Logoff method
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
ms.openlocfilehash: 014a15dc62ec90228ec99d9daca45e858cba9d915eea28983f2a8db66932e808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007175"
---
# <a name="ivmguestoslogoff-method"></a>IVMGuestOS::Logoff (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

Objeto [**IVMTask que**](ivmtask.md) se usa para realizar un seguimiento del progreso de finalización de la secuencia de cierre de sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                | La operación se realizó correctamente.<br/>                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Se produjo un error inesperado.<br/>                                            |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                  | El parámetro es **NULL.**<br/>                                                   |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ACCESO DE ERROR \_ \_ DENEGADO)**</dt> <dt>0x80070005</dt> </dl> | El autor de la llamada debe tener permisos de acceso de ejecución para esta máquina virtual.<br/>                 |
| <dl> <dt>**Máquina virtual \_ Se \_ ha \_ 0xA0040202**</dt> <dt></dt> </dl>                           | La operación no se ha completado a tiempo.<br/>                           |
| <dl> <dt>**Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl>       | La característica de componentes de integración no está instalada en esta máquina virtual.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>                     | La máquina virtual (VM) debe estar en ejecución para esta operación.<br/>                 |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | La configuración es desconocida.<br/>                                                |



 

## <a name="remarks"></a>Comentarios

`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) se devuelve a través de la propiedad [**Error**](ivmtask-error.md) del objeto [**IVMTask**](ivmtask.md) devuelto no hay sesiones de inicio de sesión en el sistema operativo invitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

