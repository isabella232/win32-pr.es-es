---
title: LM_GETITEM mensaje (Commctrl.h)
description: Recupera los estados y atributos de un elemento.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- LM_GETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974109"
---
# <a name="lm_getitem-message"></a>Mensaje \_ GETITEM de LM

Recupera los estados y atributos de un elemento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser **NULL.** </dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-litem">estructura LITEM</a> que se va a rellenar con información sobre el elemento. </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el mensaje consigue obtener los valores y atributos especificados.

## <a name="remarks"></a>Observaciones

Con el **mensaje \_ LM GETITEM,** solo se puede acceder a los vínculos a través del índice numérico devuelto en el **miembro iLink** [**de LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem). No se admite el acceso al vínculo a través del nombre de identificador devuelto en **szID.**

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





