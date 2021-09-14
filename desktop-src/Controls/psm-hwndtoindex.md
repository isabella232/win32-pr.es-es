---
title: PSM_HWNDTOINDEX mensaje (Prsht.h)
description: Toma el identificador de ventana de la página de la hoja de propiedades y devuelve su índice de base cero. Puede enviar este mensaje explícitamente o usar la macro PropSheet \_ HwndToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- PSM_HWNDTOINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167566"
---
# <a name="psm_hwndtoindex-message"></a>Mensaje \_ HWNDTOINDEX de PSM

Toma el identificador de ventana de la página de la hoja de propiedades y devuelve su índice de base cero. Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ HwndToIndex.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana de la página.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero de la página de hoja de propiedades especificada por *wParam* si se realiza correctamente. De lo contrario, devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





