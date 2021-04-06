---
title: Mensaje de TB_SETHOTITEM2 (commctrl. h)
description: Establece el elemento activo en una barra de herramientas.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 controles de mensajes de Windows
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
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803139"
---
# <a name="tb_sethotitem2-message"></a>\_Mensaje SETHOTITEM2 TB

Establece el elemento activo en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento que se hará activo. Si este valor es-1, ninguno de los elementos estará activo.

</dd> <dt>

*lParam* 
</dt> <dd>Combinación de marcas HICF \_ xxx. Vea <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento activo anterior, o-1 si no hay ningún elemento activo.

## <a name="remarks"></a>Observaciones

El comportamiento de este mensaje no está definido para las barras de herramientas que no tienen el estilo [**\_ plano TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





