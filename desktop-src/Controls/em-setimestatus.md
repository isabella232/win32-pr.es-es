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
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062097"
---
# <a name="em_setimestatus-message"></a>Mensaje \_ EM SETIMESTATUS

Establece las marcas de estado que determinan cómo interactúa un control de edición con el Editor de métodos de entrada (IME).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de estado que se establecerá. Este parámetro puede ser el siguiente valor.



| Value                                                                                                                                                                                       | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Establece el comportamiento de la cadena de composición de control.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Datos específicos del tipo de estado. Si *wParam es* **EMSIS \_ COMPOSITIONSTRING,** este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**QUEMES \_ GETCOMPSTRATONCE**</dt> </dl>                         | Si se establece esta marca, el control de edición enlazará el mensaje [**\_ WM IME \_ COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) con *lParam* establecido en GCS RESULTSTR y devolverá la cadena \_ de resultado inmediatamente. Si no se establece esta marca, el control de edición pasa el mensaje COMPOSITION de **WM \_ IME \_** al procedimiento de ventana predeterminado y controla la cadena de resultado del mensaje CHAR de [**WM; \_**](/windows/desktop/inputdev/wm-char) este es el comportamiento predeterminado del control de edición.<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**\_CANCELCOMPSTRINFOCUS DE QUEMES**</dt> </dl>             | Si se establece esta marca, el control de edición cancela la cadena de composición cuando recibe el [**mensaje \_ SETFOCUS de WM.**](/windows/desktop/inputdev/wm-setfocus) Si no se establece esta marca, el control de edición no cancela la cadena de composición; este es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**QUEMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Si se establece esta marca, el control de edición completa la cadena de composición al recibir el [**mensaje \_ KILLFOCUS de WM.**](/windows/desktop/inputdev/wm-killfocus) Si no se establece esta marca, el control de edición no completa la cadena de composición; este es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor anterior del *parámetro lParam.*

## <a name="remarks"></a>Observaciones

**Edición enriquecte:** No **se admite el mensaje EM \_ SETIMESTATUS.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETIMESTATUS**](em-getimestatus.md)
</dt> </dl>

 

