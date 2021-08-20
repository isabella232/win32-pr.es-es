---
title: Propiedad IVMVirtualPC HostInfo (VPCCOMInterfaces.h)
description: Recupera información sobre el equipo físico.
ms.assetid: 9efefea1-e608-48db-a91a-e3808b420fc2
keywords:
- HostInfo, propiedad Virtual PC
- Propiedad HostInfo Virtual PC, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , propiedad HostInfo
topic_type:
- apiref
api_name:
- IVMVirtualPC.HostInfo
- IVMVirtualPC.get_HostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438c42f02b76c4e4bf7647ba4b1921cc99d04f3d1c99d6004a8323823a2dfd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056563"
---
# <a name="ivmvirtualpchostinfo-property"></a>IVMVirtualPC::HostInfo, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera información sobre el equipo físico.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HostInfo(
  [out, retval] IVMHostInfo **hostInfo
);
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IVMHostInfo**](ivmhostinfo.md) que contiene información sobre el equipo host.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                | El parámetro es **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

