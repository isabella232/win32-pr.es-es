---
title: EM_SETIMEMODEBIAS mensaje (Richedit.h)
description: Establezca el sesgo del modo del Editor de métodos de entrada (IME) para un control de edición enriquecido.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062096"
---
# <a name="em_setimemodebias-message"></a>Mensaje \_ EM SETIMEMODEBIAS

Establezca el sesgo del modo del Editor de métodos de entrada (IME) para un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de sesgo del modo IME. Puede ser uno de los siguientes.



| Value                                                                                                                                                                                        | Significado                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**\_PLAURALCLAUSE DE SMODE \_ PARA EL GOBIERNO DEL PAÍS**</dt> </dl> | Establece el sesgo del modo IME en Nombre.<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**LA \_ SMODE DE LA \_ ZONA DE LA CONSEJEÍA NO EXISTE**</dt> </dl>                            | Sin sesgo.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser el mismo valor que *wParam.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve la nueva configuración de sesgo del modo IME.

## <a name="remarks"></a>Observaciones

Cuando el IME genera una lista de opciones alternativas para un conjunto de caracteres, este mensaje establece los criterios por los que algunas de las opciones aparecerán en la parte superior de la lista.

Para establecer el sesgo Text Services Framework modo de Text Services Framework (TSF), use [**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md).

La aplicación debe llamar a [**EM \_ ISIME antes**](em-isime.md) de llamar a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> </dl>

 

 





