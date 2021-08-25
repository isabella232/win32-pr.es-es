---
title: Propiedad IVMVirtualMachine GuestOS (VPCCOMInterfaces.h)
description: Recupera el sistema operativo invitado para esta máquina virtual.
ms.assetid: 9cca2a4a-e3bb-4c41-873c-e5bc4863c415
keywords:
- Equipo virtual de la propiedad GuestOS
- Propiedad de GuestOS Virtual PC, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , propiedad GuestOS
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GuestOS
- IVMVirtualMachine.get_GuestOS
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5cb9c5fdfb2b6bd8c77eb7b19e421c666a1d4696bdb1b13ba32bfd4218b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006815"
---
# <a name="ivmvirtualmachineguestos-property"></a>IVMVirtualMachine::GuestOS, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el sistema operativo invitado para esta máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_GuestOS(
  [out, retval] IVMGuestOS **guestOS
);
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IVMGuestOS.**](ivmguestos.md)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración es desconocida.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

