---
description: Enviado por la implementación predeterminada del menú contextual durante la creación, especificando el comando de menú predeterminado y permitiendo realizar una elección alternativa. Usado por LPFNDFMCALLBACK.
title: Mensaje de DFM_GETDEFSTATICID (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423708"
---
# <a name="dfm_getdefstaticid-message"></a>DFM \_ GETDEFSTATICID

Enviado por la implementación predeterminada del menú contextual durante la creación, especificando el comando de menú predeterminado y permitiendo realizar una elección alternativa. Usado por [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*defaultID* \[ in, out\]
</dt> <dd>

Puntero al identificador del comando de menú seleccionado. Se reconoce la siguiente marca.

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**propiedades de DFM \_ cmd \_**


</dt> <dd>

Muestra la interfaz de usuario de **propiedades** del elemento en el que se invocó el menú.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Para invalidar la opción predeterminada del comando, el controlador debería, tras la recepción de este mensaje, establecer el valor señalado por *defaultID* en el identificador del comando de reemplazo y devolver S \_ correcto. Devuelve un código de error en caso contrario.

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se construya el objeto de menú contextual predeterminado. Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
