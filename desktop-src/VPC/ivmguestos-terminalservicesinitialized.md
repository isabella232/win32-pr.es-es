---
title: Propiedad IVMGuestOS TerminalServicesInitialized (VPCCOMInterfaces.h)
description: Estado de Servicios de Escritorio remoto en el sistema operativo invitado.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- TerminalServicesInitialized, propiedad Virtual PC
- TerminalServicesInitialized, propiedad Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Pc virtual, propiedad TerminalServicesInitialized
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595ae6028bea1984a320a699d204e4d3c23c1ca44e021cbbd994bbc5b832655a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512155"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a>Propiedad IVMGuestOS::TerminalServicesInitialized

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el estado de Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) en el sistema operativo invitado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a>Valor de propiedad

Estado de inicialización.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                          | La operación se ha realizado correctamente Servicios de Escritorio remoto se ha inicializado. El valor de propiedad devuelto indica si Servicios de Escritorio remoto está disponible en el sistema operativo invitado.<br/> |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | La característica de componentes de integración se está ejecutando, Servicios de Escritorio remoto aún no se ha inicializado.<br/>                                                                                               |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **NULL.**<br/>                                                                                                                                                                       |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual (VM) debe estar en ejecución para esta operación.<br/>                                                                                                                                     |
| <dl> <dt>Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | La característica de componentes de integración no se ejecuta en el sistema operativo invitado.<br/>                                                                                                                 |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                                                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS se define como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

