---
title: Mensaje de LB_DELETESTRING (Winuser. h)
description: Elimina una cadena de un cuadro de lista.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905476"
---
# <a name="lb_deletestring-message"></a>\_Mensaje lb DELETESTRING

Elimina una cadena de un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la cadena que se va a eliminar.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un recuento de las cadenas que permanecen en la lista. El valor devuelto es LB \_ Err si el parámetro *wParam* especifica un índice mayor que el número de elementos de la lista.

## <a name="remarks"></a>Observaciones

Si una aplicación crea el cuadro de lista con un estilo dibujado por el propietario pero sin el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) , el sistema envía un mensaje de [**WM \_ DELETEITEM**](wm-deleteitem.md) al propietario del cuadro de lista para que la aplicación pueda liberar cualquier dato adicional asociado al elemento.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





