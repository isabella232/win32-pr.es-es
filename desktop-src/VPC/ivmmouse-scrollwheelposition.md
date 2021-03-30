---
title: Propiedad IVMMouse ScrollWheelPosition (VPCCOMInterfaces. h)
description: Ajusta la coordenada z del mouse (solo relativo).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Propiedad ScrollWheelPosition Virtual PC
- Propiedad ScrollWheelPosition Virtual PC, interfaz IVMMouse
- Interfaz IVMMouse Virtual PC, propiedad ScrollWheelPosition
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
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803740"
---
# <a name="ivmmousescrollwheelposition-property"></a>IVMMouse:: ScrollWheelPosition (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ajusta la coordenada z del mouse (solo relativo).

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a>Valor de propiedad

Coordenada z que indica el número de píxeles que se va a desplace el mouse a lo largo del eje z.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                     | Significado                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                        | La operación se realizó correctamente.<br/>                                                                |
| <dl> <dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt> </dl>             | La máquina virtual a la que está conectado este dispositivo de mouse no se está ejecutando actualmente.<br/>         |
| <dl> <dt>Máquina virtual \_ E \_ mouse \_ no \_ activo</dt> <dt>0xA0040800</dt> </dl>           | El dispositivo de mouse no se ha encendido o no está activo actualmente en la máquina virtual.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ usar \_ \_ coordenadas absolutas</dt> <dt>0xA0040801</dt> </dl> | No se puede establecer la posición de la rueda de desplazamiento cuando el dispositivo del mouse usa coordenadas absolutas.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                  | Se produjo un error inesperado.<br/>                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse se define como ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

