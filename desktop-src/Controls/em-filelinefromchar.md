---
title: EM_FILELINEFROMCHAR mensaje (CommCtrl.h)
description: Obtiene el índice de la línea que contiene el índice de caracteres especificado en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_FILELINEFROMCHAR controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d238117a9f2ba18ae838eec32d7dc2fa12ba0833f9cdee54ce2d1a2c998944
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915635"
---
# <a name="em_filelinefromchar-message"></a>Mensaje \_ EM FILELINEFROMCHAR

Obtiene el índice de la línea que contiene el índice de caracteres especificado en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla. Un índice de caracteres es el índice de base cero del carácter desde el principio del control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de caracteres del carácter contenido en la línea cuyo número se va a recuperar. Si este parámetro es -1, **EM \_ FILELINEFROMCHAR** recupera el número de línea de la línea actual (la línea que contiene el centro de referencia) o, si hay una selección, el número de línea de la línea que contiene el principio de la selección.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de línea de base cero de la línea que contiene el índice de caracteres especificado por *wParam,* independientemente de cómo se muestren las líneas en la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





