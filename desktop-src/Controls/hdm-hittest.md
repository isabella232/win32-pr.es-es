---
title: Mensaje de HDM_HITTEST (commctrl. h)
description: Comprueba un punto para determinar qué elemento de encabezado, si existe, está en el punto especificado.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- HDM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150553"
---
# <a name="hdm_hittest-message"></a>HDM \_ mensaje HITTEST

Comprueba un punto para determinar qué elemento de encabezado, si existe, está en el punto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) que contiene la posición que se va a probar y recibe información sobre los resultados de la prueba.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento en la posición especificada, si existe, o en 1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





