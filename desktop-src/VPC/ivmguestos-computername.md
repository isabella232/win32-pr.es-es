---
title: Propiedad ComputerName de IVMGuestOS (VPCCOMInterfaces.h)
description: Nombre del equipo del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: b35fa1a1-e105-43e6-9a2f-a5c7e71772cf
keywords:
- Equipo virtual de la propiedad ComputerName
- Propiedad ComputerName Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Pc virtual, propiedad ComputerName
topic_type:
- apiref
api_name:
- IVMGuestOS.ComputerName
- IVMGuestOS.get_ComputerName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6bb741c0196c79afb758ecd0567c6f334bdd574eb06b901a11e3d48b1efdc01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653455"
---
# <a name="ivmguestoscomputername-property"></a>IVMGuestOS::ComputerName, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el nombre de equipo del sistema operativo invitado que se ejecuta en la máquina virtual (VM).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ComputerName(
  [out, retval] BSTR *guestComputerName
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre del equipo del sistema operativo invitado.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                        |
| <dl> <dt>E \_ Invalidarg</dt> <dt>0x80000003</dt> </dl>                         | El parámetro no es válido o no se ha especificado.<br/>         |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                               |
| <dl> <dt>Máquina virtual \_ LA \_ CARACTERÍSTICA DE \_ ADICIONES \_ NO \_ ESTÁ</dt> DISPONIBLE <dt>0XA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                    |



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

 

