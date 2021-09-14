---
title: TB_GETIMAGELIST mensaje (Commctrl.h)
description: Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en su estado predeterminado. Un control de barra de herramientas usa esta lista de imágenes para mostrar botones cuando no están encendidos o deshabilitados.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- TB_GETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166817"
---
# <a name="tb_getimagelist-message"></a>Mensaje \_ GETIMAGELIST de TB

Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en su estado predeterminado. Un control de barra de herramientas usa esta lista de imágenes para mostrar botones cuando no están encendidos o deshabilitados.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes o **NULL si** no se establece ninguna lista de imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





