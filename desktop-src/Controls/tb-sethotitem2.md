---
title: TB_SETHOTITEM2 mensaje (Commctrl.h)
description: 'TB_SETHOTITEM2 mensaje: establece el elemento de acceso rápido en una barra de herramientas.'
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 mensaje Controles de Windows
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104143"
---
# <a name="tb_sethotitem2-message"></a>Mensaje \_ SETHOTITEM2 de TB

Establece el elemento de acceso rápido en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento que se hará en caliente. Si este valor es -1, ninguno de los elementos estará en caliente.

</dd> <dt>

*lParam* 
</dt> <dd>Combinación de marcas XXX \_ de HICF. Vea <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM.**</a></dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento de acceso actual anterior o -1 si no había ningún elemento de acceso.

## <a name="remarks"></a>Comentarios

El comportamiento de este mensaje no está definido para las barras de herramientas que no tienen el [**estilo TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





