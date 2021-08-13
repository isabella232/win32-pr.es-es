---
title: IVMGuestOS MultipleUserSessionsAllowed, propiedad
description: Determina si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- MultipleUserSessionsAllowed, propiedad Virtual PC
- MultipleUserSessionsAllowed, propiedad Virtual PC, interfaz IVMGuestOS
- IVMGuestOS interface Virtual PC , MultipleUserSessionsAllowed property
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68075c13cfc65b79d992b849b310bd3c88b09f7901567baf249bff15496ede05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594078"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a>IVMGuestOS::MultipleUserSessionsAllowed, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Determina si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a>Valor de propiedad

**VARIANT \_ TRUE** si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado; en caso contrario, **VARIANT \_ FALSE.**

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                                                       |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) aún no se ha inicializado en el sistema operativo invitado.<br/> |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                            | El *parámetro sessionStatus* es **NULL.**<br/>                                                                          |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                                                                                 |
| <dl> <dt>Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/>                                                   |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                                                                   |



## <a name="remarks"></a>Observaciones

El valor de esta propiedad no es válido a menos que la propiedad [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) sea **VARIANT \_ TRUE.**

Para Windows sistemas operativos cliente, **MultipleUserSessionsAllowed** es **VARIANT \_ TRUE** si se admite la conmutación rápida de usuarios. Para Windows server, **MultipleUserSessionsAllowed** es **VARIANT \_ TRUE** si Servicios de Escritorio remoto (anteriormente denominado Terminal Services) está instalado y habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                      |
| Idl<br/>                      | <dl> <dt>IVMGuestOS.idl</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS se define como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

