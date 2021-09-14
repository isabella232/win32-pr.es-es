---
title: EM_SETCARETINDEX mensaje (CommCtrl.h)
description: Establece el valor de índice de base cero de la posición del elemento de diálogo en un control de edición.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETCARETINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062132"
---
# <a name="em_setcaretindex-message"></a>Mensaje \_ SETCARETINDEX DE EM

Establece el valor de índice de base cero de la posición del elemento de diálogo en un control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nuevo valor de índice de base cero de la posición del cursor de cursor.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Si el índice está fuera del intervalo del texto de un control de edición, el índice se ajustará para que quepa dentro del intervalo del texto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETCARETINDEX**](em-getcaretindex.md)
</dt> </dl>

 

 





