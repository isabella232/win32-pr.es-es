---
title: EM_SETLANGOPTIONS mensaje (Richedit.h)
description: Establece las opciones para el Editor de métodos de entrada (IME) y la compatibilidad con idiomas asiáticos en un control de edición enriquecido.
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
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062094"
---
# <a name="em_setlangoptions-message"></a>Mensaje \_ EM SETLANGOPTIONS

Establece las opciones para el Editor de métodos de entrada (IME) y la compatibilidad con idiomas asiáticos en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica las opciones de idioma. Para obtener una lista de valores posibles, [**vea EM \_ GETLANGOPTIONS**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve un valor de 1.

## <a name="remarks"></a>Observaciones

El **mensaje \_ EM SETLANGOPTIONS** controla lo siguiente:

-   Enlace automático de fuentes.
-   Cambio automático de teclado.
-   Ajuste automático del tamaño de fuente.
-   Uso de fuentes predeterminadas de interfaz de usuario en lugar de fuentes predeterminadas de documento.
-   Notificaciones al cliente durante la composición de IME.
-   Cómo anula IME el modo de composición.
-   Revisión ortográfica, corrección automática y predicción de teclado táctil.

Este mensaje establece los valores de todas las marcas de opción de idioma. Para cambiar un subconjunto de las marcas, envíe el mensaje [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md) para obtener las marcas de opción actuales, cambie las marcas que necesita cambiar y, a continuación, envíe el mensaje **EM \_ SETLANGOPTIONS** con el resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)
</dt> </dl>

 

 





