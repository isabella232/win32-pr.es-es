---
title: LB_GETITEMDATA mensaje (Winuser.h)
description: Obtiene el valor definido por la aplicación asociado al elemento de cuadro de lista especificado.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- LB_GETITEMDATA controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfdb091fb98c0cf448af1cf5f554f7d0db2b03f53826154f7d62f2f6b27b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019343"
---
# <a name="lb_getitemdata-message"></a>Mensaje \_ GETITEMDATA de LB

Obtiene el valor definido por la aplicación asociado al elemento de cuadro de lista especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el valor asociado al elemento o LB \_ ERR si se produce un error. Si el elemento está en un cuadro de lista dibujado por el propietario y se creó sin el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LB, este valor estaba en el parámetro *lParam* del mensaje [**LB \_ ADDSTRING**](lb-addstring.md) o [**LB \_ INSERTSTRING**](lb-insertstring.md) que agregó el elemento al cuadro de lista. De lo contrario, es el valor de *lParam* del [**mensaje LB \_ SETITEMDATA.**](lb-setitemdata.md)

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**LB \_ SETITEMDATA**](lb-setitemdata.md)
</dt> </dl>

 

 





