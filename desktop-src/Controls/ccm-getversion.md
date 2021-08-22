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
ms.openlocfilehash: fb1ad49ebb00d5d57555bb07be1bcf78ab97115ada43e18a7f81cda93e29fa1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320265"
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

Devuelve el número de versión establecido por el mensaje [**\_ SETVERSION de CCM**](ccm-setversion.md) más reciente. Si no se ha enviado ningún mensaje de este tipo, devuelve cero.

## <a name="remarks"></a>Comentarios

Este mensaje no devuelve la versión del archivo DLL. Vea [Versiones de shell](common-control-versions.md) para obtener una explicación sobre cómo usar [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para recuperar la versión actual de DLL.

> [!Note]  
> El número de versión se establece en función del control y puede que no sea el mismo para todos los controles.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

