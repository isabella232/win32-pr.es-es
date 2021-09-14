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
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167537"
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

Identificador HPROPSHEETPAGE a la página de la hoja de propiedades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero de la página de hoja de propiedades especificada por *lParam* si se realiza correctamente. De lo contrario, devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





