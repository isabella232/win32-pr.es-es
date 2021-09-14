---
title: TB_REPLACEBITMAP mensaje (Commctrl.h)
description: Reemplaza un mapa de bits existente por un nuevo mapa de bits.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- TB_REPLACEBITMAP controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166669"
---
# <a name="tb_replacebitmap-message"></a>Mensaje \_ REPLACEBITMAP de TB

Reemplaza un mapa de bits existente por un nuevo mapa de bits.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) que contiene la información del mapa de bits que se va a reemplazar y el nuevo mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





