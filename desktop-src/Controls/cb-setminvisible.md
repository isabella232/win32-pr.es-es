---
title: CB_SETMINVISIBLE mensaje (Commctrl.h)
description: Una aplicación envía un mensaje CB SETMINVISIBLE para establecer el número mínimo de elementos visibles en la lista desplegable \_ de un cuadro combinado.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- CB_SETMINVISIBLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9790c43141ef836c1dec86304f260b0490854b593b7005b594d2a718332296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063325"
---
# <a name="cb_setminvisible-message"></a>Mensaje \_ DE CB SETMINVISIBLE

Una aplicación envía un **mensaje \_ CB SETMINVISIBLE** para establecer el número mínimo de elementos visibles en la lista desplegable de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el número mínimo de elementos visibles.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje es correcto, el valor devuelto es **TRUE.** De lo contrario, el valor devuelto **es FALSE.**

## <a name="remarks"></a>Comentarios

Cuando el número de elementos de la lista desplegable es mayor que el mínimo, el cuadro combinado usa una barra de desplazamiento. De forma predeterminada, 30 es el número mínimo de elementos visibles.

Este mensaje se omite si el control de cuadro combinado tiene el estilo [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).

Para usar **CB \_ SETMINVISIBLE,** la aplicación debe especificar comctl32.dll versión 6 en el manifiesto. Para obtener más información, vea [Habilitar estilos visuales.](cookbook-overview.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ GETMINVISIBLE**](cb-getminvisible.md)
</dt> <dt>

[**ComboBox \_ SetMinVisible**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





