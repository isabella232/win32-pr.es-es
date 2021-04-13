---
title: Propiedad IVMGuestOS HeartbeatPercentage (VPCCOMInterfaces. h)
description: Porcentaje de latidos esperados recibidos en el último minuto.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Propiedad HeartbeatPercentage Virtual PC
- Propiedad HeartbeatPercentage Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad HeartbeatPercentage
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
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535187"
---
# <a name="ivmguestosheartbeatpercentage-property"></a>IVMGuestOS:: HeartbeatPercentage (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                 | La operación se realizó correctamente.<br/>                                                                                                            |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                   | El parámetro es **null**.<br/>                                                                                                               |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>           | La configuración es desconocida.<br/>                                                                                                            |
| <dl> <dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt> </dl>      | La máquina virtual (VM) debe estar en ejecución para esta operación.<br/>                                                                             |
| <dl> <dt>Máquina virtual \_ E/s \_ \_ no \_ DISP</dt> <dt>0xA0040504</dt> </dl> | La máquina virtual no se ha iniciado completamente, la característica componentes de integración no está instalada o la versión instalada no admite esta característica.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>           | Se produjo un error inesperado.<br/>                                                                                                        |



## <a name="remarks"></a>Observaciones

Los componentes de integración enviarán un latido periódico a Windows Virtual PC mientras se ejecuta el sistema operativo invitado. Si el sistema operativo invitado está muy cargado, es posible que Windows Virtual PC reciba menos latidos de lo esperado. Si el porcentaje de latido desciende a cero, es posible que el sistema operativo invitado no responda o se bloquee. La máquina virtual debe estar en ejecución (es decir, completamente arrancada y sin apagar) y los componentes de integración deben instalarse cuando se invoca esta propiedad.

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

 

