---
description: Enviado por la implementación predeterminada del menú contextual para asignar un nombre a un comando de menú.
title: DFM_MAPCOMMANDNAME mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3dac1cdb3c04397a59b26a2212fe1c46b611ce72ba029aabd25e0b01c9000b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459981"
---
# <a name="dfm_mapcommandname-message"></a>Mensaje \_ MAPCOMMANDNAME de DFM

Enviado por la implementación predeterminada del menú contextual para asignar un nombre a un comando de menú.


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*defaultID* \[ in, out\]
</dt> <dd>

Puntero al identificador del comando de menú seleccionado.

</dd> <dt>

*pszCommandName* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el nombre del comando.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada en función de cómo se implemente el objeto de menú contextual predeterminado. Hay dos API para su implementación, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)y [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX es**](dfm-invokecommandex.md) una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX si** la información adicional proporcionada por esa interfaz es necesaria en la implementación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




