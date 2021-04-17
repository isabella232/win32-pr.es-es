---
title: Mensaje de CBEM_GETITEM (commctrl. h)
description: Obtiene la información de un elemento ComboBoxEx determinado.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- CBEM_GETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658341"
---
# <a name="cbem_getitem-message"></a>CBEM \_ mensaje GETITEM

Obtiene la información de un elemento ComboBoxEx determinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que recibe la información del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

Cuando se envía el mensaje, se deben establecer los miembros **iItem** y **Mask** de la estructura para indicar el índice del elemento de destino y el tipo de información que se va a recuperar. Otros miembros se establecen según sea necesario. Por ejemplo, para recuperar texto, debe establecer la \_ marca de texto CBEIF en **Mask** y asignar un valor a **cchTextMax**. Al establecer el miembro **iItem** en-1 se recuperará el elemento mostrado en el control de edición.

Si la \_ marca de texto CBEIF se establece en el miembro **Mask** de la estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , el control puede cambiar el miembro **miembros pszText** de la estructura para que apunte al nuevo texto en lugar de llenar el búfer con el texto solicitado. Las aplicaciones no deben suponer que el texto siempre se colocará en el búfer solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CBEM \_ GETITEMW** (Unicode) y **CBEM \_ GETITEMA** (ANSI)<br/>                 |



 

 





