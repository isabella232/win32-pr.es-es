---
title: Mensaje de TVM_GETISEARCHSTRING (commctrl. h)
description: Recupera la cadena de búsqueda incremental para un control de vista de árbol.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151045"
---
# <a name="tvm_getisearchstring-message"></a>\_Mensaje de GETISEARCHSTRING TVM

Recupera la cadena de búsqueda incremental para un control de vista de árbol. El control de vista de árbol utiliza la cadena de búsqueda incremental para seleccionar un elemento en función de los caracteres especificados por el usuario. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetISearchString de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe la cadena de búsqueda incremental.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres de la cadena de búsqueda incremental.

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso incorrecto de este mensaje podría poner en peligro la seguridad del programa. Debe asignar un búfer suficientemente grande para contener la cadena. En primer lugar, llame al mensaje que pasa **null** en *lParam*. Esto devuelve el número de caracteres, excluidos los **valores NULL**, que son necesarios. A continuación, llame al mensaje una segunda vez para recuperar la cadena. Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.

Si el control de vista de árbol no está en modo de búsqueda incremental, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVM \_ GETISEARCHSTRINGW** (Unicode) y **TVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





