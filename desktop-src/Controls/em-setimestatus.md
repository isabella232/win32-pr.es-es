---
title: EM_SETIMESTATUS mensaje (Winuser.h)
description: Establece las marcas de estado que determinan cómo interactúa un control de edición con el Editor de métodos de entrada (IME).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- EM_SETIMESTATUS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5a3e5413c577fcecd89ebb27bc61e5fff31f7e71b3ec7e6da67523d6ee9392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412402"
---
# <a name="em_setimestatus-message"></a>Mensaje \_ EM SETIMESTATUS

Establece las marcas de estado que determinan cómo interactúa un control de edición con el Editor de métodos de entrada (IME).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de estado que se establecerá. Este parámetro puede ser el siguiente valor.



| Valor                                                                                                                                                                                       | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Establece el comportamiento de la cadena de composición de control.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Datos específicos del tipo de estado. Si *wParam* es **EMSIS \_ COMPOSITIONSTRING**, este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**QUEMES \_ GETCOMPSTRATONCE**</dt> </dl>                         | Si se establece esta marca, el control de edición enlazará el mensaje [**\_ WM IME \_ COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) con *lParam* establecido en GCS RESULTSTR y devolverá la cadena \_ de resultado inmediatamente. Si no se establece esta marca, el control de edición pasa el mensaje **DE WM \_ IME \_ COMPOSITION** al procedimiento de ventana predeterminado y controla la cadena de resultado del mensaje CHAR de [**WM; \_**](/windows/desktop/inputdev/wm-char) este es el comportamiento predeterminado del control de edición.<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**QUEMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>             | Si se establece esta marca, el control de edición cancela la cadena de composición cuando recibe el [**mensaje \_ SETFOCUS de WM.**](/windows/desktop/inputdev/wm-setfocus) Si no se establece esta marca, el control de edición no cancela la cadena de composición; este es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**QUEMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Si se establece esta marca, el control de edición completa la cadena de composición al recibir el [**mensaje \_ KILLFOCUS de WM.**](/windows/desktop/inputdev/wm-killfocus) Si no se establece esta marca, el control de edición no completa la cadena de composición; este es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor anterior del *parámetro lParam.*

## <a name="remarks"></a>Comentarios

**Edición enriqueceda:** No **se admite el mensaje EM \_ SETIMESTATUS.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETIMESTATUS**](em-getimestatus.md)
</dt> </dl>

 

