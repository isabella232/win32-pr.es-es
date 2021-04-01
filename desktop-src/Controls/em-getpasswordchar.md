---
title: Mensaje de EM_GETPASSWORDCHAR (Winuser. h)
description: Obtiene el carácter de la contraseña que muestra un control de edición cuando el usuario escribe texto. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR controles de mensajes de Windows
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
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905525"
---
# <a name="em_getpasswordchar-message"></a>\_Mensaje GETPASSWORDCHAR em

Obtiene el carácter de la contraseña que muestra un control de edición cuando el usuario escribe texto. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

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

El valor devuelto especifica el carácter que se va a mostrar en lugar de los caracteres que escriba el usuario. Si el valor devuelto es **null**, no hay ningún carácter de contraseña y el control muestra los caracteres que escribe el usuario.

## <a name="remarks"></a>Observaciones

Si se crea un control de edición con el estilo de [**\_ contraseña de es**](edit-control-styles.md) , el carácter de contraseña predeterminado se establece en un asterisco ( \* ). Si se crea un control de edición sin el estilo de **\_ contraseña** es, no hay ningún carácter de contraseña. Para cambiar el carácter de contraseña, envíe el mensaje [**\_ SETPASSWORDCHAR em**](em-setpasswordchar.md) .

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

[**\_SETPASSWORDCHAR em**](em-setpasswordchar.md)
</dt> </dl>

 

 





