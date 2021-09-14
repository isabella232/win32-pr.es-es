---
title: EM_GETOPTIONS mensaje (Richedit.h)
description: Recupera las opciones de control de edición enriquecciones.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- EM_GETOPTIONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b31af3663331b63553fc262fc9bdbd5613c5768
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170058"
---
# <a name="em_getoptions-message"></a>Mensaje \_ DE EM GETOPTIONS

Recupera las opciones de control de edición enriquecciones.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve una combinación de los valores de marca de opción actuales descritos en el [**mensaje EM \_ SETOPTIONS.**](em-setoptions.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETOPTIONS**](em-setoptions.md)
</dt> </dl>

 

 





