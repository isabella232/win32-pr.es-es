---
title: Mensaje de EM_GETLINECOUNT (Winuser. h)
description: Obtiene el número de líneas de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETLINECOUNT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489461"
---
# <a name="em_getlinecount-message-winuserh"></a>Mensaje de EM_GETLINECOUNT (Winuser. h)

Obtiene el número de líneas de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

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

El valor devuelto es un entero que especifica el número total de líneas de texto en el control de edición multilínea o el control Rich Edit. Si el control no tiene texto, el valor devuelto es 1. El valor devuelto nunca será menor que 1.

## <a name="remarks"></a>Observaciones

El **mensaje \_ GETLINECOUNT em** recupera el número total de líneas de texto, no solo el número de líneas que están visibles actualmente.

Si la característica WordWrap está habilitada, el número de líneas puede cambiar cuando cambian las dimensiones de la ventana de edición.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

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

[**\_GETLINE em**](em-getline.md)
</dt> <dt>

[**\_LINELENGTH em**](em-linelength.md)
</dt> <dt>

[**Editar \_ GetLineCount**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





