---
description: Se envía a una ventana que el usuario está cambiando de tamaño. Al procesar este mensaje, una aplicación puede supervisar el tamaño y la posición del rectángulo de arrastre y, si es necesario, cambiar su tamaño o posición.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: Mensaje de WM_SIZING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813867"
---
# <a name="wm_sizing-message"></a>Mensaje de ajuste de tamaño de WM \_

Se envía a una ventana que el usuario está cambiando de tamaño. Al procesar este mensaje, una aplicación puede supervisar el tamaño y la posición del rectángulo de arrastre y, si es necesario, cambiar su tamaño o posición.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Borde de la ventana a la que se va a ajustar el tamaño. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                         | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <dt>**WMSZ \_ INFERIOR**</dt> <dt>6</dt> </dl>                | Borde inferior<br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt> </dl>    | Esquina inferior izquierda<br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt> </dl> | Esquina inferior derecha<br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <dt>**WMSZ \_ IZQUIERDA**</dt> <dt>1</dt> </dl>                      | Borde izquierdo<br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <dt>**WMSZ \_ DERECHA**</dt> <dt>2</dt> </dl>                   | Borde derecho<br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <dt>**WMSZ \_**</dt>Los <dt>3</dt> principales </dl>                         | Borde superior<br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <dt>**WMSZ \_ Lado izquierdo**</dt> <dt>4</dt> </dl>             | Esquina superior izquierda<br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <dt>**WMSZ \_**</dt> <dt>5</dt> de la derecha </dl>          | Esquina superior derecha<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) con las coordenadas de pantalla del rectángulo de arrastre. Para cambiar el tamaño o la posición del rectángulo de arrastre, una aplicación debe cambiar los miembros de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver **true** si procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**movimiento de WM \_**](wm-moving.md)
</dt> <dt>

[**tamaño de WM \_**](wm-size.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
