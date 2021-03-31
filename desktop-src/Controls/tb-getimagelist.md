---
title: Mensaje de TB_GETIMAGELIST (commctrl. h)
description: Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en su estado predeterminado. Un control de barra de herramientas usa esta lista de imágenes para mostrar botones cuando no están activos o deshabilitados.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- TB_GETIMAGELIST controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801357"
---
# <a name="tb_getimagelist-message"></a>\_Mensaje GETIMAGELIST TB

Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en su estado predeterminado. Un control de barra de herramientas usa esta lista de imágenes para mostrar botones cuando no están activos o deshabilitados.

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

Devuelve el identificador de la lista de imágenes o **null** si no se ha establecido ninguna lista de imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





