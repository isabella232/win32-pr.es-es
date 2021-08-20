---
title: SB_SETICON mensaje (Commctrl.h)
description: Establece el icono de un elemento en una barra de estado.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e08b1c3b0ce1a453ca9050c20552a14169a594c8091708339b4a436f1fb1a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540075"
---
# <a name="sb_seticon-message"></a>Mensaje \_ DE SB SETICON

Establece el icono de un elemento en una barra de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que recibirá el icono. Si este parámetro es -1, se supone que la barra de estado es una barra de estado simple.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del icono que se va a establecer. Si este valor es **NULL,** el icono se quita del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

La barra de estado no destruirá el icono. Es responsabilidad de la aplicación que realiza la llamada realizar un seguimiento de los iconos y destruirlos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





