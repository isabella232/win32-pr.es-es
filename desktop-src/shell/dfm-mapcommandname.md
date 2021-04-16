---
description: Enviado por la implementación predeterminada del menú contextual para asignar un nombre a un comando de menú.
title: Mensaje de DFM_MAPCOMMANDNAME (ShlObj. h)
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
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540502"
---
# <a name="dfm_mapcommandname-message"></a>DFM \_ MAPCOMMANDNAME

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

*pszCommandName* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el nombre del comando.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se implemente el objeto de menú contextual predeterminado. Hay dos API para su implementación, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 




