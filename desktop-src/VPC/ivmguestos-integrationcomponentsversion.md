---
title: Propiedad IVMGuestOS IntegrationComponentsVersion (VPCCOMInterfaces.h)
description: Recupera la versión de los componentes de integración instalados en el sistema operativo invitado.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- IntegrationComponentsVersion, propiedad Virtual PC
- IntegrationComponentsVersion, propiedad Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Pc virtual, propiedad IntegrationComponentsVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854cb86817f461085c72a437fa962649e50ab11b65a847d0756dc8e9c7b18177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999055"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a>Propiedad IVMGuestOS::IntegrationComponentsVersion

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la versión de los componentes de integración instalados en el sistema operativo invitado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a>Valor de propiedad

La versión.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                              | Significado                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                 | La operación se realizó correctamente.<br/>                                                     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                   | El parámetro es **NULL.**<br/>                                                        |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>           | No se encontró la máquina virtual.<br/>                                      |
| <dl> <dt>Máquina virtual \_ E \_ LAS \_ ADICIONES NO ESTÁN \_ DISPONIBLES</dt> <dt>0xA0040504</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual o la máquina virtual nunca se inició.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Se produjo un error inesperado.<br/>                                                 |



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

 

