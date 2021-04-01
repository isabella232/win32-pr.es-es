---
title: Mensaje de LVM_GETINSERTMARKRECT (commctrl. h)
description: Recupera el rectángulo que delimita el punto de inserción.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- LVM_GETINSERTMARKRECT controles de mensajes de Windows
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
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996917"
---
# <a name="lvm_getinsertmarkrect-message"></a>\_Mensaje GETINSERTMARKRECT LVM

Recupera el rectángulo que delimita el punto de inserción.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>No se utiliza; debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una estructura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> que contiene las coordenadas de un rectángulo que delimita el punto de inserción.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                      | Descripción                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**0,1**</dt> </dl> | No se encontró ningún punto de inserción.<br/> |
| <dl> <dt>**1**</dt> </dl> | Se encontró el punto de inserción.<br/>    |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

