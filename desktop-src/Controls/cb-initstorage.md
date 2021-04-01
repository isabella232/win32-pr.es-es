---
title: Mensaje de CB_INITSTORAGE (Winuser. h)
description: Una aplicación envía el \_ mensaje de INITSTORAGE CB antes de agregar un gran número de elementos a la parte de cuadro de lista de un cuadro combinado. Este mensaje asigna memoria para almacenar los elementos del cuadro de lista.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- CB_INITSTORAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150267"
---
# <a name="cb_initstorage-message"></a>\_Mensaje INITSTORAGE de CB

Una aplicación envía el mensaje de **\_ INITSTORAGE CB** antes de agregar un gran número de elementos a la parte de cuadro de lista de un cuadro combinado. Este mensaje asigna memoria para almacenar los elementos del cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos que se van a agregar.

</dd> <dt>

*lParam* 
</dt> <dd>

Cantidad de memoria que se va a asignar para las cadenas de elementos, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el número total de elementos para los que se ha asignado previamente la memoria, es decir, el número total de elementos agregados por todos los mensajes del **\_ INITSTORAGE** del elemento CB correctos.

Si se produce un error en el mensaje, el valor devuelto es CB \_ ERRSPACE.

El mensaje asigna memoria y devuelve los valores correctos y de error descritos anteriormente.

## <a name="remarks"></a>Observaciones

El mensaje de **\_ INITSTORAGE de CB** ayuda a acelerar la inicialización de los cuadros combinados que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes de la [**\_ dir**](cb-dir.md) [**CB \_ ADDSTRING**](cb-addstring.md), [**CB \_ INSERTSTRING**](cb-insertstring.md)y CB posteriores tarden el menor tiempo posible. Puede usar estimaciones para los parámetros *wParam* e *lParam* . Si sobrestima, se asigna la memoria adicional, si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**\_directorio CB**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





