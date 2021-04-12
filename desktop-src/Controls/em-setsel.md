---
title: Mensaje de EM_SETSEL (Winuser. h)
description: Selecciona un intervalo de caracteres en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETSEL controles de mensajes de Windows
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
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489989"
---
# <a name="em_setsel-message"></a>\_Mensaje SETSEL em

Selecciona un intervalo de caracteres en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

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

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El valor inicial puede ser mayor que el valor final. En el nivel inferior de los dos valores se especifica la posición del carácter del primer carácter de la selección. El valor superior especifica la posición del primer carácter más allá de la selección.

El valor inicial es el punto de anclaje de la selección y el valor final es el extremo activo. Si el usuario usa la tecla Mayús para ajustar el tamaño de la selección, el extremo activo se puede mover, pero el punto de anclaje sigue siendo el mismo.

Si el inicio es 0 y el final es-1, se selecciona todo el texto del control de edición. Si el inicio es-1, se anula la selección de cualquier selección actual.

**Controles de edición:** El control muestra un símbolo de intercalación parpadeante en la posición final sin tener en cuenta los valores relativos de inicio y fin.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

Si el control de edición tiene el estilo [**es \_ NOHIDESEL**](edit-control-styles.md) , el texto seleccionado se resalta sin tener en cuenta si el control tiene el foco. Sin el estilo **es \_ NOHIDESEL** , el texto seleccionado se resalta solo cuando el control de edición tiene el foco.

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

[**\_GETSEL em**](em-getsel.md)
</dt> <dt>

[**\_REPLACESEL em**](em-replacesel.md)
</dt> <dt>

[**\_SCROLLCARET em**](em-scrollcaret.md)
</dt> <dt>

[**\_EXSETSEL em**](em-exsetsel.md)
</dt> </dl>

 

 





