---
title: PSM_INDEXTOPAGE mensaje (Prsht.h)
description: Toma el índice de una página de hoja de propiedades y devuelve su identificador HPROPSHEETPAGE. Puede enviar este mensaje explícitamente o usar la \_ macro PropSheet IndexToPage.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- PSM_INDEXTOPAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167554"
---
# <a name="psm_indextopage-message"></a>Mensaje \_ INDEXTOPAGE de PSM

Toma el índice de una página de hoja de propiedades y devuelve su identificador HPROPSHEETPAGE. Puede enviar este mensaje explícitamente o usar la [**macro \_ PropSheet IndexToPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage)

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

Devuelve el identificador HPROPSHEETPAGE de la página de la hoja de propiedades especificada por *wParam* si se realiza correctamente. De lo contrario, devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





