---
title: Propiedad IVMGuestOS SuiteMask (VPCCOMInterfaces. h)
description: Recupera el SuiteMask del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Propiedad SuiteMask Virtual PC
- Propiedad SuiteMask Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad SuiteMask
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803842"
---
# <a name="ivmguestossuitemask-property"></a>IVMGuestOS:: SuiteMask (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el SuiteMask del sistema operativo invitado que se ejecuta en la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a>Valor de propiedad

Máscara del conjunto. Se admiten los siguientes valores de cadena.



| Value                                                                                   | Significado                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000004</dt> </dl> | Los componentes de Microsoft BackOffice están instalados.<br/>                                                                                                              |
| <dl> <dt>"0x00000400"</dt> </dl> | Windows Server 2003, Web Edition está instalado.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows Server 2003, Compute Cluster Edition está instalado.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server están instalados.<br/> |
| <dl> <dt>0x00000002</dt> </dl> | Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server están instalados.<br/>   |
| <dl> <dt>0x00000040</dt> </dl> | Windows XP Embedded está instalado.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition está instalado.<br/>                                                              |
| <dl> <dt>0x00000100</dt> </dl> | Escritorio remoto es compatible, pero solo se admite una sesión interactiva.<br/>                                                                                 |
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server se ha instalado en el sistema, pero es posible que se haya actualizado a otra versión de Windows.<br/>                                 |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor.<br/>                                                                  |
| <dl> <dt>0x00002000</dt> </dl> | Windows Storage Server 2003 R2 o Windows Storage Server 2003 está instalado.<br/>                                                                                 |
| <dl> <dt>0x00000010</dt> </dl> | Servicios de Escritorio remoto está instalado. Siempre se establece este valor.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Windows Home Server está instalado.<br/>                                                                                                                           |



 

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

 

