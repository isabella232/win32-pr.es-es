---
title: Mensaje de EM_SETIMESTATUS (Winuser. h)
description: Establece las marcas de estado que determinan cómo interactúa un control de edición con el editor de métodos de entrada (IME).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- EM_SETIMESTATUS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802659"
---
# <a name="em_setimestatus-message"></a>\_Mensaje SETIMESTATUS em

Establece las marcas de estado que determinan cómo interactúa un control de edición con el editor de métodos de entrada (IME).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de estado que se va a establecer. Este parámetro puede ser el valor siguiente.



| Value                                                                                                                                                                                       | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Establece el comportamiento de la cadena de composición de control.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Datos específicos del tipo de estado. Si *wParam* es **EMSIS \_ COMPOSITIONSTRING**, este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>                         | Si se establece esta marca, el control de edición enlaza el mensaje de [**\_ \_ composición del IME de WM**](/windows/desktop/Intl/wm-ime-composition) con *lParam* establecido en el valor de RESULTSTR de GC \_ y devuelve la cadena de resultado inmediatamente. Si no se establece esta marca, el control de edición pasa el mensaje de **\_ \_ composición del IME de WM** al procedimiento de ventana predeterminado y controla la cadena de resultado del mensaje de [**\_ carácter de WM**](/windows/desktop/inputdev/wm-char) ; éste es el comportamiento predeterminado del control de edición.<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>             | Si se establece esta marca, el control de edición cancela la cadena de composición cuando recibe el mensaje de [**\_ SETFOCUS de WM**](/windows/desktop/inputdev/wm-setfocus) . Si no se establece esta marca, el control de edición no cancela la cadena de composición; Éste es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Si se establece esta marca, el control de edición completa la cadena de composición al recibir el mensaje de [**\_ KILLFOCUS de WM**](/windows/desktop/inputdev/wm-killfocus) . Si no se establece esta marca, el control de edición no completa la cadena de composición; Éste es el comportamiento predeterminado del control de edición.<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor anterior del parámetro *lParam* .

## <a name="remarks"></a>Observaciones

**Edición enriquecida:** No se admite el mensaje **\_ SETIMESTATUS em** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETIMESTATUS em**](em-getimestatus.md)
</dt> </dl>

 

