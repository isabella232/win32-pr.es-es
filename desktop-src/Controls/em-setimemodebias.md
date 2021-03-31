---
title: Mensaje EM_SETIMEMODEBIAS (RichEdit. h)
description: Establezca el sesgo del modo editor de métodos de entrada (IME) para un control Rich Edit.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491212"
---
# <a name="em_setimemodebias-message"></a>\_Mensaje SETIMEMODEBIAS em

Establezca el sesgo del modo editor de métodos de entrada (IME) para un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de diferencia del modo IME. Puede ser uno de los siguientes.



| Value                                                                                                                                                                                        | Significado                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**\_PLAURALCLAUSE SMODE \_ IMF**</dt> </dl> | Establece la diferencia entre el modo IME y el nombre.<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**IMF \_ SMODE \_ ninguno**</dt> </dl>                            | Sin sesgo.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser el mismo valor que *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el nuevo valor de diferencia del modo IME.

## <a name="remarks"></a>Observaciones

Cuando el IME genera una lista de opciones alternativas para un juego de caracteres, este mensaje establece los criterios por los que algunas de las opciones aparecerán en la parte superior de la lista.

Para establecer la diferencia del modo de Text Services Framework (TSF), use [**em \_ SETCTFMODEBIAS**](em-setctfmodebias.md).

La aplicación debe llamar a [**em \_ ISIME**](em-isime.md) antes de llamar a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_ISIME em**](em-isime.md)
</dt> <dt>

[**\_SETCTFMODEBIAS em**](em-setctfmodebias.md)
</dt> </dl>

 

 





