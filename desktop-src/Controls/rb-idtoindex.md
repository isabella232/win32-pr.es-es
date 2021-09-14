---
title: RB_IDTOINDEX mensaje (Commctrl.h)
description: Convierte un identificador de banda en un índice de banda en un control rebar.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- RB_IDTOINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7acd85862bc4787a6b32d2fdd3c897a52913b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167325"
---
# <a name="rb_idtoindex-message"></a>Mensaje \_ IDTOINDEX de RB

Convierte un identificador de banda en un índice de banda en un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador definido por la aplicación de la banda en cuestión. Este es el valor que se pasó en el **miembro wID** de la [**estructura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) cuando se insertó la banda.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de banda de base cero si se realiza correctamente o -1 en caso contrario. Si existen identificadores de banda duplicados, se devuelve el primero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





