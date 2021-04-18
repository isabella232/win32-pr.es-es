---
title: Mensaje de CBEM_INSERTITEM (commctrl. h)
description: Inserta un nuevo elemento en un control ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658393"
---
# <a name="cbem_insertitem-message"></a>CBEM \_ INSERTITEM Message

Inserta un nuevo elemento en un control ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que contiene información sobre el elemento que se va a insertar. Cuando se envía el mensaje, se debe establecer el miembro **iItem** para indicar el índice basado en cero en el que se va a insertar el elemento. Para insertar un elemento al final de la lista, establezca el miembro **iItem** en-1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice en el que se insertó el nuevo elemento si se realiza correctamente, o-1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CBEM \_ INSERTITEMW** (Unicode) y **CBEM \_ INSERTITEMA** (ANSI)<br/>           |



 

 





