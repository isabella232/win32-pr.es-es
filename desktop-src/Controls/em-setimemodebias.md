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
ms.openlocfilehash: b4812c21558fba07be2709c0fd1a011f31d79fad17e0b4146fa0c7d65843a087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672675"
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
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**LA ZONA \_ DE SMODE \_ DEL FONDO MONETARIO NO EXISTE**</dt> </dl>                            | Sin sesgo.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser el mismo valor que *wParam.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve la nueva configuración de sesgo del modo IME.

## <a name="remarks"></a>Observaciones

Cuando el IME genera una lista de opciones alternativas para un conjunto de caracteres, este mensaje establece los criterios por los que algunas de las opciones aparecerán en la parte superior de la lista.

Para establecer el sesgo del modo Text Services Framework (TSF), use [**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md).

La aplicación debe llamar a [**EM \_ ISIME antes**](em-isime.md) de llamar a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> </dl>

 

 





