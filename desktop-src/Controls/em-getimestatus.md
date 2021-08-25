---
title: EM_GETIMESTATUS mensaje (Winuser.h)
description: Obtiene un conjunto de marcas de estado que indican cómo interactúa el control de edición con el Editor de métodos de entrada (IME).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a8251a62aa9cf48bcc6476af27e4c3a5dbbb82dd0ce76ca21ae094225a3e46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048995"
---
# <a name="em_getimestatus-message"></a>Mensaje \_ GETIMESTATUS de EM

Obtiene un conjunto de marcas de estado que indican cómo interactúa el control de edición con el Editor de métodos de entrada (IME).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de estado que se recuperará. Este parámetro puede ser el siguiente valor.



| Value                                                                                                                                                                                       | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Establece el comportamiento para controlar la cadena de composición.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Datos específicos del tipo de estado que se recuperará. Con el **valor DE EMSIS \_ COMPOSITIONSTRING** para *status*, este valor devuelto es uno o varios de los valores siguientes.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**QUEMES \_ GETCOMPSTRATONCE**</dt> </dl>         | Si se establece esta marca, el control de edición enlazará el mensaje [**\_ WM IME \_ COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) con *fFlags* establecido en GCS RESULTSTR y devolverá la cadena \_ de resultado inmediatamente. Si no se establece esta marca, el control de edición pasa el mensaje COMPOSITION de **WM \_ IME \_** al procedimiento de ventana predeterminado y procesa la cadena de resultado del mensaje CHAR de [**WM; \_**](/windows/desktop/inputdev/wm-char) este es el comportamiento predeterminado del control de edición.<br/> |
| <dl> <dt>**QUEMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>     | Si se establece esta marca, el control de edición cancela la cadena de composición cuando recibe el [**mensaje \_ SETFOCUS de WM.**](/windows/desktop/inputdev/wm-setfocus) Si no se establece esta marca, el control de edición no cancela la cadena de composición; este es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                       |
| <dl> <dt>**QUEMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Si se establece esta marca, el control de edición completa la cadena de composición al recibir el [**mensaje \_ KILLFOCUS de WM.**](/windows/desktop/inputdev/wm-killfocus) Si no se establece esta marca, el control de edición no completa la cadena de composición; este es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentarios

**Edición enriqueceda:** No **se admite el mensaje EM \_ GETIMESTATUS.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETIMESTATUS**](em-setimestatus.md)
</dt> </dl>

 

