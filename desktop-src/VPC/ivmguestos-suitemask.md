---
title: Propiedad IVMGuestOS SuiteMask (VPCCOMInterfaces.h)
description: Recupera la máscara de conjunto del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- SuiteMask, propiedad Virtual PC
- SuiteMask, propiedad Virtual PC, interfaz IVMGuestOS
- IVMGuestOS interface Virtual PC , SuiteMask property
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
ms.openlocfilehash: 22075c68ef30fda7360f25e76c84dbffbf7e306335a0ef20bda45559cb6dac09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472304"
---
# <a name="ivmguestossuitemask-property"></a>IVMGuestOS::SuiteMask, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la máscara de conjunto del sistema operativo invitado que se ejecuta en la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a>Valor de propiedad

Máscara del conjunto de datos. Se admiten los siguientes valores de cadena.



| Value                                                                                   | Significado                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"0x00000004"</dt> </dl> | Los componentes de Microsoft BackOffice están instalados.<br/>                                                                                                              |
| <dl> <dt>"0x00000400"</dt> </dl> | Windows Server 2003, Web Edition está instalado.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows Server 2003, Compute Cluster Edition está instalado.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows Datacenter Server 2000.<br/> |
| <dl> <dt>"0x00000002"</dt> </dl> | Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server está instalado.<br/>   |
| <dl> <dt>"0x00000040"</dt> </dl> | Windows XP Embedded está instalado.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Windows Vista Home Premium, Windows Vista Home Basic o Windows xp Home Edition está instalado.<br/>                                                              |
| <dl> <dt>"0x00000100"</dt> </dl> | Escritorio remoto se admite, pero solo se admite una sesión interactiva.<br/>                                                                                 |
| <dl> <dt>"0x00000001"</dt> </dl> | Microsoft Small Business Server se instaló una vez en el sistema, pero puede que se haya actualizado a otra versión de Windows.<br/>                                 |
| <dl> <dt>"0x00000020"</dt> </dl> | Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor.<br/>                                                                  |
| <dl> <dt>"0x00002000"</dt> </dl> | Windows Storage Server 2003 R2 o Windows Storage Server 2003 está instalado.<br/>                                                                                 |
| <dl> <dt>"0x00000010"</dt> </dl> | Servicios de Escritorio remoto está instalado. Este valor siempre se establece.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Windows El servidor principal está instalado.<br/>                                                                                                                           |



 

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                        |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **NULL.**<br/>                           |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                               |
| <dl> <dt>Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                    |



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

 

