---
title: Mensaje EM_SELECTIONTYPE (RichEdit. h)
description: Determina el tipo de selección de un control Rich Edit.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535068"
---
# <a name="em_selectiontype-message"></a>\_Mensaje SELECTIONTYPE em

Determina el tipo de selección de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la selección está vacía, el valor devuelto es SEL \_ Empty.

Si la selección no está vacía, el valor devuelto es un conjunto de marcas que contienen uno o varios de los valores siguientes.



| Código devuelto                                                                                     | Descripción                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_texto SEL**</dt> </dl>        | Texto.<br/>                            |
| <dl> <dt>**SEL ( \_ objeto)**</dt> </dl>      | Al menos un objeto COM.<br/>         |
| <dl> <dt>**SEL \_ MULTIchar**</dt> </dl>   | Más de un carácter de texto.<br/> |
| <dl> <dt>**SEL \_ MULTIobject**</dt> </dl> | Más de un objeto COM.<br/>        |



 

## <a name="remarks"></a>Observaciones

Este mensaje es útil durante el procesamiento de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) para el elemento primario de un control Rich Edit no completo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**tamaño de WM \_**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

