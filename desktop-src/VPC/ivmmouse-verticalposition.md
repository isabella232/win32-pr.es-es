---
title: Propiedad IVMMouse VerticalPosition (VPCCOMInterfaces.h)
description: Coordenada Y absoluta del mouse.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- Propiedad VerticalPosition Virtual PC
- Propiedad VerticalPosition Virtual PC , interfaz IVMMouse
- IVMMouse interface Virtual PC , propiedad VerticalPosition
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
ms.openlocfilehash: 06f202a81e5d95909f1ec223087aceecb2a221c9836d1fcd799734f81a250141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344812"
---
# <a name="ivmmouseverticalposition-property"></a>IVMMouse::VerticalPosition, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la coordenada Y absoluta del mouse.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Valor de propiedad

Coordenada Y que indica la nueva posición del mouse. Cuando se usan coordenadas absolutas, este valor especifica la nueva coordenada Y del mouse. Cuando se usan coordenadas relativas, este valor especifica el número de píxeles que el mouse debe moverse en la dirección y.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                                                                                |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **NULL.**<br/>                                                                                                                   |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual a la que está conectado este dispositivo del mouse no se está ejecutando actualmente.<br/>                                                         |
| <dl> <dt>Máquina virtual \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Los componentes de integración deben instalarse para recuperar la posición del mouse o para establecer la posición del mouse cuando se usan coordenadas absolutas.<br/>       |
| <dl> <dt>Máquina virtual \_ E \_ USO DE COORDENADAS \_ \_ RELATIVAS</dt> <dt>0xA0040802</dt> </dl>   | El dispositivo del mouse está configurado actualmente para usar coordenadas relativas del mouse.<br/>                                                                         |
| <dl> <dt>Máquina virtual \_ E \_ MOUSE \_ NOT \_ ACTIVE</dt> <dt>0xA0040800</dt> </dl>             | Las coordenadas absolutas no se pueden recuperar si el dispositivo del mouse no está encendido o si no está activo actualmente en la máquina virtual.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                                                                                            |



## <a name="remarks"></a>Comentarios

Esta propiedad no se puede recuperar cuando se usan coordenadas relativas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMmouse se define como \_ ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

