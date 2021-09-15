---
description: Se envía a todas las ventanas de nivel superior cuando el sistema detecta más del 12,5 % del tiempo del sistema durante un intervalo de entre 30 y 60 segundos que se está dedicando a compactar la memoria. Esto indica que la memoria del sistema es baja.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: WM_COMPACTING mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466232"
---
# <a name="wm_compacting-message"></a>Mensaje \_ DE COMPACTACIÓN DE WM

Se envía a todas las ventanas de nivel superior cuando el sistema detecta más del 12,5 % del tiempo del sistema durante un intervalo de entre 30 y 60 segundos que se está dedicando a compactar la memoria. Esto indica que la memoria del sistema es baja.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> Este mensaje solo se proporciona por compatibilidad con aplicaciones basadas en Windows de 16 bits.

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La proporción de tiempo de unidad de procesamiento central (CPU) empleado actualmente por el sistema para compactar la memoria con el tiempo de CPU que el sistema dedica actualmente a realizar otras operaciones. Por ejemplo, 0x8000 representa el 50 por ciento del tiempo de CPU dedicado a compactar la memoria.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Cuando una aplicación recibe este mensaje, debe liberar toda la memoria posible, teniendo en cuenta el nivel actual de actividad de la aplicación y el número total de aplicaciones que se ejecutan en el sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Windows Visión general](windows.md)
</dt> </dl>

 

 
