---
title: LB_DELETESTRING mensaje (Winuser.h)
description: Elimina una cadena en un cuadro de lista.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061896"
---
# <a name="lb_deletestring-message"></a>Mensaje \_ DELETESTRING de LB

Elimina una cadena en un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la cadena que se va a eliminar.

Windows edición 95/Windows 98/Windows Desánimo (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un recuento de las cadenas restantes en la lista. El valor devuelto es LB ERR si el \_ *parámetro wParam* especifica un índice mayor que el número de elementos de la lista.

## <a name="remarks"></a>Observaciones

Si una aplicación crea el cuadro de lista con un estilo dibujado por el propietario pero sin el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LBS, el sistema envía un mensaje [**\_ DELETEITEM**](wm-deleteitem.md) de WM al propietario del cuadro de lista para que la aplicación pueda liberar los datos adicionales asociados al elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**DELETEITEM de WM \_**](wm-deleteitem.md)
</dt> </dl>

 

 





