---
title: EM_SETPASSWORDCHAR mensaje (Winuser.h)
description: Establece o quita el carácter de contraseña para un control de edición. Cuando se establece un carácter de contraseña, ese carácter se muestra en lugar de los caracteres que escribe el usuario. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062075"
---
# <a name="em_setpasswordchar-message"></a>Mensaje \_ EM SETPASSWORDCHAR

Establece o quita el carácter de contraseña para un control de edición. Cuando se establece un carácter de contraseña, ese carácter se muestra en lugar de los caracteres que escribe el usuario. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Carácter que se va a mostrar en lugar de los caracteres que escribe el usuario. Si este parámetro es cero, el control quita el carácter de contraseña actual y muestra los caracteres que escribe el usuario.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Cuando un control de edición recibe el mensaje **EM \_ SETPASSWORDCHAR,** el control vuelve a dibujar todos los caracteres visibles con el carácter especificado por el *parámetro wParam.* Si *wParam es* cero, el control vuelve a dibujar todos los caracteres visibles con los caracteres que escribe el usuario.

Si se crea un control de edición con el estilo [**ES \_ PASSWORD,**](edit-control-styles.md) el carácter de contraseña predeterminado se establece en un asterisco ( \* ). Si se crea un control de edición sin el **estilo ES \_ PASSWORD,** no hay ningún carácter de contraseña. El **estilo ES \_ PASSWORD** se quita si se envía un **mensaje EM \_ SETPASSWORDCHAR** con el *parámetro wParam* establecido en cero.

**Editar controles:** Los controles de edición multilínea no admiten el estilo de contraseña ni los mensajes.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 2.0 y versiones posteriores. Los controles de edición de línea única y multilínea admiten el estilo de contraseña y los mensajes. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md)
</dt> </dl>

 

 





