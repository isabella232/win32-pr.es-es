---
title: Mensaje de WM_CTLCOLORBTN (Winuser. h)
description: El \_ mensaje de CTLCOLORBTN de WM se envía a la ventana primaria de un botón antes de dibujar el botón. La ventana primaria puede cambiar los colores de texto y de fondo del botón. Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa este mensaje.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- WM_CTLCOLORBTN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995921"
---
# <a name="wm_ctlcolorbtn-message"></a>Mensaje de CTLCOLORBTN de WM \_

El mensaje de **\_ CTLCOLORBTN de WM** se envía a la ventana primaria de un botón antes de dibujar el botón. La ventana primaria puede cambiar los colores de texto y de fondo del botón. Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa este mensaje.


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**HDC** que especifica el identificador del contexto de presentación para el botón.

</dd> <dt>

*lParam* 
</dt> <dd>

**HWnd** que especifica el identificador del botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver un identificador a un pincel. El sistema utiliza el pincel para pintar el fondo del botón.

## <a name="remarks"></a>Observaciones

Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la función [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), la aplicación debe liberar el pincel. Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), no es necesario que la aplicación libere el pincel.

De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el botón. Los botones con los estilos de [**\_ pulsador BS**](button-styles.md), [**BS \_ DEFPUSHBUTTON**](button-styles.md)o [**BS \_ PUSHLIKE**](button-styles.md) no usan el pincel devuelto. Los botones con estos estilos siempre se dibujan con los colores del sistema predeterminados. Dibujar botones de reenvío requiere varios pinceles diferentes: la esfera, el resaltado y la sombra, pero el mensaje de **\_ CTLCOLORBTN de WM** permite que solo se devuelva un pincel. Para proporcionar una apariencia personalizada para botones de tecla de reenvío, use un botón dibujado por el propietario. Para obtener más información, vea [crear controles de Owner-Drawn](user-controls-intro.md).

El mensaje de **\_ CTLCOLORBTN de WM** nunca se envía entre subprocesos. Solo se envía dentro de un subproceso.

El color del texto de una casilla o un botón de radio se aplica al cuadro o botón, su marca de verificación y el texto. El rectángulo de foco de estos botones sigue siendo el color predeterminado del sistema (normalmente negro). El color de texto de un cuadro de grupo se aplica al texto, pero no a la línea que define el cuadro. El color del texto de un botón de la tecla de reenvío solo se aplica a su rectángulo de foco; no afecta al color del texto.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado. \_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

