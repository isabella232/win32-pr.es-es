---
title: EM_LINEFROMCHAR mensaje (Winuser.h)
description: Obtiene el índice de la línea que contiene el índice de caracteres especificado en un control de edición multilínea.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_LINEFROMCHAR controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062164"
---
# <a name="em_linefromchar-message"></a>Mensaje EM \_ LINEFROMCHAR

Obtiene el índice de la línea que contiene el índice de caracteres especificado en un control de edición multilínea. Un índice de caracteres es el índice de base cero del carácter desde el principio del control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de caracteres del carácter contenido en la línea cuyo número se va a recuperar. Si este parámetro es -1, **EM \_ LINEFROMCHAR** recupera el número de línea de la línea actual (la línea que contiene el centro de referencia) o, si hay una selección, el número de línea de la línea que contiene el principio de la selección.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de línea de base cero de la línea que contiene el índice de caracteres especificado por *wParam*.

## <a name="remarks"></a>Observaciones

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Si el índice de caracteres es mayor que 64 000, use el [**mensaje EM \_ EXLINEFROMCHAR.**](em-exlinefromchar.md) Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

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

[**EM \_ EXLINEFROMCHAR**](em-exlinefromchar.md)
</dt> <dt>

[**EM \_ LINEINDEX**](em-lineindex.md)
</dt> </dl>

 

 





