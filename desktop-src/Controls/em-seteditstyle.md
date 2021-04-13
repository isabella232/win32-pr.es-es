---
title: Mensaje EM_SETEDITSTYLE (RichEdit. h)
description: Establece las marcas de estilo de edición actuales para un control Rich Edit.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535056"
---
# <a name="em_seteditstyle-message"></a>\_Mensaje SETEDITSTYLE em

Establece las marcas de estilo de edición actuales para un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica una o más marcas de estilo de edición. Para obtener una lista de los valores posibles, consulte [**em \_ GETEDITSTYLE**](em-geteditstyle.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara formada por uno o varios de los valores de *wParam* . Solo se establecerán o se borrarán los valores especificados en esta máscara. Esto permite establecer o borrar una sola marca sin leer los Estados actuales de la marca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el estado de las marcas de estilo de edición después de que el control Rich Edit ha intentado implementar los cambios de estilo de edición. Las marcas de estilo de edición son un conjunto de marcas que indican el estilo de edición actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETEDITSTYLE em**](em-geteditstyle.md)
</dt> </dl>

 

 





