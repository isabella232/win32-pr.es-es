---
title: EM_SETLANGOPTIONS mensaje (Richedit.h)
description: Establece opciones para la compatibilidad del Editor de métodos de entrada (IME) y el idioma asiático en un control de edición enriquecido.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5984c20273d2daa0a2e39fc6caf6dde88c8b274502a50e1a5e5eb3cca2b6f94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831216"
---
# <a name="em_setlangoptions-message"></a>Mensaje \_ EM SETLANGOPTIONS

Establece opciones para la compatibilidad del Editor de métodos de entrada (IME) y el idioma asiático en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica las opciones de idioma. Para obtener una lista de los valores posibles, [**vea EM \_ GETLANGOPTIONS**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve un valor de 1.

## <a name="remarks"></a>Comentarios

El **mensaje EM \_ SETLANGOPTIONS** controla lo siguiente:

-   Enlace de fuente automático.
-   Cambio automático del teclado.
-   Ajuste automático del tamaño de fuente.
-   Uso de fuentes predeterminadas de interfaz de usuario en lugar de fuentes predeterminadas de documento.
-   Notificaciones al cliente durante la composición de IME.
-   Cómo anula IME el modo de composición.
-   Corrector ortográfica, corrección automática y predicción táctil del teclado.

Este mensaje establece los valores de todas las marcas de opción de idioma. Para cambiar un subconjunto de las marcas, envíe el mensaje [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md) para obtener las marcas de opción actuales, cambie las marcas que necesita cambiar y, a continuación, envíe el mensaje **EM \_ SETLANGOPTIONS con** el resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)
</dt> </dl>

 

 





