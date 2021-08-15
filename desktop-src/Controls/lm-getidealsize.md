---
title: LM_GETIDEALSIZE mensaje (Commctrl.h)
description: 'LM_GETIDEALSIZE mensaje: recupera el alto preferido de un vínculo para el ancho actual del control.'
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035a919aabeb5d07587c7d9e4fc97e5edc728de4ec8fc476448dca62658f1ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958384"
---
# <a name="lm_getidealsize-message"></a>Mensaje \_ GETIDEALSIZE de LM

Recupera el alto preferido de un vínculo para el ancho actual del control.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Ancho máximo del vínculo, en píxeles.</dd> <dt>

*lParam* \[ out\]
</dt> <dd>Cuando este mensaje devuelve un resultado, contiene un puntero a una <a href="/previous-versions//dd145106(v=vs.85)">**estructura SIZE.**</a> El **miembro cy** de esta estructura indica el alto ideal del control para el ancho dado. Ajusta el miembro **cx a** la cantidad de espacio realmente necesario.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Entero que representa el alto preferido del texto del vínculo, en píxeles.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

