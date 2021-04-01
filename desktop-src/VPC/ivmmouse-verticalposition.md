---
title: IVMMouse propiedad VerticalPosition (VPCCOMInterfaces. h)
description: Coordenada y absoluta del mouse.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- Propiedad VerticalPosition Virtual PC
- Propiedad VerticalPosition Virtual PC, interfaz IVMMouse
- Interfaz IVMMouse Virtual PC, propiedad VerticalPosition
topic_type:
- apiref
api_name:
- IVMMouse.VerticalPosition
- IVMMouse.get_VerticalPosition
- IVMMouse.put_VerticalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64712f557a3fcd59181e8ce65d835b630da68e48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997042"
---
# <a name="ivmmouseverticalposition-property"></a>IVMMouse:: VerticalPosition (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera la coordenada y absoluta del mouse.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Valor de propiedad

Coordenada y que indica la nueva posición del mouse. Cuando se usan coordenadas absolutas, este valor especifica la nueva coordenada y del mouse. Cuando se usan coordenadas relativas, este valor especifica el número de píxeles que el mouse debe moverse en la dirección y.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                                                                                |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **null**.<br/>                                                                                                                   |
| <dl> <dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual a la que está conectado este dispositivo de mouse no se está ejecutando actualmente.<br/>                                                         |
| <dl> <dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt> </dl> | Los componentes de integración deben instalarse para recuperar la posición del mouse o para establecer la posición del mouse cuando se usan coordenadas absolutas.<br/>       |
| <dl> <dt>Máquina virtual \_ E \_ usar \_ \_ coordenadas relativas</dt> <dt>0xA0040802</dt> </dl>   | El dispositivo de mouse está establecido actualmente para usar coordenadas relativas del mouse.<br/>                                                                         |
| <dl> <dt>Máquina virtual \_ E \_ mouse \_ no \_ activo</dt> <dt>0xA0040800</dt> </dl>             | No se pueden recuperar las coordenadas absolutas si el dispositivo del mouse no está encendido o si no está activo actualmente en la máquina virtual.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                                                                                            |



## <a name="remarks"></a>Observaciones

No se puede recuperar esta propiedad cuando se usan coordenadas relativas.

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

 

