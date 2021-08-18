---
title: LM_HITTEST mensaje (Commctrl.h)
description: Determina si el usuario hizo clic en el vínculo especificado.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- LM_HITTEST controles de Windows mensaje
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 559ea1500c7270ece1785391777133bdaaeb1e95e5b01fa5ca7d4bb76e40f1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958385"
---
# <a name="lm_hittest-message"></a>Mensaje \_ HITTEST de LM

Determina si el usuario hizo clic en el vínculo especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser **NULL.**</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**estructura LHITTESTINFO**</a> que se va a rellenar con información sobre el vínculo en el que el usuario hizo clic, si existe alguno. </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** el usuario hizo clic en un vínculo; de lo contrario, devuelve **FALSE.**

## <a name="remarks"></a>Comentarios

Si el **mensaje \_ HITTEST de LM** se realiza correctamente, el sistema rellena [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) y **LITEM.szID**. Si se produce un error en el mensaje **\_ HITTEST** de LM, no suponga que ninguna **información de LITEM** es válida.

> [!Note]  
> Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





