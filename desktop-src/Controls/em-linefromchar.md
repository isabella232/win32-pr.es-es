---
title: Mensaje de EM_LINEFROMCHAR (Winuser. h)
description: Obtiene el índice de la línea que contiene el índice de carácter especificado en un control de edición multilínea.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_LINEFROMCHAR controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150140"
---
# <a name="em_linefromchar-message"></a>\_Mensaje LINEFROMCHAR em

Obtiene el índice de la línea que contiene el índice de carácter especificado en un control de edición multilínea. Un índice de carácter es el índice de base cero del carácter desde el principio del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de carácter del carácter incluido en la línea cuyo número se va a recuperar. Si este parámetro es-1, **em \_ LINEFROMCHAR** recupera el número de línea de la línea actual (la línea que contiene el símbolo de intercalación) o, si hay una selección, el número de línea de la línea que contiene el principio de la selección.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de línea de base cero de la línea que contiene el índice de caracteres especificado por *wParam*.

## <a name="remarks"></a>Observaciones

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Si el índice de caracteres es mayor que 64.000, use el mensaje [**\_ EXLINEFROMCHAR em**](em-exlinefromchar.md) . Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_EXLINEFROMCHAR em**](em-exlinefromchar.md)
</dt> <dt>

[**\_LINEINDEX em**](em-lineindex.md)
</dt> </dl>

 

 





