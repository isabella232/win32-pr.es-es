---
title: TB_CHECKBUTTON mensaje (Commctrl.h)
description: Comprueba o desactiva un botón determinado en una barra de herramientas.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- TB_CHECKBUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec35b6a333e0663acc8c94dec22c2b8f4138cb6024b1f7919fd0ec73cdb0eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919135"
---
# <a name="tb_checkbutton-message"></a>Mensaje \_ CHECKBUTTON de TB

Comprueba o desactiva un botón determinado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón que se comprobará.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **BOOL** que indica si se debe comprobar o desactivar el botón especificado. Si **es TRUE,** se agrega la comprobación. Si **es FALSE,** se quita la comprobación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Cuando se comprueba un botón, se muestra en estado presionado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

