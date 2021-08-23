---
title: EM_GETSELTEXT mensaje (Richedit.h)
description: Recupera el texto seleccionado actualmente en un control de edición enriquecido.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- EM_GETSELTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540567f1b52c936ad085acac8e0374fdb0a912bae06480632263f9676f2948e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019503"
---
# <a name="em_getseltext-message"></a>Mensaje \_ EM GETSELTEXT

Recupera el texto seleccionado actualmente en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que recibe el texto seleccionado. La aplicación que realiza la llamada debe asegurarse de que el búfer sea lo suficientemente grande como para contener el texto seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el número de caracteres copiados, sin incluir el carácter nulo de terminación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





