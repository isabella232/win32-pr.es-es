---
description: Se envía a todas las ventanas de nivel superior cuando el sistema detecta más del 12,5 por ciento de la hora del sistema durante un intervalo de 30 a 60 segundos en la compactación de la memoria. Esto indica que la memoria del sistema es baja.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: Mensaje de WM_COMPACTING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706673"
---
# <a name="wm_compacting-message"></a>\_Mensaje de compactación de WM

Se envía a todas las ventanas de nivel superior cuando el sistema detecta más del 12,5 por ciento de la hora del sistema durante un intervalo de 30 a 60 segundos en la compactación de la memoria. Esto indica que la memoria del sistema es baja.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> Este mensaje se proporciona solo para ofrecer compatibilidad con aplicaciones basadas en Windows de 16 bits.

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La proporción de tiempo de la unidad central de procesamiento (CPU) empleada actualmente por el sistema que compacta la memoria en el tiempo de CPU empleado actualmente por el sistema que realiza otras operaciones. Por ejemplo, 0x8000 representa el 50 por ciento del tiempo de CPU empleado en compactar la memoria.

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
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Windows](windows.md)
</dt> </dl>

 

 
