---
title: Mensaje EM_SETLANGOPTIONS (RichEdit. h)
description: Establece opciones para la compatibilidad con el editor de métodos de entrada (IME) y idiomas asiáticos en un control Rich Edit.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996290"
---
# <a name="em_setlangoptions-message"></a>\_Mensaje SETLANGOPTIONS em

Establece opciones para la compatibilidad con el editor de métodos de entrada (IME) y idiomas asiáticos en un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica las opciones de idioma. Para obtener una lista de los valores posibles, vea [**em \_ GETLANGOPTIONS**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve un valor de 1.

## <a name="remarks"></a>Observaciones

El **mensaje \_ SETLANGOPTIONS em** controla lo siguiente:

-   Enlace de fuente automático.
-   Cambio automático de teclado.
-   Ajuste automático de tamaño de fuente.
-   Uso de las fuentes predeterminadas de la interfaz de usuario en lugar de las fuentes predeterminadas del documento.
-   Notificaciones al cliente durante la composición del IME.
-   Cómo el IME anula el modo de composición.
-   Revisión ortográfica, Autocorrección y predicción táctil de teclado.

Este mensaje establece los valores de todas las marcas de opciones de lenguaje. Para cambiar un subconjunto de las marcas, envíe el mensaje [**em \_ GETLANGOPTIONS**](em-getlangoptions.md) para obtener las marcas de opciones actuales, cambie las marcas que debe cambiar y, a continuación, envíe el mensaje **\_ SETLANGOPTIONS em** con el resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETLANGOPTIONS em**](em-getlangoptions.md)
</dt> </dl>

 

 





