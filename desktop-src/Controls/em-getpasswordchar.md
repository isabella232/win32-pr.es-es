---
title: EM_GETPASSWORDCHAR mensaje (Winuser.h)
description: Obtiene el carácter de contraseña que un control de edición muestra cuando el usuario escribe texto. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c4e7ac576f18d0ab28fcf8c2288d2bee7966866a71180a81c34896c2396f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831215"
---
# <a name="em_getpasswordchar-message"></a>Mensaje \_ EM GETPASSWORDCHAR

Obtiene el carácter de contraseña que un control de edición muestra cuando el usuario escribe texto. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

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

El valor devuelto especifica el carácter que se va a mostrar en lugar de los caracteres que escriba el usuario. Si el valor devuelto es **NULL,** no hay ningún carácter de contraseña y el control muestra los caracteres especificados por el usuario.

## <a name="remarks"></a>Comentarios

Si se crea un control de edición con el estilo [**ES \_ PASSWORD,**](edit-control-styles.md) el carácter de contraseña predeterminado se establece en un asterisco ( \* ). Si se crea un control de edición sin el **estilo ES \_ PASSWORD,** no hay ningún carácter de contraseña. Para cambiar el carácter de contraseña, envíe el [**mensaje EM \_ SETPASSWORDCHAR.**](em-setpasswordchar.md)

**Editar controles:** Los controles de edición multilínea no admiten el estilo de contraseña ni los mensajes.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 2.0 y versiones posteriores. Los controles de edición de línea única y multilínea admiten el estilo de contraseña y los mensajes. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md)
</dt> </dl>

 

 





