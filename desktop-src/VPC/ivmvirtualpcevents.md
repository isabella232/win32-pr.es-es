---
title: Interfaz IVMVirtualPCEvents (VPCCOMInterfaces.h)
description: Define la interfaz de eventos saliente para la interfaz IVMVirtualPC.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- IVMVirtualPCEvents interface Virtual PC
- IVMVirtualPCEvents interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e2998adebd38d6e51329771d1ea538a97fd06c5c46e14bfd47d16fc3dce17b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938297"
---
# <a name="ivmvirtualpcevents-interface"></a>IVMVirtualPCEvents (interfaz)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define la interfaz de eventos saliente para [**la interfaz IVMVirtualPC.**](ivmvirtualpc.md) El cliente implementa estos métodos para recibir eventos enviados desde [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="members"></a>Miembros

La **interfaz IVMVirtualPCEvents** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualPCEvents** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IVMVirtualPCEvents** tiene estos métodos.



| Método                                                        | Descripción                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnEventLogged**](ivmvirtualpcevents-oneventlogged.md)     | Recibe una notificación que Windows Virtual PC registra un evento.<br/>      |
| [**OnVMStateChange**](ivmvirtualpcevents-onvmstatechange.md) | Recibe la notificación de que el estado de una máquina virtual ha cambiado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents se define como efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



 

