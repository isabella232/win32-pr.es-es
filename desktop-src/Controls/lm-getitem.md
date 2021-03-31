---
title: Mensaje de LM_GETITEM (commctrl. h)
description: Recupera los Estados y atributos de un elemento.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- LM_GETITEM controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149913"
---
# <a name="lm_getitem-message"></a>\_Mensaje GETITEM de LM

Recupera los Estados y atributos de un elemento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser **null**. </dd> <dt>

*lParam* 
</dt> <dd>Puntero <a href="/windows/win32/api/commctrl/ns-commctrl-litem">a una estructura de la</a> que se va a rellenar información sobre el elemento. </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el mensaje se obtiene correctamente al obtener los valores y atributos especificados.

## <a name="remarks"></a>Observaciones

Con el mensaje de mensaje de error de **\_ LM** , solo se puede tener acceso a los vínculos a través del índice numérico devuelto en el miembro **iLink** [**de la**](/windows/win32/api/commctrl/ns-commctrl-litem). No se admite el acceso al vínculo a través del nombre de identificador devuelto en **szID** .

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





