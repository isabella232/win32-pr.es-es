---
title: Propiedad IVMMouse ScrollWheelPosition (VPCCOMInterfaces.h)
description: Ajusta la coordenada z del mouse (solo relativa).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- ScrollWheelPosition, propiedad Virtual PC
- Propiedad ScrollWheelPosition Virtual PC, interfaz IVMMouse
- IVMMouse interface Virtual PC , propiedad ScrollWheelPosition
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334190707cd43e63ce2244f410180b11bf6eb5018ff1482f073903adfb4b7878
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510655"
---
# <a name="ivmmousescrollwheelposition-property"></a>IVMMouse::ScrollWheelPosition, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ajusta la coordenada z del mouse (solo relativa).

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a>Valor de propiedad

Coordenada z que indica el número de píxeles que el mouse se va a mover a lo largo del eje Z.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                     | Significado                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                        | La operación se realizó correctamente.<br/>                                                                |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>             | La máquina virtual a la que está conectado este dispositivo del mouse no se está ejecutando actualmente.<br/>         |
| <dl> <dt>Máquina virtual \_ E \_ MOUSE \_ NOT \_ ACTIVE</dt> <dt>0xA0040800</dt> </dl>           | El dispositivo del mouse no se ha encendido o no está activo actualmente en la máquina virtual.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ USAR \_ COORDENADAS \_ ABSOLUTAS</dt> <dt>0xA0040801</dt> </dl> | No se puede establecer la posición de la rueda de desplazamiento cuando el dispositivo del mouse usa coordenadas absolutas.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                  | Se produjo un error inesperado.<br/>                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMmouse se define como \_ ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

