---
title: TTM_GETCURRENTTOOL mensaje (Commctrl.h)
description: Recupera la información de la herramienta actual en un control de información sobre herramientas.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL controles de Windows mensaje
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
ms.openlocfilehash: 4558e582e4619cd7d96380a1e38e2efe68808b9241e4c627e12a74946965d8de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769345"
---
# <a name="ttm_getcurrenttool-message"></a>Mensaje \_ GETCURRENTTOOL de TTM

Recupera la información de la herramienta actual en un control de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recibe información sobre la herramienta actual. Si este valor es **NULL,** el valor devuelto indica la existencia de la herramienta actual sin recuperar realmente la información de la herramienta. Si este valor no es **NULL,** el **miembro cbSize** de la **estructura TOOLINFO** debe rellenarse antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario. Si *lParam* es **NULL,** devuelve distinto de cero si existe una herramienta actual o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ GETCURRENTTOOLW** (Unicode) y **TTM \_ GETCURRENTTOOLA** (ANSI)<br/>     |



 

 





