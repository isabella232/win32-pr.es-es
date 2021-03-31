---
title: Mensaje de LM_SETITEM (commctrl. h)
description: Establece los Estados y los atributos de un elemento.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- LM_SETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149911"
---
# <a name="lm_setitem-message"></a>\_Mensaje SETITEM de LM

Establece los Estados y los atributos de un elemento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser **null**. </dd> <dt>

*lParam* 
</dt> <dd>Puntero <a href="/windows/win32/api/commctrl/ns-commctrl-litem">a una estructura de un</a> valor que contiene los nuevos Estados y atributos que se desean para el vínculo. </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el mensaje se establece correctamente en el establecimiento de los valores y los atributos especificados.

## <a name="remarks"></a>Observaciones

Con el mensaje de mensaje de error de [**\_ LM**](lm-getitem.md) , solo se puede tener acceso a los vínculos a través del índice numérico devuelto en el miembro **iLink** [**de la**](/windows/win32/api/commctrl/ns-commctrl-litem). No se admite el acceso al vínculo a través del nombre de identificador devuelto en **szID** .

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comctl32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





