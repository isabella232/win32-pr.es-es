---
title: TB_GETBITMAP mensaje (Commctrl.h)
description: Recupera el índice del mapa de bits asociado a un botón en una barra de herramientas.
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- TB_GETBITMAP controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771073b67b1421a5d9bda9d162bc234400c85885
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166865"
---
# <a name="tb_getbitmap-message"></a>Mensaje \_ GETBITMAP de TB

Recupera el índice del mapa de bits asociado a un botón en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón cuyo índice de mapa de bits se va a recuperar.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del mapa de bits si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





