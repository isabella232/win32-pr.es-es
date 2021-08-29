---
title: TB_ENABLEBUTTON mensaje (Commctrl.h)
description: Habilita o deshabilita el botón especificado en una barra de herramientas.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- TB_ENABLEBUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4edc2fd7c1e088c376772f38c106cf12f41274de0bc5fda6385851c74126e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919105"
---
# <a name="tb_enablebutton-message"></a>Mensaje \_ ENABLEBUTTON de TB

Habilita o deshabilita el botón especificado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón que se habilitará o deshabilitará.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **BOOL** que indica si se debe habilitar o deshabilitar el botón especificado. Si **es TRUE,** el botón está habilitado. Si **es FALSE,** el botón está deshabilitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Cuando se ha habilitado un botón, se puede presionar y activar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

