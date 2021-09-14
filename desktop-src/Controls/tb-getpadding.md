---
title: TB_GETPADDING mensaje (Commctrl.h)
description: Recupera el relleno de un control de barra de herramientas.
ms.assetid: dde0f44d-5d22-4cab-a7f8-48d84b8995d3
keywords:
- TB_GETPADDING controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15babf2fd5d97377991d1827ea8947e9d794600
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166785"
---
# <a name="tb_getpadding-message"></a>MENSAJE \_ GETPADDING DE TB

Recupera el relleno de un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene el relleno horizontal de la palabra baja y el relleno vertical en la palabra alta, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ SETPADDING**](tb-setpadding.md)
</dt> </dl>

 

 





