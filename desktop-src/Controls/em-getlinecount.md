---
title: EM_GETLINECOUNT mensaje (Winuser.h)
description: Obtiene el número de líneas de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETLINECOUNT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062190"
---
# <a name="em_getlinecount-message-winuserh"></a>EM_GETLINECOUNT mensaje (Winuser.h)

Obtiene el número de líneas de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

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

El valor devuelto es un entero que especifica el número total de líneas de texto en el control de edición multilínea o el control de edición enriquecido. Si el control no tiene texto, el valor devuelto es 1. El valor devuelto nunca será menor que 1.

## <a name="remarks"></a>Observaciones

El **mensaje EM \_ GETLINECOUNT** recupera el número total de líneas de texto, no solo el número de líneas que están visibles actualmente.

Si la característica Wordwrap está habilitada, el número de líneas puede cambiar cuando cambien las dimensiones de la ventana de edición.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETLINE**](em-getline.md)
</dt> <dt>

[**EM \_ LINELENGTH**](em-linelength.md)
</dt> <dt>

[**Editar \_ GetLineCount**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





