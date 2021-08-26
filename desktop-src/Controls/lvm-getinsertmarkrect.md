---
title: LVM_GETINSERTMARKRECT mensaje (Commctrl.h)
description: Recupera el rectángulo que delimita el punto de inserción.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- LVM_GETINSERTMARKRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5832ce185a579432b341482847400e96d60869a64d3ff0a2cd599e2eecf6b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062605"
---
# <a name="lvm_getinsertmarkrect-message"></a>Mensaje \_ LVM GETINSERTMARKRECT

Recupera el rectángulo que delimita el punto de inserción.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>No se usa; debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/previous-versions//dd162897(v=vs.85)">**estructura RECT**</a> que contiene las coordenadas de un rectángulo que delimita el punto de inserción.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                      | Descripción                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**0**</dt> </dl> | No se encontró ningún punto de inserción.<br/> |
| <dl> <dt>**1**</dt> </dl> | Punto de inserción encontrado.<br/>    |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

