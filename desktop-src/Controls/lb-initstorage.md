---
title: Mensaje de LB_INITSTORAGE (Winuser. h)
description: Asigna memoria para almacenar los elementos del cuadro de lista. Este mensaje se usa antes de que una aplicación agregue un gran número de elementos a un cuadro de lista.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- LB_INITSTORAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490708"
---
# <a name="lb_initstorage-message"></a>\_Mensaje lb INITSTORAGE

Asigna memoria para almacenar los elementos del cuadro de lista. Este mensaje se usa antes de que una aplicación agregue un gran número de elementos a un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos que se van a agregar.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Cantidad de memoria, en bytes, que se va a asignar para las cadenas de elementos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el número total de elementos para los que se ha asignado previamente la memoria, es decir, el número total de elementos agregados por todos los mensajes del **\_ INITSTORAGE** del error de carga correctos.

Si se produce un error en el mensaje, el valor devuelto es LB \_ ERRSPACE.

Microsoft Windows NT 4,0: este mensaje no asigna la cantidad de memoria especificada; sin embargo, siempre devuelve el valor especificado en el parámetro *wParam* .

## <a name="remarks"></a>Observaciones

El mensaje **lb \_ INITSTORAGE** ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada de modo que los mensajes de [**lb \_ ADDSTRING**](lb-addstring.md), [**lb \_ INSERTSTRING**](lb-insertstring.md), [**lb \_ dir**](lb-dir.md)y [**lb \_ ADDFILE**](lb-addfile.md) posteriores tarden el menor tiempo posible. Puede usar estimaciones para los parámetros *wParam* e *lParam* . Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.

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

[**LB \_ ADDFILE**](lb-addfile.md)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**DIR de LB \_**](lb-dir.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





