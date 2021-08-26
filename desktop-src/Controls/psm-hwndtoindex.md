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
ms.openlocfilehash: 2ed61c958fb3a0b30ba7cf55d1040cac51caa67f460d329312fb0e798b016aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985835"
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

Devuelve el índice de base cero de la página de la hoja de propiedades especificada por *wParam* si se realiza correctamente. De lo contrario, devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





