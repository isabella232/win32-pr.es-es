---
title: Mensaje de EM_FILELINEFROMCHAR (CommCtrl. h)
description: Obtiene el índice de la línea que contiene el índice de carácter especificado en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_FILELINEFROMCHAR controles de mensajes de Windows
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
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491224"
---
# <a name="em_filelinefromchar-message"></a>\_Mensaje FILELINEFROMCHAR em

Obtiene el índice de la línea que contiene el índice de carácter especificado en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla. Un índice de carácter es el índice de base cero del carácter desde el principio del control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de carácter del carácter incluido en la línea cuyo número se va a recuperar. Si este parámetro es-1, **em \_ FILELINEFROMCHAR** recupera el número de línea de la línea actual (la línea que contiene el símbolo de intercalación) o, si hay una selección, el número de línea de la línea que contiene el principio de la selección.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de línea de base cero de la línea que contiene el índice de caracteres especificado por *wParam*, independientemente de cómo se muestren las líneas en la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_FILELINEINDEX em**](em-filelineindex.md)
</dt> </dl>

 

 





