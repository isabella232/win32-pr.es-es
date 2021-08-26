---
title: TVM_GETISEARCHSTRING mensaje (Commctrl.h)
description: Recupera la cadena de búsqueda incremental para un control de vista de árbol.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79838b2b0d2f109216caf970d33d51b4a3c1369da7b1fc47f5a53e45c3ee82fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060245"
---
# <a name="tvm_getisearchstring-message"></a>Mensaje \_ GETISEARCHSTRING de TVM

Recupera la cadena de búsqueda incremental para un control de vista de árbol. El control de vista de árbol usa la cadena de búsqueda incremental para seleccionar un elemento basado en los caracteres especificados por el usuario. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetISearchString.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe la cadena de búsqueda incremental.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres de la cadena de búsqueda incremental.

## <a name="remarks"></a>Comentarios

**Advertencia de seguridad:** El uso incorrecto de este mensaje podría poner en peligro la seguridad del programa. Debe asignar un búfer lo suficientemente grande como para contener la cadena. En primer lugar, llame al mensaje **pasando NULL** *en lParam*. Esto devuelve el número de caracteres, excepto **NULL,** que son necesarios. A continuación, llame al mensaje una segunda vez para recuperar la cadena. Debe revisar [Consideraciones de seguridad: Controles de Windows Microsoft](sec-comctls.md) antes de continuar.

Si el control de vista de árbol no está en modo de búsqueda incremental, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVM \_ GETISEARCHSTRINGW** (Unicode) y **TVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





