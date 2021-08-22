---
title: EM_SETSEL mensaje (Winuser.h)
description: Selecciona un intervalo de caracteres en un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETSEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190d8a62b874d3449e0a9bf5d334a515000fb0436ba73753a8657936363071b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062895"
---
# <a name="em_setsel-message"></a>Mensaje \_ EM SETSEL

Selecciona un intervalo de caracteres en un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Posición del carácter inicial de la selección.

</dd> <dt>

*lParam* 
</dt> <dd>

Posición del carácter final de la selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

El valor inicial puede ser mayor que el valor final. La parte inferior de los dos valores especifica la posición del carácter del primer carácter de la selección. El valor superior especifica la posición del primer carácter más allá de la selección.

El valor inicial es el punto delimitador de la selección y el valor final es el extremo activo. Si el usuario usa la tecla MAYÚS para ajustar el tamaño de la selección, el extremo activo puede moverse, pero el punto delimitador sigue siendo el mismo.

Si el inicio es 0 y el final es -1, se selecciona todo el texto del control de edición. Si el inicio es -1, se deselecciona cualquier selección actual.

**Editar controles:** El control muestra un cursor intermitente en la posición final, independientemente de los valores relativos de inicio y fin.

**Edición enriqueceda:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

Si el control de edición tiene el estilo [**\_ ES NOHIDESEL,**](edit-control-styles.md) el texto seleccionado se resalta independientemente de si el control tiene el foco. Sin el **estilo \_ ES NOHIDESEL,** el texto seleccionado solo se resalta cuando el control de edición tiene el foco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETSEL**](em-getsel.md)
</dt> <dt>

[**EM \_ REPLACESEL**](em-replacesel.md)
</dt> <dt>

[**EM \_ SCROLLCARET**](em-scrollcaret.md)
</dt> <dt>

[**EM \_ EXSETSEL**](em-exsetsel.md)
</dt> </dl>

 

 





