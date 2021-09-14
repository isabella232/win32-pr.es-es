---
title: PSM_INDEXTOHWND mensaje (Prsht.h)
description: Toma el índice de una página de hoja de propiedades y devuelve su identificador de ventana. Puede enviar este mensaje explícitamente o usar la macro PropSheet \_ IndexToHwnd.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- PSM_INDEXTOHWND controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167561"
---
# <a name="psm_indextohwnd-message"></a>Mensaje \_ DE PSM INDEXTOHWND

Toma el índice de una página de hoja de propiedades y devuelve su identificador de ventana. Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ IndexToHwnd.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd)

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

Devuelve el identificador a la ventana de la página de la hoja de propiedades especificada por *wParam* si se realiza correctamente. De lo contrario, devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





