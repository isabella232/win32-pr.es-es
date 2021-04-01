---
title: Mensaje de TB_REPLACEBITMAP (commctrl. h)
description: Reemplaza un mapa de bits existente por un nuevo mapa de bits.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- TB_REPLACEBITMAP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905449"
---
# <a name="tb_replacebitmap-message"></a>\_Mensaje REPLACEBITMAP TB

Reemplaza un mapa de bits existente por un nuevo mapa de bits.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) que contiene la información del mapa de bits que se va a reemplazar y el nuevo mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





