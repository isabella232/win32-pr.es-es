---
description: Se envía a una ventana en la que el usuario está redimensionando el tamaño. Al procesar este mensaje, una aplicación puede supervisar el tamaño y la posición del rectángulo de arrastre y, si es necesario, cambiar su tamaño o posición.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: WM_SIZING mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251648"
---
# <a name="wm_sizing-message"></a>Mensaje \_ wm SIZING

Se envía a una ventana en la que el usuario está redimensionando el tamaño. Al procesar este mensaje, una aplicación puede supervisar el tamaño y la posición del rectángulo de arrastre y, si es necesario, cambiar su tamaño o posición.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Borde de la ventana a la que se va a dimensionado. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                         | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <dt>**WMSZ \_ INFERIOR**</dt> <dt>6</dt> </dl>                | Borde inferior<br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt> </dl>    | Esquina inferior izquierda<br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt> </dl> | Esquina inferior derecha<br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <dt>**WMSZ \_ LEFT**</dt> <dt>1</dt> </dl>                      | Borde izquierdo<br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <dt>**WMSZ \_ DERECHA**</dt> <dt>2</dt> </dl>                   | Borde derecho<br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <dt>**WMSZ \_ TOP**</dt> <dt>3</dt> </dl>                         | Borde superior<br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <dt>**WMSZ \_ TOPLEFT**</dt> <dt>4</dt> </dl>             | Esquina superior izquierda<br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <dt>**WMSZ \_ TOPRIGHT**</dt> <dt>5</dt> </dl>          | Esquina superior derecha<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**RECT**](/previous-versions//dd162897(v=vs.85)) con las coordenadas de pantalla del rectángulo de arrastre. Para cambiar el tamaño o la posición del rectángulo de arrastre, una aplicación debe cambiar los miembros de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver **TRUE** si procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**MOVIMIENTO DE \_ WM**](wm-moving.md)
</dt> <dt>

[**TAMAÑO \_ DE WM**](wm-size.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
