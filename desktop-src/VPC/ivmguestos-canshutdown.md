---
title: Propiedad CanShutdown de IVMGuestOS (VPCCOMInterfaces.h)
description: Indica si el sistema operativo invitado se puede apagar correctamente.
ms.assetid: 239cba43-9494-4efd-a4c8-0bb47f476b81
keywords:
- CanShutdown, propiedad Virtual PC
- Propiedad CanShutdown Virtual PC , interfaz IVMGuestOS
- Interfaz IVMGuestOS Pc virtual, propiedad CanShutdown
topic_type:
- apiref
api_name:
- IVMGuestOS.CanShutdown
- IVMGuestOS.get_CanShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29396178a376fb9649b2a953c4086c4c1460744cd1b4268645dba9877125cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594757"
---
# <a name="ivmguestoscanshutdown-property"></a>IVMGuestOS::CanShutdown, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Indica si el sistema operativo invitado se puede apagar correctamente (requiere componentes de integración).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CanShutdown(
  [out, retval] VARIANT_BOOL *canShutdown
);
```



## <a name="property-value"></a>Valor de propiedad

**VARIANT \_ TRUE** si el sistema operativo admite la operación de apagado y **VARIANT \_ FALSE** en caso contrario.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>           |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | La máquina virtual no está activada.<br/>   |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>              |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | No se encontró la máquina virtual.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

