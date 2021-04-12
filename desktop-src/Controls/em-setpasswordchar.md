---
title: Mensaje de EM_SETPASSWORDCHAR (Winuser. h)
description: Establece o quita el carácter de contraseña de un control de edición. Cuando se establece un carácter de contraseña, ese carácter se muestra en lugar de los caracteres que escribe el usuario. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490228"
---
# <a name="em_setpasswordchar-message"></a>\_Mensaje SETPASSWORDCHAR em

Establece o quita el carácter de contraseña de un control de edición. Cuando se establece un carácter de contraseña, ese carácter se muestra en lugar de los caracteres que escribe el usuario. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Carácter que se va a mostrar en lugar de los caracteres especificados por el usuario. Si este parámetro es cero, el control quita el carácter de contraseña actual y muestra los caracteres que escribe el usuario.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando un control de edición recibe el mensaje **\_ SETPASSWORDCHAR em** , el control vuelve a dibujar todos los caracteres visibles mediante el carácter especificado por el parámetro *wParam* . Si *wParam* es cero, el control vuelve a dibujar todos los caracteres visibles con los caracteres que escribe el usuario.

Si se crea un control de edición con el estilo de [**\_ contraseña de es**](edit-control-styles.md) , el carácter de contraseña predeterminado se establece en un asterisco ( \* ). Si se crea un control de edición sin el estilo de **\_ contraseña** es, no hay ningún carácter de contraseña. Se quita el estilo de **\_ contraseña** de es si se envía un mensaje **\_ SETPASSWORDCHAR em** con el parámetro *wParam* establecido en cero.

**Controles de edición:** Los controles de edición multilínea no admiten el estilo de contraseña ni los mensajes.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 2,0 y versiones posteriores. Los controles de edición de línea única y multilínea admiten el estilo de contraseña y los mensajes. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETPASSWORDCHAR em**](em-getpasswordchar.md)
</dt> </dl>

 

 





