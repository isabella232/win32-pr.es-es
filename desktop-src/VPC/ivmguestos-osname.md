---
title: Propiedad IVMGuestOS OSName (VPCCOMInterfaces.h)
description: Nombre del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 6381fc15-a6ab-429b-809d-7f89e7ec666d
keywords:
- OSName, propiedad Virtual PC
- Propiedad OSName Virtual PC , interfaz IVMGuestOS
- Interfaz IVMGuestOS Pc virtual, propiedad OSName
topic_type:
- apiref
api_name:
- IVMGuestOS.OSName
- IVMGuestOS.get_OSName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5df969058facebd99e7438b10ed3021d9033df7f30874d4b1c23a8339cc9994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512425"
---
# <a name="ivmguestososname-property"></a>Propiedad IVMGuestOS::OSName

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el nombre del sistema operativo invitado que se ejecuta en la máquina virtual (VM).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_OSName(
  [out, retval] BSTR *guestOSName
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre completo (incluido el nombre del conjunto de datos) del sistema operativo invitado.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                        |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **NULL.**<br/>                           |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                               |
| <dl> <dt>Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                    |



## <a name="remarks"></a>Comentarios

La máquina virtual debe estar en ejecución (es decir, totalmente arrancada y no apagada) y los componentes de integración deben instalarse cuando se invoca este método.

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

 

