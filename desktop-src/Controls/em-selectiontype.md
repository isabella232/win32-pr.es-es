---
title: EM_SELECTIONTYPE mensaje (Richedit.h)
description: Determina el tipo de selección de un control de edición enriquecido.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE controles de Windows mensaje
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
ms.openlocfilehash: 1b79cb36759c857cea280b1c4beb5a476fa27a794f1f9985e1d259c345a9dc4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437845"
---
# <a name="em_selectiontype-message"></a>Mensaje \_ EM SELECTIONTYPE

Determina el tipo de selección de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la selección está vacía, el valor devuelto es SEL \_ EMPTY.

Si la selección no está vacía, el valor devuelto es un conjunto de marcas que contienen uno o varios de los valores siguientes.



| Código devuelto                                                                                     | Descripción                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**TEXTO \_ DE SEL**</dt> </dl>        | Texto.<br/>                            |
| <dl> <dt>**OBJETO \_ SEL**</dt> </dl>      | Al menos un objeto COM.<br/>         |
| <dl> <dt>**SEL \_ MULTICHAR**</dt> </dl>   | Más de un carácter de texto.<br/> |
| <dl> <dt>**SEL \_ MULTIOBJECT**</dt> </dl> | Más de un objeto COM.<br/>        |



 

## <a name="remarks"></a>Comentarios

Este mensaje es útil durante el [**procesamiento de WM \_ SIZE**](/windows/desktop/winmsg/wm-size) para el elemento primario de un control de edición enriquecido sin fondo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TAMAÑO \_ WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

