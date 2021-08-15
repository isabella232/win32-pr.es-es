---
description: Se envía para comprobar la existencia de un comando de menú.
title: DFM_VALIDATECMD mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fd647d5cd6e171cc71e0968abb29d80e7aef5900d43fe4bd4b88f5f49bbdc7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721951"
---
# <a name="dfm_validatecmd-message"></a>Mensaje \_ VALIDATECMD de DFM

Se envía para comprobar la existencia de un comando de menú.


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmd* 
</dt> <dd>Desplazamiento del identificador del comando de menú.</dd> <dt>

*lParam* 
</dt> <dd>No se usa. Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S OK si el comando existe o S FALSE en caso \_ \_ contrario.

## <a name="remarks"></a>Observaciones

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada en función de cómo se construya el objeto de menú contextual predeterminado. Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX es**](dfm-invokecommandex.md) una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX si** la información adicional proporcionada por esa interfaz es necesaria en la implementación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




