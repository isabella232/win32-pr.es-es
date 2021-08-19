---
title: Propiedad HeartbeatPercentage de IVMGuestOS (VPCCOMInterfaces.h)
description: Porcentaje de latidos esperados recibidos en el último minuto.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- HeartbeatPercentage, propiedad Virtual PC
- HeartbeatPercentage, propiedad De PC virtual, interfaz IVMGuestOS
- Interfaz IVMGuestOS Pc virtual, propiedad HeartbeatPercentage
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1415b9d59e28e5658dc5b54a1a6d118e0b12a77b3208978448afb2b336f313e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753452"
---
# <a name="ivmguestosheartbeatpercentage-property"></a>IVMGuestOS::HeartbeatPercentage, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el porcentaje de latidos esperados recibidos en el último minuto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a>Valor de propiedad

Porcentaje de latidos esperados recibidos en el último minuto.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                              | Significado                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                 | La operación se realizó correctamente.<br/>                                                                                                            |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                   | El parámetro es **NULL.**<br/>                                                                                                               |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>           | La configuración es desconocida.<br/>                                                                                                            |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>      | La máquina virtual (VM) debe estar en ejecución para esta operación.<br/>                                                                             |
| <dl> <dt>Máquina virtual \_ LAS \_ ADICIONES \_ NO ESTÁN \_ DISPONIBLES</dt> <dt>0XA0040504</dt> </dl> | La máquina virtual no está totalmente arrancada, la característica de componentes de integración no está instalada o la versión instalada no admite esta característica.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Se produjo un error inesperado.<br/>                                                                                                        |



## <a name="remarks"></a>Comentarios

Los componentes de integración enviarán un latido periódico a Windows virtual mientras se ejecuta el sistema operativo invitado. Si el sistema operativo invitado está muy cargado, es posible que Windows Virtual PC reciba menos latidos de los esperados. Si el porcentaje de latidos cae a cero, es posible que el sistema operativo invitado no responda o se bloquea. La máquina virtual debe estar en ejecución (es decir, arrancar completamente y no apagarse) y los componentes de integración deben instalarse cuando se invoca esta propiedad.

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

 

