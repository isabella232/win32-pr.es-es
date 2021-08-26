---
title: EM_FILELINEINDEX mensaje (CommCtrl.h)
description: Obtiene el índice de caracteres del primer carácter de una línea especificada en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c4bd1f21ee6bcdf7bec56828ea9c2996c837def614c0c537ef83ee053ebfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915615"
---
# <a name="em_filelineindex-message-commctrlh"></a>EM_FILELINEINDEX mensaje (CommCtrl.h)

Obtiene el índice de caracteres del primer carácter de una línea especificada en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla. Un índice de caracteres es el índice de base cero del carácter desde el principio del control de edición.

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

El valor devuelto es el índice de caracteres de la línea especificada en el parámetro *wParam,* independientemente de cómo se muestren las líneas en la pantalla, o es -1 si el número de línea especificado es mayor que el número de líneas del control de edición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ FILELINEFROMCHAR**](em-filelinefromchar.md)
</dt> </dl>

 

 





