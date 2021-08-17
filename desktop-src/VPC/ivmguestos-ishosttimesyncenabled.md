---
title: Propiedad IsHostTimeSyncEnabled de IVMGuestOS (VPCCOMInterfaces.h)
description: Indica si los componentes de integración de esta máquina virtual deben sincronizar el reloj del invitado con el reloj del host.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- Equipo virtual de la propiedad IsHostTimeSyncEnabled
- IsHostTimeSyncEnabled, propiedad Virtual PC, interfaz IVMGuestOS
- IVMGuestOS interface Virtual PC , IsHostTimeSyncEnabled property
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d64482db1c4d541204fa925d10e7e1d860347183f2229449937038782e22e06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136788"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a>IVMGuestOS::IsHostTimeSyncEnabled, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Indica si los componentes de integración de esta máquina virtual (VM) deben sincronizar el reloj del invitado con el reloj del host.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a>Valor de propiedad

Use **VARIANT \_ TRUE si** los componentes de integración de esta máquina virtual deben sincronizar el reloj del invitado con el reloj del host y VARIANT FALSE **\_ en** caso contrario.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>               |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | No se especifica el parámetro *isEnabled.*<br/> |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración es desconocida.<br/>               |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>           |



## <a name="remarks"></a>Comentarios

No puede cambiar esta configuración mientras la máquina virtual esté activa (es decir, en ejecución o en estado guardado).

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

 

