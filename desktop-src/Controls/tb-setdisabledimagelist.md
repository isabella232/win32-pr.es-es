---
title: TB_SETDISABLEDIMAGELIST mensaje (Commctrl.h)
description: Establece la lista de imágenes que usará el control de barra de herramientas para mostrar los botones deshabilitados.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- TB_SETDISABLEDIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166629"
---
# <a name="tb_setdisabledimagelist-message"></a>Mensaje \_ SETDISABLEDIMAGELIST de TB

Establece la lista de imágenes que usará el control de barra de herramientas para mostrar los botones deshabilitados.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se establecerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes que se usó anteriormente para mostrar los botones deshabilitados, o **NULL** si no se estableció previamente ninguna lista de imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





