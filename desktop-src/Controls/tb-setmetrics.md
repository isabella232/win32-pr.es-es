---
title: TB_SETMETRICS mensaje (Commctrl.h)
description: Establece las métricas de un control de barra de herramientas.
ms.assetid: 60e35d65-6291-4a55-a4cf-19b5b1db8a65
keywords:
- TB_SETMETRICS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5320ecc85f0a44c4c80868ae5699b051e1ac1781
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166582"
---
# <a name="tb_setmetrics-message"></a>Mensaje \_ DE TB SETMETRICS

Establece las métricas de un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Estructura TBMETRICS que**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) contiene las métricas de la barra de herramientas que se establecerán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





