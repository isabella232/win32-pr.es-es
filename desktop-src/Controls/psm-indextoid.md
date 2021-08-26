---
title: PSM_INDEXTOID mensaje (Prsht.h)
description: Toma el índice de una página de hoja de propiedades y devuelve su identificador de recurso. Puede enviar este mensaje explícitamente o usar la \_ macro PropSheet IndexToId.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- PSM_INDEXTOID controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7a26cd97d324ae9bb4cfee85df00387c59293c7de8817b67da5605a207f07f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985725"
---
# <a name="psm_indextoid-message"></a>Mensaje \_ INDEXTOID de PSM

Toma el índice de una página de hoja de propiedades y devuelve su identificador de recurso. Puede enviar este mensaje explícitamente o usar la macro [**\_ PropSheet IndexToId.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la página.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de recurso de la página de hoja de propiedades especificada por *wParam* si se realiza correctamente. De lo contrario, devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





