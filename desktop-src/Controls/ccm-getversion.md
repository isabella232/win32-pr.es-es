---
title: Mensaje de CCM_GETVERSION (commctrl. h)
description: Obtiene el número de versión de un control establecido por el mensaje de SETVERSION de CCM más reciente \_ .
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150563"
---
# <a name="ccm_getversion-message"></a>\_Mensaje GETVERSION de CCM

Obtiene el número de versión de un control establecido por el mensaje [**de \_ SETVERSION de CCM**](ccm-setversion.md) más reciente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de versión establecido por el mensaje [**de \_ SETVERSION de CCM**](ccm-setversion.md) más reciente. Si no se ha enviado ningún mensaje de este tipo, devuelve cero.

## <a name="remarks"></a>Observaciones

Este mensaje no devuelve la versión del archivo DLL. Consulte [versiones de Shell](common-control-versions.md) para obtener una explicación de cómo usar [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para recuperar la versión de dll actual.

> [!Note]  
> El número de versión se establece en un control según el control y puede no ser el mismo para todos los controles.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

