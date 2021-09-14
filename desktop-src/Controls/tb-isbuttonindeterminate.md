---
title: TB_ISBUTTONINDETERMINATE mensaje (Commctrl.h)
description: Determina si el botón especificado en una barra de herramientas es indeterminado.
ms.assetid: b4d759b3-cdbc-417b-9da4-4ed9edc38c0e
keywords:
- TB_ISBUTTONINDETERMINATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_ISBUTTONINDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc024efcad9f0f48ae4882b019269903c249bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166698"
---
# <a name="tb_isbuttonindeterminate-message"></a>Mensaje \_ ISBUTTONINDETERMINATE de TB

Determina si el botón especificado en una barra de herramientas es indeterminado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si el botón es indeterminado o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





