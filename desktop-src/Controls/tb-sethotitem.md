---
title: TB_SETHOTITEM mensaje (Commctrl.h)
description: 'TB_SETHOTITEM mensaje: establece el elemento de acceso rápido en una barra de herramientas.'
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90e5b38675d33a361857c4303fa2a89f22cff29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166614"
---
# <a name="tb_sethotitem-message"></a>Mensaje \_ SETHOTITEM de TB

Establece el elemento de acceso rápido en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento que se hará en caliente. Si este valor es -1, ninguno de los elementos estará en caliente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento de acceso actual anterior o -1 si no había ningún elemento de acceso.

## <a name="remarks"></a>Observaciones

El comportamiento de este mensaje no está definido para las barras de herramientas que no tienen el [**estilo TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





