---
title: EM_GETWORDWRAPMODE mensaje (Richedit.h)
description: Obtiene las opciones actuales de ajuste de palabras y de salto de palabras para el control de edición enriquecido.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- EM_GETWORDWRAPMODE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062175"
---
# <a name="em_getwordwrapmode-message"></a>Mensaje \_ EM GETWORDWRAPMODE

Obtiene las opciones actuales de ajuste de palabras y de salto de palabras para el control de edición enriquecido.

> [!Note]  
> Este mensaje solo se admite en versiones en idioma asiático de Microsoft Rich Edit 1.0. No se admite en versiones posteriores de Rich Edit.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El mensaje devuelve las opciones actuales de ajuste de palabras y de salto de palabras.

## <a name="remarks"></a>Observaciones

El procedimiento de interrupción de palabras definido por la aplicación no debe enviar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





