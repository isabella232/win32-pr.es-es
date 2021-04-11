---
title: Propiedad MultipleUserSessionsAllowed de IVMGuestOS
description: Determina si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- Propiedad MultipleUserSessionsAllowed Virtual PC
- Propiedad MultipleUserSessionsAllowed Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad MultipleUserSessionsAllowed
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
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150382"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a>IVMGuestOS:: MultipleUserSessionsAllowed (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a>Valor de propiedad

**Variante \_ TRUE** si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado, **Variant \_ false** en caso contrario.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                                                       |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                       | Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) aún no se ha inicializado en el sistema operativo invitado.<br/> |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                            | El parámetro *sessionStatus* es **null**.<br/>                                                                          |
| <dl> <dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                                                                                 |
| <dl> <dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/>                                                   |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                                                                   |



## <a name="remarks"></a>Observaciones

El valor de esta propiedad no es válido a menos que la propiedad [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) sea una **variante \_ verdadera**.

En el caso de los sistemas operativos de cliente de Windows, **MultipleUserSessionsAllowed** es **Variant \_ true** si se admite el cambio rápido de usuario. En el caso de los sistemas operativos Windows Server, **MultipleUserSessionsAllowed** es **VARIANT \_ true** si servicios de escritorio remoto (anteriormente denominado Terminal Services) está instalado y habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                      |
| IDL<br/>                      | <dl> <dt>IVMGuestOS. idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

