---
title: Mensaje de LM_HITTEST (commctrl. h)
description: Determina si el usuario hizo clic en el vínculo especificado.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- LM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905008"
---
# <a name="lm_hittest-message"></a>\_Mensaje LM HITTEST

Determina si el usuario hizo clic en el vínculo especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser **null**.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> que se va a rellenar con información sobre el vínculo en el que el usuario hizo clic, si existe. </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el usuario hizo clic en un vínculo; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Si el mensaje de **LM \_ HITTEST** se realiza correctamente, el sistema rellena en el [**. iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) y en el **. szID**. Si se produce un error en el mensaje **LM \_ HITTEST** , no suponga que la **información de la** tarea es válida.

> [!Note]  
> Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





