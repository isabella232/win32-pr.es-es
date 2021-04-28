---
title: LM_GETIDEALSIZE mensaje (Commctrl.h)
description: 'LM_GETIDEALSIZE mensaje: recupera el alto preferido de un vínculo para el ancho actual del control.'
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE de mensajes controles de Windows
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
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112393"
---
# <a name="lm_getidealsize-message"></a>Mensaje \_ GETIDEALSIZE de LM

Recupera el alto preferido de un vínculo para el ancho actual del control.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Ancho máximo del vínculo, en píxeles.</dd> <dt>

*lParam* \[ out\]
</dt> <dd>Cuando este mensaje vuelve, contiene un puntero a una <a href="/previous-versions//dd145106(v=vs.85)">**estructura SIZE.**</a> El **miembro cy** de esta estructura indica el alto ideal del control para el ancho dado. Ajusta el miembro **cx a** la cantidad de espacio realmente necesario.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Entero que representa el alto preferido del texto del vínculo, en píxeles.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

