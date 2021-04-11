---
title: Mensaje de EM_FILELINEINDEX (CommCtrl. h)
description: Obtiene el índice de carácter del primer carácter de una línea especificada en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX controles de mensajes de Windows
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
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150468"
---
# <a name="em_filelineindex-message-commctrlh"></a>Mensaje de EM_FILELINEINDEX (CommCtrl. h)

Obtiene el índice de carácter del primer carácter de una línea especificada en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla. Un índice de carácter es el índice de base cero del carácter desde el principio del control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de línea de base cero. Un valor de-1 especifica el número de línea actual (la línea que contiene el símbolo de intercalación).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de carácter de la línea especificada en el parámetro *wParam* , independientemente de cómo se muestran las líneas en la pantalla o es-1 si el número de línea especificado es mayor que el número de líneas del control de edición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_FILELINEFROMCHAR em**](em-filelinefromchar.md)
</dt> </dl>

 

 





