---
title: TB_GETIDEALSIZE mensaje (Commctrl.h)
description: Obtiene el tamaño ideal de la barra de herramientas.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1844f3ae4200c1120f784c03e5f80d2df4457319cf81e12c88ce0ed84525117d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816315"
---
# <a name="tb_getidealsize-message"></a>Mensaje \_ GETIDEALSIZE de TB

Obtiene el tamaño ideal de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Un **valor BOOL** que indica si se debe recuperar el alto o ancho ideales de la barra de herramientas. Use **TRUE** para recuperar el alto ideal, **FALSE,** para recuperar el ancho ideal.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SIZE**](/previous-versions//dd145106(v=vs.85)) que recibe el alto o ancho en el que se mostrarían todos los botones. Si *wParam es* **TRUE,** solo el **miembro cy** (height) es válido. Si *wParam* es **FALSE,** solo el **miembro cx** (ancho) es válido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

