---
title: Mensaje de TTM_GETCURRENTTOOL (commctrl. h)
description: Recupera la información de la herramienta actual en un control de información sobre herramientas.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996414"
---
# <a name="ttm_getcurrenttool-message"></a>TTM \_ GETCURRENTTOOL

Recupera la información de la herramienta actual en un control de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recibe información sobre la herramienta actual. Si este valor es **null**, el valor devuelto indica la existencia de la herramienta actual sin recuperar realmente la información de la herramienta. Si este valor no es **null**, el miembro **cbSize** de la estructura **TOOLINFO** se debe rellenar antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario. Si *lParam* es **null**, devuelve un valor distinto de cero si existe una herramienta actual o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ GETCURRENTTOOLW** (Unicode) y **TTM \_ GETCURRENTTOOLA** (ANSI)<br/>     |



 

 





