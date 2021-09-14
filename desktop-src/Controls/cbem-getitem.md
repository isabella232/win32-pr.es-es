---
title: CBEM_GETITEM mensaje (Commctrl.h)
description: Obtiene información de elemento para un elemento ComboBoxEx determinado.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- CBEM_GETITEM controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170077"
---
# <a name="cbem_getitem-message"></a>Mensaje \_ GETITEM de CBEM

Obtiene información de elemento para un elemento ComboBoxEx determinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que recibe la información del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando se envía el mensaje, se deben establecer los miembros **iItem** y **mask** de la estructura para indicar el índice del elemento de destino y el tipo de información que se va a recuperar. Otros miembros se establecen según sea necesario. Por ejemplo, para recuperar texto, debe establecer la marca CBEIF TEXT en mask y asignar un \_ valor a **cchTextMax**.  Si se **establece el miembro iItem** en -1, se recuperará el elemento mostrado en el control de edición.

Si la marca CBEIF TEXT se establece en el miembro mask de la estructura \_ [**COMBOBOXEXITEM,**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) el control puede cambiar el miembro **pszText** de la estructura para que apunte al texto nuevo en lugar de rellenar el búfer con el texto solicitado.  Las aplicaciones no deben suponer que el texto siempre se colocará en el búfer solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CBEM \_ GETITEMW** (Unicode) y **CBEM \_ GETITEMA** (ANSI)<br/>                 |



 

 





