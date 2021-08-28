---
title: Propiedad IVMMouse HorizontalPosition (VPCCOMInterfaces.h)
description: Coordenada X absoluta del mouse.
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- Equipo virtual de la propiedad HorizontalPosition
- Propiedad HorizontalPosition Virtual PC, interfaz IVMMouse
- IVMMouse interface Virtual PC , propiedad HorizontalPosition
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2cb3fde1caff23845c653024d9c5e2859b0b7b5df8502dbaea167d3e969a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007155"
---
# <a name="ivmmousehorizontalposition-property"></a>IVMMouse::HorizontalPosition, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la coordenada X absoluta del mouse.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Valor de propiedad

Coordenada x que indica la nueva posición del mouse. Cuando se usan coordenadas absolutas, este valor especifica la nueva coordenada x del mouse. Cuando se usan coordenadas relativas, este valor especifica el número de píxeles que debe mover el mouse en la dirección x.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                                                                                |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **NULL.**<br/>                                                                                                                   |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual a la que está conectado este dispositivo del mouse no se está ejecutando actualmente.<br/>                                                         |
| <dl> <dt>Máquina virtual \_ LA \_ CARACTERÍSTICA DE \_ ADICIONES \_ NO \_ ESTÁ</dt> DISPONIBLE <dt>0XA0040505</dt> </dl> | Los componentes de integración deben instalarse para recuperar la posición del mouse o para establecer la posición del mouse cuando se usan coordenadas absolutas.<br/>       |
| <dl> <dt>Máquina virtual \_ E \_ USAR \_ COORDENADAS \_ RELATIVAS</dt> <dt>0xA0040802</dt> </dl>   | El dispositivo del mouse está configurado actualmente para usar coordenadas relativas del mouse.<br/>                                                                         |
| <dl> <dt>Máquina virtual \_ E \_ MOUSE \_ NOT \_ ACTIVE</dt> <dt>0xA0040800</dt> </dl>             | Las coordenadas absolutas no se pueden recuperar si el dispositivo del mouse no está encendido o si no está activo actualmente en la máquina virtual.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                                                                                            |



## <a name="remarks"></a>Comentarios

Esta propiedad no se puede recuperar cuando se usan coordenadas relativas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

