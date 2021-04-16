---
title: Mensaje de WM_COMPAREITEM (Winuser. h)
description: Se envía para determinar la posición relativa de un nuevo elemento en la lista ordenada de un cuadro combinado dibujado por el propietario o un cuadro de lista.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- WM_COMPAREITEM controles de mensajes de Windows
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
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489005"
---
# <a name="wm_compareitem-message"></a>Mensaje de COMPAREITEM de WM \_

Se envía para determinar la posición relativa de un nuevo elemento en la lista ordenada de un cuadro combinado dibujado por el propietario o un cuadro de lista. Cada vez que la aplicación agrega un nuevo elemento, el sistema envía este mensaje al propietario de un cuadro combinado o un cuadro de lista creado con el estilo de [**\_ ordenación**](list-box-styles.md) [**CBS \_**](combo-box-styles.md) o lbs.


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el identificador del control que envió el mensaje de **\_ COMPAREITEM de WM** .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**compareitemstruct (**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) que contiene los identificadores y los datos proporcionados por la aplicación para dos elementos en el cuadro combinado o de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto indica la posición relativa de los dos elementos. Puede ser cualquiera de los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**Value**</dt> </dl> | Significado<br/>                                           |
| <dl> <dt>**-1**</dt> </dl>    | El elemento 1 precede al elemento 2 en el criterio de ordenación.<br/>       |
| <dl> <dt>**0,1**</dt> </dl>     | Los elementos 1 y 2 son equivalentes en el criterio de ordenación.<br/> |
| <dl> <dt>**1**</dt> </dl>     | El elemento 1 sigue el elemento 2 en el criterio de ordenación.<br/>        |



 

## <a name="remarks"></a>Observaciones

Cuando el propietario de un cuadro combinado dibujado por el propietario o un cuadro de lista recibe este mensaje, el propietario devuelve un valor que indica cuál de los elementos especificados por la estructura [**compareitemstruct (**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) aparecerá antes que el otro. Normalmente, el sistema envía este mensaje varias veces hasta que determina la posición exacta del nuevo elemento.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un **booleano** y devolver el valor directamente. \_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**COMPAREITEMSTRUCT (**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

