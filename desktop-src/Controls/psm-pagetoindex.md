---
title: PSM_PAGETOINDEX mensaje (Prsht.h)
description: Toma el identificador HPROPSHEETPAGE de la página de la hoja de propiedades y devuelve su índice de base cero. Puede enviar este mensaje explícitamente o usar la \_ macro PropSheet PageToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- PSM_PAGETOINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71651853d0d403c25a0f8c554bd31c2ae649bcf0258b6f1f578a03cc65a3b539
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985675"
---
# <a name="psm_pagetoindex-message"></a>Mensaje \_ PAGETOINDEX de PSM

Toma el identificador HPROPSHEETPAGE de la página de la hoja de propiedades y devuelve su índice de base cero. Puede enviar este mensaje explícitamente o usar la [**macro \_ PropSheet PageToIndex.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador HPROPSHEETPAGE en la página de la hoja de propiedades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero de la página de hoja de propiedades especificada por *lParam* si se realiza correctamente. De lo contrario, devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





