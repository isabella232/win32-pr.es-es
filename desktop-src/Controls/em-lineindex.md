---
title: EM_LINEINDEX mensaje (Winuser.h)
description: Obtiene el índice de caracteres del primer carácter de una línea especificada en un control de edición multilínea.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_LINEINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062160"
---
# <a name="em_lineindex-message-winuserh"></a>EM_LINEINDEX mensaje (Winuser.h)

Obtiene el índice de caracteres del primer carácter de una línea especificada en un control de edición multilínea. Un índice de caracteres es el índice de base cero del carácter desde el principio del control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de línea de base cero. Un valor de -1 especifica el número de línea actual (la línea que contiene el centro de referencia).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de caracteres de la línea especificada en el parámetro *wParam* o es -1 si el número de línea especificado es mayor que el número de líneas del control de edición.

## <a name="remarks"></a>Observaciones

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ LINEFROMCHAR**](em-linefromchar.md)
</dt> </dl>

 

 





