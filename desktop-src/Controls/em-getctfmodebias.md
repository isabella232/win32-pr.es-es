---
title: Mensaje EM_GETCTFMODEBIAS (RichEdit. h)
description: Obtiene los valores de sesgo del modo de marco de trabajo de servicios de texto para un control Rich Edit de Microsoft.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- EM_GETCTFMODEBIAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150406"
---
# <a name="em_getctfmodebias-message"></a>\_Mensaje GETCTFMODEBIAS em

Obtiene los valores de sesgo del modo de marco de trabajo de servicios de texto para un control Rich Edit de Microsoft.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor de diferencia del modo de marco de servicios de texto actual.

## <a name="remarks"></a>Observaciones

Para obtener la diferencia del modo IME, llame a [**em \_ GETIMEMODEBIAS**](em-getimemodebias.md).

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

[**\_SETCTFMODEBIAS em**](em-setctfmodebias.md)
</dt> <dt>

[**\_GETIMEMODEBIAS em**](em-getimemodebias.md)
</dt> </dl>

 

 





