---
title: PSM_IDTOINDEX mensaje (Prsht.h)
description: Toma el identificador de recurso de una página de hoja de propiedades y devuelve su índice de base cero. Puede enviar este mensaje explícitamente o usar la \_ macro PropSheet IdToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- PSM_IDTOINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167562"
---
# <a name="psm_idtoindex-message"></a>Mensaje \_ IDTOINDEX de PSM

Toma el identificador de recurso de una página de hoja de propiedades y devuelve su índice de base cero. Puede enviar este mensaje explícitamente o usar la [**macro \_ PropSheet IdToIndex.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de recurso de la página.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero de la página de hoja de propiedades especificada por *lParam* si se realiza correctamente. De lo contrario, devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





