---
title: CCM_GETVERSION mensaje (Commctrl.h)
description: Obtiene el número de versión de un control establecido por el mensaje SETVERSION de CCM \_ más reciente.
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION controles de Windows mensaje
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160289"
---
# <a name="ccm_getversion-message"></a>Mensaje \_ GETVERSION de CCM

Obtiene el número de versión de un control establecido por el mensaje [**\_ SETVERSION de CCM más**](ccm-setversion.md) reciente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de versión establecido por el mensaje [**\_ SETVERSION de CCM más**](ccm-setversion.md) reciente. Si no se ha enviado ningún mensaje de este tipo, devuelve cero.

## <a name="remarks"></a>Observaciones

Este mensaje no devuelve la versión del archivo DLL. Consulte [Versiones de Shell](common-control-versions.md) para obtener una explicación de cómo usar [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para recuperar la versión actual de DLL.

> [!Note]  
> El número de versión se establece en un control por control y puede que no sea el mismo para todos los controles.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

