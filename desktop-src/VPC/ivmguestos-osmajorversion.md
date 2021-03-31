---
title: Propiedad IVMGuestOS OSMajorVersion (VPCCOMInterfaces. h)
description: La versión principal del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: c9be8b4e-15fe-402d-8396-30be6b065b73
keywords:
- Propiedad OSMajorVersion Virtual PC
- Propiedad OSMajorVersion Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad OSMajorVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMajorVersion
- IVMGuestOS.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f76e3105c4917141c8a5304082d55f383ee947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490450"
---
# <a name="ivmguestososmajorversion-property"></a>IVMGuestOS:: OSMajorVersion (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera la versión principal del sistema operativo invitado que se ejecuta en la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_OSMajorVersion(
  [out, retval] BSTR *majorVersion
);
```



## <a name="property-value"></a>Valor de propiedad

Versión principal.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                        |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **null**.<br/>                           |
| <dl> <dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                               |
| <dl> <dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                    |



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

 

