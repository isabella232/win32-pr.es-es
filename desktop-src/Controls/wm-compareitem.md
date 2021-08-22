---
title: WM_COMPAREITEM mensaje (Winuser.h)
description: Se envía para determinar la posición relativa de un nuevo elemento en la lista ordenada de un cuadro combinado dibujado por el propietario o un cuadro de lista.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- WM_COMPAREITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819df3c4dd36c784ef5747d4aa4cdf688b3a48dbd052254192a7c98574bbfa94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655775"
---
# <a name="wm_compareitem-message"></a>Mensaje \_ COMPAREITEM de WM

Se envía para determinar la posición relativa de un nuevo elemento en la lista ordenada de un cuadro combinado dibujado por el propietario o un cuadro de lista. Cada vez que la aplicación agrega un nuevo elemento, el sistema envía este mensaje al propietario de un cuadro combinado o cuadro de lista creado con el estilo SORT o [**LBS \_ SORT**](list-box-styles.md) de [**CBS. \_**](combo-box-styles.md)


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el identificador del control que envió el **mensaje \_ COMPAREITEM de WM.**

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) que contiene los identificadores y los datos proporcionados por la aplicación para dos elementos del cuadro combinado o de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto indica la posición relativa de los dos elementos. Puede ser cualquiera de los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**Valor**</dt> </dl> | Significado<br/>                                           |
| <dl> <dt>**-1**</dt> </dl>    | El elemento 1 precede al elemento 2 en el orden ordenado.<br/>       |
| <dl> <dt>**0**</dt> </dl>     | Los elementos 1 y 2 son equivalentes en el orden ordenado.<br/> |
| <dl> <dt>**1**</dt> </dl>     | El elemento 1 sigue el elemento 2 en el orden ordenado.<br/>        |



 

## <a name="remarks"></a>Comentarios

Cuando el propietario de un cuadro combinado o un cuadro de lista dibujado por el propietario recibe este mensaje, el propietario devuelve un valor que indica cuál de los elementos especificados por la estructura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) aparecerá antes que el otro. Normalmente, el sistema envía este mensaje varias veces hasta que determina la posición exacta del nuevo elemento.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **un BOOL** y devolver el valor directamente. Se omite el valor MSGRESULT de DWL establecido por la función \_ [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

